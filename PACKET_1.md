# Dark Factory — Packet 1

**Status:** Locked with CONSTITUTION.md Rev 0.4  
**Date:** 2026-08-24  
**Kind:** First implementation packet. Not a second constitution. Not the factory binary.

This packet names what Rev 0.4 left as “the next document”: the kernel you actually build, the on-disk layout, the schemas, the language, the proofs this packet must turn green. Constitution is what. This is the first how.

If a sentence here conflicts with CONSTITUTION.md, the constitution wins and this packet is wrong.

---

## 1. Scope

Packet 1 ships a factory that can `serve`, `bind grok` (and `bind codex` if the client id is in hand), `admit` a typed spec, run one Produce worker through the door, verify with programs, and `ship` a tarball — or raise a closed exception. Zero HIL on the happy path.

Against: `examples/add.yaml` (the §24 admissible spec).

Proofs this packet must turn green: **P1–P6, P9, P11, P16–P19, P21, P23, P24, P26.**

Packet 2 (not this document): P7 crash, P8 remaining-path NEVER_DO, P10 slop-repair depth, P13 fetch-cap, P14 think-in-code, P15 map budget, P20 rotate, P22 sandbox depth, P25 delta slop on a brownfield baseline.

---

## 2. Language

**Go.** One binary. Unix socket, flock, JSON, `os/exec`. No framework. Module path: `github.com/AtonoRobotics/dark_factory`.

The product in `examples/add.yaml` is Rust. That is the SKU, not the plant. The plant does not need two languages in packet 1’s own tree.

Go 1.23+. `CGO_ENABLED=0`.

---

## 3. Tree

```
CONSTITUTION.md
PACKET_1.md
README.md
.gitignore
schema/
  spec.v1.json          # JSON Schema for a factory spec (YAML is the admit encoding)
  effect.v1.json        # proposed effect list (worker → kernel)
  pass.v1.json          # compiled pass (kernel → worker)
  work_order.v1.json
  evidence.v1.json
examples/
  add.yaml              # admissible. P1 target.
  reject-incomplete.yaml
  reject-waiver.yaml
  reject-slop-required.yaml
cmd/darkfactory/
  main.go               # CLI. Parses argv. Dials the socket. serve is the same binary.
internal/
  kernel/
    admit.go            # schema + unknown-key + waiver + typed oracles
    door.go             # effect admit/refuse
    journal.go          # append-only JSON lines
    order.go            # work order compile (first SKU: one grant)
    context.go          # compile working set; refuse naked/stale
    verify.go           # run oracles + gates
    ship.go             # tarball + evidence
    sandbox.go          # product tree isolation
    flock.go            # one serve
    kill.go
    budget.go
  vault/
    vault.go            # adapter secrets. never logged.
  adapter/
    port.go             # model_call
    grok.go             # device-code
    codex.go
  produce/
    port.go             # encode pass, decode effects
    worker.go           # in-process worker that speaks the port. not a wrapped CLI.
  cli/
    serve.go
    bind.go
    commands.go
proof/
  p1_clean_ship_test.go
  p2_incomplete_test.go
  ...                   # one file per packet-1 proof
```

No `internal/station` package. No persona names. Produce is `internal/produce`. Everything else is `internal/kernel` or `internal/adapter`.

---

## 4. On-disk instance

`serve --dir <instance>` (default: `$XDG_STATE_HOME/darkfactory`, else `~/.local/state/darkfactory`).

```
<dir>/
  factory.lock          # flock. second serve exits 1.
  factory.sock          # unix socket. 0600. uid of the server is the principal.
  journal.jsonl         # append-only. no secrets.
  vault/                # 0700. adapter tokens. gitignored.
  compile/              # context compiles by pass_id. pointers from the journal.
  product/              # the product tree. the only mutable surface for Produce.
  baseline/             # snapshot at admit. first SKU: empty.
  ship/                 # last tarball + evidence.json
```

Socket path override: `--socket`. Default `$XDG_RUNTIME_DIR/darkfactory.sock`.

---

## 5. CLI

Same binary. `darkfactory <command>`. Talks to the socket except `serve`.

| Command | Packet 1 | Notes |
|---|---|---|
| `serve --dir --socket` | yes | No browser. Takes the flock. Logs to stderr, never tokens. |
| `bind grok` / `bind codex` | yes | Print `user_code` and `verification_uri`. Poll. Vault. Exit 0. No token on stdout. |
| `unbind <adapter>` | yes | |
| `rotate <adapter>` | packet 2 | Packet 1: unbind + bind. P20 is packet 2. |
| `status` | yes | JSON to stdout: state, adapters bound (bool), budgets, wo_id, exceptions. |
| `admit <path.yaml>` | yes | |
| `kill` | yes | |
| `exceptions` | yes | |
| `exception <id> <answer.json>` | yes | Answers: `{"action":"refuse"}` \| `{"action":"grant"}` \| `{"action":"rewrite_spec"}`. No free text that starts the line. |
| `ship` | yes | Writes tarball path + `overall` bit to stdout. |
| `journal [--tail] [--pass <id>]` | yes | |
| `evidence` | yes | |
| `grant` | yes | |
| `context show <pass-id>` | yes | Prints the compiled pass JSON. |

Unknown command → exit 2. Unbound `admit` that would model_call → P18 (refuse, no files).

CLI never has `--token`, `--api-key`, `--refresh`. Those flags do not exist.

---

## 6. State machine

One work order. Sequential.

```
idle → admitting → admitted
                 ↘ exception
admitted → producing → verifying
verifying → shipping → shipped
          ↘ repairing (repair_left > 0) → producing
          ↘ exception (REPAIR_EXHAUSTED | BUDGET_EXCEEDED | NEVER_DO | …)
any non-terminal → killed   (on kill)
```

Illegal transition is a kernel bug, not an exception. Journal every transition. Crash resume: last journal record whose effects are durable (write is rename-atomic). Context recompiled. Not an exception.

Second `admit` while not idle/shipped/exception/killed → refuse, exit 1, P23. Second `serve` → flock fail, P16.

---

## 7. Admit

Read YAML. Convert to JSON. Validate `schema/spec.v1.json`. Then:

1. Unknown root key → `SPEC_INCOMPLETE` is wrong; this is **`SPEC_CONTRADICTION`** (waiver-shaped or not: unknown is refuse).
2. Any of `skip_doctrine`, `waive_doctrine`, `allow_slop`, `quality_override`, `hil_review`, `skip_gates`, `human_lgtm` at any depth → `SPEC_CONTRADICTION`. P11.
3. `done_when` empty, missing, or an item without a known `kind` or with a string item → `SPEC_INCOMPLETE`. P2, P24.
4. `constraints.perf` set with no oracle → `SPEC_INCOMPLETE`.
5. `in_scope` requires what doctrine forbids (TODO graves, unused utils “just in case”) → `SPEC_CONTRADICTION`.
6. Pin `doctrine_hash` (hash of the doctrine text welded in this binary). Compile one grant `paths: ["**"]`, all oracle ids, `allow_run: false`. Snapshot empty baseline. Default budgets if omitted.

No model in admit.

---

## 8. Produce worker

In-process. Speaks `schema/pass.v1.json` in, `schema/effect.v1.json` out. The kernel:

1. Compiles context (spec slice, doctrine, named files, map stub, evidence, grant).
2. Calls `adapter.model_call` with that pass as the user message and a system prefix that is doctrine + spec slice (prompt-cache keys).
3. Expects the model to return **only** the effect JSON. Parse. If not valid effects → refuse the pass, count as a repair-cycle fail, do not write files.
4. Door each effect. Execute admitted. Journal.

The worker does not `exec`, does not read the host, does not call the vendor. Kernel does. Wrapping Codex CLI / Claude Code / Cursor is a packet-1 fail.

Packet 1 structural map: file list + first-line package/module names. Full tree-sitter ranking is packet 2 (P15). Map still must list every file under `product/`. Empty product on first pass is legal (greenfield).

Packet 1 think-in-code: not required (P14 is packet 2). Raw tool bodies still must not enter the pass (kernel never puts `run` stdout in the next compile except the summary record in evidence).

---

## 9. Door (packet 1)

Admit `write` / `delete` / `rename` iff path is relative, clean (`path.Clean`, no `..`), under `product/`.  
Admit `run` only from Verify, or from Produce if `grant.allow_run` (first SKU: false).  
Admit `fetch_handle` iff handle exists and `max_bytes` ≤ remaining fetch budget.  
Admit `raise_exception` iff `code` is on the closed list.  
Admit `grant_expand` → packet 1: **refuse** unless the path is already inside `**` (first SKU grant is the whole tree, so expand is a no-op). P26 still has a test: a write to `/etc/passwd` or `../kernel` is refused.

Unknown type → refuse.

---

## 10. Verify (programs)

For each work-order oracle, run in the product sandbox:

- `command` / `probe`: `exec` with `network=off`, `cwd=product/`, timeout. `probe` runs `build` first if set.
- `file` / `hash`: stat + sha256.
- `not_present`: regex over delta files (first SKU delta = all product files).

Gates this packet implements (delta = product tree vs baseline):

| Gate | How |
|---|---|
| SLOP_RESIDUE | regex `TODO\|FIXME\|placeholder\|lorem\|example\.com` on new/changed files |
| SLOP_SECRET | regex on `sk-`, `ghp_`, `xai-`, `Bearer `, plus high-entropy quoted strings ≥ 32 |
| SLOP_GOD | new path basename in `util`, `utils`, `helper`, `helpers`, `common`, `misc`, `dump` |
| SLOP_GOLD | `go.mod`/`Cargo.toml`/`package.json` added a dep with a single import site in the delta |
| SLOP_UNUSED | packet 1: new file under product/ that nothing in the tree references by name, and that is not the file oracle. Cheap. |
| SLOP_TEST_THEATER | new `*_test.go` / `*_test.rs` / `*.test.ts` whose body is only `expect(true)` / `assert True` / `assert.True(t, true)` |

`SLOP_DUP` / `SLOP_LIE`: do not block. Doctrine prefix only.

---

## 11. Sandbox (packet 1)

Minimum that makes P1 safe enough to run `cargo test` on a machine you own:

- `chdir` to `product/`
- extra files: none
- env: stripped. `PATH` = toolchain only (`cargo`, `rustc`, `go` as needed for the SKU). No `DARKFACTORY_*`. No vault path.
- network: `setrlimit` is not network. Packet 1 network deny: unset proxy env; if `landlock` or `bubblewrap` is present, use it to deny `AF_INET`. If not present, **document the hole** and still unset env; P22 is packet 2.
- no read of `<dir>/vault`, `<dir>/journal.jsonl`, kernel binary dir.

Writes from Produce go through kernel `write` (temp file in `product/.tmp/` + `rename`). Not through the worker.

---

## 12. Adapters (packet 1)

Device-code. Packet data (vendor-volatile; change without a constitution bump):

| Adapter | Device code URL | Token URL | Client id |
|---|---|---|---|
| grok | fill from xAI device-code docs at implement time (`accounts.x.ai`) | fill | fill |
| codex | `https://auth.openai.com/api/accounts/deviceauth/usercode` | fill from Codex CLI | fill |

If the client id is not in hand, `bind grok` still has to print `user_code` + `verification_uri` against the live vendor or fail closed with `MISSING_AUTHORITY`. Do not scrape. Do not add `--api-key`.

`glm` does not exist as a command.

Unbound → no `model_call`. P18.

Vault file: `<dir>/vault/<adapter>.json` mode 0600. Fields `access_token`, `refresh_token`, `expiry`. Journal records `{adapter, event: bound|unbound|refresh_fail}` with no secret bytes. `status` prints `bound: true|false`.

---

## 13. Defaults

From constitution §14, welded here:

```
repair_cycles: 3
wall_clock_s: 3600
model_calls: 40
fetch_bytes_per_pass: 32768
map_tokens: 2000
```

---

## 14. Shipment

`ship/` contains:

- `product.tar` — tar of `product/`, sorted names, uid/gid 0, mtime epoch, gzip. sha256 next to it.
- `evidence.json` — oracles + gates + `overall: pass|fail`
- `journal.slice.jsonl` — records for this `wo_id`
- `exception.json` — `[]` on a clean ship

Stdout of `darkfactory ship`:

```json
{"overall":"pass","tar":"<dir>/ship/product.tar","evidence":"<dir>/ship/evidence.json"}
```

Red evidence still produces the tar. `overall` is `fail`. Callers read the bit.

---

## 15. Proof harness

`go test ./proof/...` is the packet-1 gate. Each P-file is a real run against a temp `--dir`, not a mock of the door.

| Test | Spec fixture | Expect |
|---|---|---|
| P1 | `examples/add.yaml` | `overall=pass`, zero exceptions, tarball has a binary that prints `5` and `ok` |
| P2 | `examples/reject-incomplete.yaml` | `SPEC_INCOMPLETE`, `product/` empty |
| P3 / P11 | `examples/reject-waiver.yaml` and `examples/reject-slop-required.yaml` | `SPEC_CONTRADICTION`, no product files |
| P4 | fixture whose first produce is forced to fail one oracle (seed a broken product tree via a test-only kernel hook **or** a spec whose first cargo test fails until repair). Prefer: worker stub in test that emits a bad write, then a good write. | first verify fail, second pass, no exception |
| P5 | worker stub always emits slop residue | `REPAIR_EXHAUSTED`, `overall=fail` |
| P6 | kill during a slow write | no path outside product; no further journal execute after `killed` |
| P9 | call produce without `compile_context` | refuse, no write |
| P16 | `serve` twice | second exits non-zero |
| P17 | `bind grok` against a fake device-code HTTP | stdout contains `user_code` and `verification_uri`, not the access token |
| P18 | admit with vault empty | no model HTTP, no product files |
| P19 | after bind, grep journal/status/argv | no token bytes |
| P21 | worker writes tests that pass and a product that fails the work-order probe | `overall=fail` |
| P23 | admit twice | second refuse |
| P24 | prose `done_when` | `SPEC_INCOMPLETE` |
| P26 | effect `write` path `/etc/passwd` or `../vault/x` | refuse, no write |

P1 needs a bound adapter **or** a test double behind `internal/adapter.Port`. The double is a fake `model_call` that returns canned effects. Production `serve` does not install the double. Tests may.

A P1 that pages a human fails the packet.

---

## 16. Done when (this packet)

Packet 1 is done when:

1. `go test ./proof/...` is green for the table in §15.
2. `go build -o darkfactory ./cmd/darkfactory` produces one binary.
3. `darkfactory serve` on a box with `DISPLAY` unset does not exec a browser (P16).
4. CONSTITUTION.md is unchanged in meaning. This packet does not patch doctrine.

Out of packet 1: web UI, queueing, glm, brownfield DAGs, git push, images, Temporal, Magnus, context-mode, tree-sitter vendor, FTS, rotate, landlock-if-absent as a hard fail.

---

## 17. Build order

Do not start Produce until the door, journal, admit, and P2/P11/P16/P18/P23/P24 are green. A worker on an open door is not a factory.

1. CLI + serve + flock + journal  
2. admit + spec schema  
3. vault + bind (fake HTTP in tests, live vendor in a manual bind)  
4. door + atomic write  
5. verify programs + gates  
6. produce port + worker  
7. P1 against `examples/add.yaml`  
8. remaining packet-1 proofs  

---

## 18. Doctrine text

Weld the doctrine (CONSTITUTION.md §7 D1–D13 plus §8 gate names) as a string in `internal/kernel/doctrine.go`. Hash it. That hash is `doctrine_hash` on the work order. Changing doctrine is a factory version bump, not a spec field.
