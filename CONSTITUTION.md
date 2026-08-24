# Dark Factory — Constitution

**Status:** Rev 0.4 (Locked machine)  
**Date:** 2026-08-24  
**Kind:** Greenfield. Own repo. Separate from Magnus, alphavector-core, Mission Control, and Buyer Agent Ops.

> Cognitive runtimes propose. The factory admits. Durable work executes. Evidence owns truth.

## 0. Preamble

*locked — What 0.4 is, what changed, the filter that still kills theater.*

Dark Factory is an autonomous software plant. A principal submits a spec. The factory builds the smallest complete product that spec allows under doctrine. Correctly. Efficiently. Lights-out.

A human is not in the manufacturing path. A human authors the spec, answers a closed exception list, and can kill the line. That is the whole human job.

| Field | Value |
| --- | --- |
| Status | Rev 0.4 — locked machine |
| Date | 2026-08-24 |
| Kind | Greenfield. Own repo. Separate from Magnus, alphavector-core, Mission Control, Buyer Agent Ops. |
| Supersedes | Rev 0.3 (constitution). 0.3 remains the intent. 0.4 is the machine 0.3 was missing. |

> **Filter (unchanged)** (lock)
>
> A piece stays only if it is necessary to turn a spec into the smallest complete product that spec allows under doctrine, or it makes that cheaper or faster. No theater. No review bureaucracy. No second habitat OS. No slop.

If ordinary work waits on a person, the factory is broken. If a station runs without a fresh context compile, the factory is broken. If slop can ship, the factory is broken. If Produce certifies its own tests, the factory is broken. If Verify is a model, evidence is not mechanical.

> **What 0.4 locks that 0.3 left as slogans** (note)
>
> Typed done_when. Typed effects with default-deny egress. Product sandbox. Oracle authorship (work-order oracles ≠ Produce’s tests). Kernel programs vs one model station. Deterministic ship-blocking gates. First SKU. Produce port protocol. grok + codex only. Sequential one-line instance. Unix-socket CLI. Delta slop. Doctrine pin. GRANT_INSUFFICIENT. Kill atomicity. Fetch-byte cap. Think-in-code as refused-if-violated law.

References (shape only — do not install or copy): Magnus (context-craft, device-code bind). Cognitive Runtime Gateway / Habitat / Temporal / PostgreSQL locks (admission + durable journal + single-writer). mksglu/context-mode (sandbox → summary + handle, think-in-code, event index — not the kernel). Aider repo map (tree-sitter outline + ranked neighbors — not Aider).

---

## 1. Purpose

*locked — Smallest complete product. Not “best.” Not a spec-to-slop compiler.*

You give it a spec. It ships the smallest complete product that spec allows under doctrine. It does not translate a spec into whatever compiles. A shipment that passes tests and is slop is a failed shipment.

> **“Best” is struck** (lock)
>
> Rev 0.3 said “the best product that spec allows.” That word licenses gold-plating Produce will invent and doctrine will have to kill. The factory metric is size under a green evidence pack: fewest files, fewest dependencies, fewest layers, shortest typed surface that satisfies every oracle. There is no bakeoff of two candidates. Size is gates, not a second Produce.

**1.1 Lights-out.** The line runs to ship or to a listed exception. No plan approval. No LGTM. No “does this look clean?”

**1.2 Evidence owns done.** Correctly means every typed done_when oracle is green and every deterministic doctrine gate is green. A model saying it looks right is not evidence.

**1.3 Efficiency is a budget.** If the spec omits budgets, defaults apply. The line cannot wander. Token, wall-clock, model-call, and repair ceilings are real.

---

## 2. What it is not

*locked — Closed kill list. Same spine as 0.3, plus the holes 0.3 would have fallen into.*

| Not | Why |
| --- | --- |
| A habitat OS | Magnus already owns named agents, wakes, and running a domain org. |
| A chatbot that writes code on request | This is a plant. Work orders run to done or exception. |
| A spec-to-slop compiler | Passing done_when is necessary, not sufficient. |
| A skill pack | Context and doctrine are welded. They cannot be forgotten, unloaded, or @-invoked. |
| A PR approver | Review theater is HIL in disguise. Doctrine is mechanical, not a human LGTM. |
| An orchestrator of humans | Humans are not a station on the line. |
| Cursor-dependent | Cursor is unavailable as a product runtime. Factory owns its workers. |
| A pack inside alphavector-re or Mission Control | Own repo, own project. |
| A second Magnus | May later run on a habitat. The factory spec does not depend on one. |
| A laptop app | Runtime is a remote headless server. |
| A pasted-key product | Subscriptions bind with device/machine-code OAuth. Keys do not live in argv, env files, or shell history. |
| A browser-login product | No scraping. No server-side browser for model auth. |
| A firm of chat personas | One model station: Produce. Everything else is a kernel program. |
| A wrapper around Codex CLI / Claude Code / Cursor | Those ports swallow raw tool bodies. Unfit under the produce protocol. |
| A Temporal replay of Produce | Kernel sequencing is a deterministic state machine. Produce is not. Resume continues; it does not bit-reproduce the tree. |

---

## 3. Authority boundary

*locked — Cognitive runtimes propose. The factory admits. Durable work executes. Evidence owns truth.*

| Noun | Owns | Does not own |
| --- | --- | --- |
| Spec | Product law: purpose, in/out, never_do, typed done_when, constraints, budgets. | Execution, evidence, shipping, taste, doctrine waiver. |
| Doctrine | How software is made. Factory law. Versioned with the factory. Pinned onto the work order at admit. | What product to build. |
| Context | The working set compiled into every station pass. Fresh every pass. | Effects, shipping. |
| Factory kernel | Admission door, work-order compile, context compile, doctrine gates, station dispatch, effect execution, exception raise, kill, crash recovery, sandbox, vault. | Model brand, editor chrome. |
| Produce | A proposed effect list under a grant, inside a compiled context. | Bypass the door, widen the spec, unload context or doctrine, ship, author ship-blocking oracles. |
| Evidence store | Whether the product matches the spec and the doctrine. | What the product should be. |
| Product | The built thing (tree, tarball). | Authority to declare itself done. |
| Principal | Spec authorship, exception answers, kill, budget ceiling, product-secret grant. | Ordinary station steps, taste waiver, oracle invention after admit. |

Admission is mechanical. Produce proposes an effect. The door checks spec + doctrine + work order + budget + egress + sandbox. Yes or no. No person in that check.

A spec that requires slop (placeholders, unused layers, “leave TODOs”, copy a bad pattern) fails admission or is interpreted to the spec’s purpose under doctrine. Doctrine wins ties. Doctrine never invents product the spec did not ask for.

> **Spec vs doctrine conflict** (refuse)
>
> Spec says what. Doctrine says how. Spec cannot waive doctrine. Doctrine cannot add product the spec did not ask for. Conflict → SPEC_CONTRADICTION. Do not “be helpful” and ship a compromise.

---

## 4. First SKU

*first-ship — The first machine the plant is allowed to run. Unbounded P1 was a hole.*

A “complete spec → shipment” proof of a hello-world does not prove a plant. First ship is not a general coding agent. It is one SKU.

**4.1 Greenfield.** Empty baseline tree, or a snapshot the principal points at. No clone-from-remote unless a deploy right is already in the vault (MISSING_AUTHORITY otherwise).

**4.2 One language, one process.** The spec names exactly one language. No GUI chrome. No third-party SaaS. No extra runtime (browser, mobile, cluster).

**4.3 Typed oracles only.** done_when is a non-empty list of closed-kind checks. Prose-only items are SPEC_INCOMPLETE.

**4.4 Offline tests.** Verify runs with network deny. Oracles that need the network fail admit or need an egress grant — first SKU has none.

**4.5 Shipment shape.** Product directory + tarball + evidence pack + journal slice. Not a git push. Not a container image. Those are later packets under MISSING_AUTHORITY.

**4.6 Sequential instance.** One serve, one active work order, one grant in flight. Second admit refused until terminal (shipped / exception / killed). Second serve process refused by an instance lock.

> **This is not theater** (lock)
>
> Bounding the first SKU is how P1, P4, and P10 become proofs instead of demos. Later SKUs (brownfield, service with HTTP, image ship) are packets. They do not leak into kernel 1.

---

## 5. Spec contract

*locked — Agent-readable product law. Schema, unknown-key refuse, no waiver keys.*

A factory spec is versioned product law. Stations cannot write it. The kernel admits it or raises. There is no skip_doctrine field. If someone adds one, admission refuses it as SPEC_CONTRADICTION.

> **Unknown-key policy** (lock)
>
> Unknown keys at the root are refused. An extensions map is the only evolution hatch; the kernel ignores it and it must not contain waiver-shaped keys (skip_doctrine, waive_doctrine, allow_slop, quality_override, hil_review, skip_gates). Those names at any depth under extensions are SPEC_CONTRADICTION.


*Spec schema v1. Required fields marked. Kernel fills doctrine_hash and spec_hash at admit.*

```yaml
spec_version: "1.0"          # required. unknown version → SPEC_INCOMPLETE
purpose: string              # required. 1–4 sentences. what the product is for.
principal:
  id: string                 # required. who may answer exceptions and kill.

in_scope: [string]           # required. min 1.
out_scope: [string]          # required. may be empty, must be present.
never_do: [string]           # required. may be empty, must be present.
                             # factory-welded never_do always applies in addition.
must_ask_when: [string]      # optional. extra exception predicates the principal adds.

done_when:                   # required. min 1. closed kinds only. see §6.
  - kind: command | probe | file | not_present | hash
    # fields per kind

constraints:
  language: string           # required for first SKU. exactly one.
  license: string            # required. ownership of output.
  compatibility: [string]    # optional.
  perf: string               # optional. if present, must be oracle-backed in done_when.

budgets:                     # optional. omitted fields take defaults in §14.
  repair_cycles: int
  wall_clock_s: int
  model_calls: int
  fetch_bytes_per_pass: int
  map_tokens: int

extensions: {}               # optional. kernel-inert. no waiver keys.

# FORBIDDEN at root (and anywhere in extensions):
# skip_doctrine, waive_doctrine, allow_slop, quality_override,
# hil_review, skip_gates, human_lgtm
```

If done_when is missing, empty, or contains an unknown kind or prose-only item, admission fails SPEC_INCOMPLETE. The factory does not guess a product the spec did not specify. If two requirements cannot be true together, or the spec requires what doctrine forbids, SPEC_CONTRADICTION. No code is written.

> **Improve** (note)
>
> There is no Improve station. A spec patch is a new admit by the principal. Produce must not write the spec file.

---

## 6. Typed oracles

*locked — done_when is a closed set of checks. Produce does not author ship-blocking evidence.*

This is the admission door for completeness and the only path to “done.” A free-text done_when makes admit a model and evidence a vibe.

| Kind | Fields | Passes when |
| --- | --- | --- |
| command | run: string, expect.exit: int, expect.stdout_contains?: string, expect.stdout_eq?: string, expect.timeout_s?: int (default 120) | Sandbox run of argv/shell-form against the product tree matches expect. Network deny. |
| probe | Same as command, but run against the built artifact after a named build command. | Same, after the build step the oracle names (build?: string). |
| file | path: string (posix, relative to product root). sha256?: hex. | Path exists in the shipment. If sha256 set, it matches. |
| not_present | pattern: regex, in: shipped_tree | delta | No match in the named set. delta = work-order added/changed files only. |
| hash | path: string, sha256: hex | File exists and digest matches. Stricter file. |


*Admissible done_when (first SKU shape).*

```yaml
done_when:
  - id: unit
    kind: command
    run: cargo test --offline
    expect: { exit: 0, timeout_s: 180 }
  - id: binary
    kind: probe
    build: cargo build --release --offline
    run: ./target/release/app --health
    expect: { exit: 0, stdout_contains: "ok" }
  - id: entry
    kind: file
    path: src/main.rs
  - id: no_todos
    kind: not_present
    pattern: "TODO|FIXME|placeholder|lorem|example\.com"
    in: delta
```

**6.1 Unknown kind → SPEC_INCOMPLETE.** No “kind: vibe”. No untyped string items. No “the app works.”

**6.2 Work-order oracles are copied at admit.** Compile freezes the oracle list onto the work order. Produce cannot add, delete, or edit ship-blocking oracles.

**6.3 Produce may add tests.** Those tests may run as part of a command oracle if the oracle’s run line says so. They are not themselves the oracle. A green product test tree with a red work-order oracle is a fail.

**6.4 Verify is a program.** Kernel runs each oracle in the product sandbox, writes a structured record (id, kind, exit, digest, pass/fail). No model in this path.

**6.5 perf constraints must be oracles.** A constraints.perf sentence with no matching command/probe is SPEC_INCOMPLETE.

> **Homework-grading is a factory bug** (refuse)
>
> If Produce writes the only tests that Verify runs, a clever Produce ships slop with a green sticker. Work-order oracles are authored from the spec at admit, before Produce runs. P21 exists to prove this.

---

## 7. Doctrine

*locked — Factory opinion. Specs do not vote. Taste in context. Only programs block ship.*

Doctrine has two faces. In context: Produce cannot think without it, so slop is not the default draft. In verify: mechanical gates. A green done_when with a red doctrine gate is a fail. Repair, do not ship.

Doctrine is versioned with the factory, not with a product spec. The work order pins doctrine_hash at admit. Mid-line doctrine bumps do not re-judge in-flight work. The next admit gets the new law.

**D1 Purpose-shaped.** Every file, type, and dependency exists because the spec needs it. No leftover scaffolding. No “utils just in case.”

**D2 One way.** One pattern per job. No parallel abstractions. No framework soup.

**D3 Truth in one place.** No duplicated state. No shadow config. No comment that contradicts the code.

**D4 Names are the design.** A reader can say what a module does from its name and signature. No Manager / Helper / Util dumping grounds.

**D5 Smallest complete shape.** Extract on the second real use, not the first imagined one. No premature layer.

**D6 Effects at the edge.** IO, network, time, randomness live at boundaries. Core is deterministic and testable.

**D7 Tests prove the spec.** Tests may support a command oracle. They are not coverage theater, snapshots that bless slop, or mocks of the thing under test.

**D8 Errors are information.** Fail closed. Named. Recoverable. No swallow. No “should never happen.”

**D9 Delete is a feature.** Unused code, unused deps, unused flags die in the same shipment that made them unused.

**D10 Readable over clever.** No puzzle code. Complexity only where the problem is complex.

**D11 Boundaries are contracts.** If it crosses a station, process, or package edge, it is typed, versioned, and tested. Internals may move.

**D12 No residue.** No TODO without a work-order grant, no placeholders, no example.com, no commented-out graves, no generated junk left in.

**D13 The diff is the unit.** A produce step is the obvious right change. Volume of files touched is not progress.

Taste that cannot be gated stays in context (Produce sees the law). It does not become a human review and it does not become a model-in-Verify. If two shapes would both pass spec + gates, Produce emits one. The factory does not run a bakeoff. Size is enforced by the gates below.

> **Ship-blocking verify is deterministic** (lock)
>
> Only programs can flip the done bit. A model may annotate the journal. It must not flip ship. Replay of Verify on the same tree must yield the same bits. Stochastic re-judge is a factory bug.

---

## 8. Mechanical slop gates

*locked — Programs that fail a shipment even when oracles are green. Applied to the work-order delta unless noted.*

Gates score the work-order delta against the baseline tree. Inherited slop is the principal’s problem unless a done_when oracle says clean it. Greenfield baseline is empty, so delta = shipment.

| Gate | Fail when (program) | Not this |
| --- | --- | --- |
| SLOP_RESIDUE | New/changed shipped files match TODO|FIXME|placeholder|lorem|example.com|commented-out graves (heuristic: consecutive commented lines that used to be code). | Pre-existing matches in the baseline (use not_present/in: shipped_tree if the spec wants a clean tree). |
| SLOP_UNUSED | Compiler/depcheck reports a new unused export, unused dependency, or a file added by this work order that nothing imports. | Baseline dead code. |
| SLOP_GOD | A new path whose final component is util(s)|helper(s)|common|misc|dump, or a new module that exports ≥3 unrelated names with no shared type (tree-sitter: no common parent type / no shared prefix in the spec’s in_scope nouns). | A spec-named module that happens to be large. |
| SLOP_TEST_THEATER | A test file added this work order whose assertions are only mock-equality, expect(true), or snapshots of implementation source. | A command oracle that shells out to a real runner. |
| SLOP_GOLD | A new runtime dependency with a single import site, or a new directory with a single call site, and no constraints.language / constraints.compatibility requiring it. | A dependency the spec named. Stdlib. The first SKU’s one language toolchain. |
| SLOP_SECRET | Credential/token shaped strings in the tree or in the model-visible journal (entropy + known prefixes: sk-, ghp_, xai-, Bearer ). Vault references by handle are allowed in kernel records, not in the pass. | Principal-supplied vault handles. |

> **Demoted from 0.3 — not ship-blocking in 0.4** (open)
>
> SLOP_DUP (clone-with-drift) and SLOP_LIE (comment contradicts code) need NLI or noisy clone detection. They stay in the Produce prefix as doctrine D3/D10. They do not flip ship. Packet later: countable dup (normalized AST equality ≥ N tokens, two homes, both in the delta). SLOP_LIE alternative that is mechanical: “no comments in shipped code unless constraints asked for docs” — not first ship.

A shipment fails if any ship-blocking gate is red, even when every oracle is green. Repair, or REPAIR_EXHAUSTED.

---

## 9. Context

*locked — Kernel law. Compile what goes in. Virtualize what stays out. Not a skill.*

Context is kernel law. Skill-shaped (a compiled working set) and not a skill. It cannot be unloaded, skipped, or left to Produce to remember. A station pass without a fresh context compile is refused. There is no “run produce naked.” Reusing the previous pass’s working set is refused.

Token savings come from both jobs. A perfect working set that then swallows 9 MB of test stdout is still a flooded window.

| Slice | Why | Shape |
| --- | --- | --- |
| Spec slice for this grant | Purpose, constraints, done_when, never_do for this job. | Stable prefix. Prompt-cache it. |
| Doctrine | Factory law. Always. Pinned hash. | Stable prefix. Prompt-cache it. |
| Product truth | The files this grant will touch, as they are. | Full text of named files only. |
| Structural map | Where those files sit. | tree-sitter outline + import/call neighbors, ranked, budgeted in map_tokens. Must include imported neighbors of granted files or compile fails. Not the repo. |
| Evidence so far | What passed, what failed, last fail reason. | Structured records, not log blobs. |
| Work-order grant | Touches, budget left, repair cycle. | Small. Exact. |

| Virtualize | Meaning |
| --- | --- |
| Sandbox the dump | Kernel executes the tool. Raw stdout/stderr/page/snapshot never enters the model-visible pass. |
| Summary + handle | Pass gets a compact result (counts, fail names, hashes, first stack) plus a store handle. |
| On-demand fetch | Produce may pull a slice by handle + query. Cap: budgets.fetch_bytes_per_pass (default 32768). Exceeding it is a refused effect, not a bigger window. |
| Think in code | A grant whose job is count/search/index may not load matching file bodies into the pass. Kernel runs a program, returns the print. Violation → refused pass, no files written. |
| Event index | File edits, fails, decisions, exceptions live in the journal. Resume reads that, not a transcript. |

**9.1 Raw body refuse.** A tool effect whose raw body would enter the pass is refused. The kernel stores it and returns summary + handle.

**9.2 Fresh compile.** Every Produce (and Repair) pass gets a new compile. Context traces are pointers, not dumped windows.

**9.3 Map miss is a failed compile.** A map that stays in budget by dropping the neighbor a granted file imports is a failed context compile, not a passing budget proof.

**9.4 Unfit port.** If a coder port cannot accept a context compile, or cannot live without raw tool bodies, that port is unfit. Codex CLI / Claude Code / Cursor unwrapped are unfit.

**9.5 Always on.** Context compile and virtualize are internal journaled effects. Always on, including repair and crash resume.

> **Killed as factory identity** (refuse)
>
> Shipping mksglu/context-mode as the kernel (bolt-on for 17 clients; we are not those clients). MCP + hooks as the door (hooks fail open). BM25 over blobs as evidence. 3-hour chat + PreCompact. Unstructured leftovers may sit behind an FTS port; the kernel still refuses raw dumps.

---

## 10. Effect algebra

*locked — Stations propose. Kernel executes. Default deny. No unnamed side effects.*

Without a closed effect list the admission door is a comment. First ship has these effects and no others. Unknown effect type → refuse, journal, no execution.

| Effect | Payload | Who proposes | Kernel does |
| --- | --- | --- | --- |
| write | path (relative), content (bytes), mode? | Produce | Admit path∈grant. Atomic: write temp in sandbox, fsync, rename. Journal content hash, not body in the pass. |
| delete | path | Produce | Admit path∈grant and path∈delta or path was created this work order. Baseline deletes need the spec to say so (in_scope). |
| rename | from, to | Produce | Both paths ∈ grant. |
| run | argv[], cwd=product, timeout_s, network=false | Produce only if the grant.allow_run is true. Verify always, for oracles. | Sandbox. No vault, no journal, no kernel paths. Network deny unless an egress grant names host+purpose. |
| model_call | role=produce, adapter, prompt_handle, budget | Kernel only | Fail closed if unbound. Tokens never enter the journal body. |
| fetch_handle | handle, query, max_bytes | Produce | Slice from the store, ≤ remaining fetch budget this pass. |
| raise_exception | code from the closed list, detail | Produce or kernel | Halt the line. Page the principal. |
| grant_expand | path | Produce | Kernel decides per §12. Produce never writes outside the current grant on its own. |

> **Egress** (lock)
>
> Default deny. First SKU has no egress grants. A later SKU may name host + purpose on the work order. Produce curl|bash on the host is a kernel bug, not a station feature.

External effects (anything that leaves the product tree or the sandbox) need compensate + reconcile. Uncertain never blind-retries — UNCERTAIN_EFFECT. First SKU’s only external effect is model_call (vendor) and the shipment tarball write (local, kernel).

---

## 11. Product sandbox

*locked — Product tests are untrusted code. Workspace ≠ kernel. Vault unreadable. Network deny.*

done_when: cargo test means the factory runs code Produce just wrote. That is RCE on the host unless the product workspace is isolated.

**11.1 Two trees.** Kernel tree (binary, journal, vault, spec store, doctrine). Product tree (the shipment). Produce effects may only name paths under the product tree.

**11.2 Isolation.** Verify and granted run execute in a sandbox (landlock / bubblewrap / equivalent packet). No read of vault, journal, kernel, or other work orders. No write outside the product tree.

**11.3 Network deny.** Default. First SKU: always. A test that opens a socket fails the run (sandbox kill), not the factory.

**11.4 No host package install.** Toolchain is the factory image. Product may vendor or use the granted language’s local deps inside the sandbox. apt/yum/curl|sh on the host is refused.

**11.5 Secret leak is a factory fail.** If a product test can read the vault, P22 fails and the factory is broken. SLOP_SECRET on the tree is necessary and not sufficient.

> **Packet: which isolator** (note)
>
> landlock + seccomp, bubblewrap, or firecracker are packets. The law is the capability cut, not the vendor. First ship picks the cheapest that enforces 11.1–11.4 on Linux.

---

## 12. Kernel vs stations

*locked — Seven chat personas are forbidden. Produce is the only required model worker.*

Rev 0.3 listed Admit, Compile, Context, Produce, Verify, Repair, Ship as stations. That recreates a firm of personas. 0.4 splits kernel programs from untrusted workers.

| Kernel program | Input | Output | Model? |
| --- | --- | --- | --- |
| admit | spec bytes | accepted spec + hash, or exception | No. Schema + unknown-key + contradiction scan + typed-oracle check. |
| compile_work_order | accepted spec + baseline tree + doctrine_hash | work order: grants[], oracles[], budgets, evidence plan | Optional bounded model with schema-validated DAG. Invalid graph → refuse, retry once, then SPEC_INCOMPLETE. First SKU: one grant covering the product tree, no model required. |
| compile_context | grant + product + evidence + doctrine | working set attached to the next pass | No. Deterministic packer. |
| door | proposed effect + grant + spec + doctrine + budget + egress | admit or refuse | No. |
| execute | admitted effect | journal record + new product state | No. |
| verify | work-order oracles + gates + product tree | evidence pack (pass/fail bits) | No. |
| ship | green evidence + product tree | tarball + evidence + journal slice | No. |
| kill / raise / bind / serve | CLI | journaled state change | No. |

| Station | Grant | Done |
| --- | --- | --- |
| Produce | Write product files under grant, inside a fresh context, propose effects only. | Proposed effect list + self-check notes. Not “done.” Not ship. |
| Repair | Same as Produce. Remaining repair_cycles. Fail records in context. | New proposal. Not a second soul. |

**12.1 First SKU compile is trivial.** One grant: product tree glob, all oracles, full remaining budget. No hidden planner. Brownfield multi-grant DAGs are a later packet.

**12.2 GRANT_INSUFFICIENT.** Produce proposes grant_expand. Kernel auto-expands only if the path is an imported neighbor of a granted file already in the structural map, and the budget holds. Else: if the path is required to satisfy an oracle, raise SPEC_INCOMPLETE (the spec did not name enough). If not required, refuse the expand, continue.

**12.3 No silent widen.** Produce writing outside the grant is a refused effect. P26.

**12.4 Verify is not Produce.** If Verify needs a model, stop. You are building a second chat agent.

---

## 13. Produce port protocol

*locked — The worker binary is a packet. The protocol is constitution. Unwrapped Codex is unfit.*

Coder implementation is a packet. The interface is not. If first ship wraps a CLI that dumps tool output into the model window, P13 fails by construction.


*One-grant-one-pass. Kernel → worker.*

```json
{
  "pass_id": "wo_…/g_…/p_…",
  "role": "produce" | "repair",
  "prefix_cache_keys": ["doctrine:<hash>", "spec_slice:<hash>"],
  "doctrine": { "hash": "…", "text": "…" },
  "spec_slice": { "purpose": "…", "in_scope": [], "never_do": [], "oracles": [] },
  "grant": { "id": "g1", "paths": ["**"], "allow_run": false, "repair_left": 3 },
  "product_truth": [{ "path": "src/main.rs", "bytes": "…" }],
  "structural_map": "…budgeted outline…",
  "evidence": [{ "oracle_id": "unit", "pass": false, "reason": "exit 1, 3 failed" }],
  "handles": [{ "id": "h_…", "summary": "cargo test: 3 failed, names: …" }],
  "budgets": { "model_calls_left": 12, "fetch_bytes_left": 32768 }
}
```


*Worker → kernel. Effects only. No “please run this and paste stdout.”*

```json
{
  "pass_id": "wo_…/g_…/p_…",
  "effects": [
    { "type": "write", "path": "src/main.rs", "content": "…" },
    { "type": "fetch_handle", "handle": "h_…", "query": "first panic", "max_bytes": 2048 }
  ],
  "self_check": { "notes": "health flag added; unit oracle should pass" }
}
```

**13.1 Kernel owns tools.** The worker does not exec, read the repo, or call the model vendor. It receives a compiled pass and returns effects. The kernel runs model_call, run, write.

**13.2 If the worker must see a dump.** It asks fetch_handle. The kernel returns a capped slice. The rest stays in the store.

**13.3 Unfit.** A port that cannot accept this message shape, or that injects raw tool bodies into its own window, is unfit. Do not wrap it “for first ship.”

---

## 14. Operating loop

*locked — One line. Sequential. Repeat until ship or exception. Defaults if budgets omitted.*

1. Admit spec. Schema, unknown keys, waiver keys, typed oracles, contradiction, factory never_do. If not → exception, no code written.
2. Pin doctrine_hash. Compile work order (first SKU: one grant). Snapshot baseline tree hash. Allocate budgets (spec or defaults).
3. Compile context for the next Produce pass. Always. Fresh.
4. Produce. Worker returns effects. Door admits or refuses each. Kernel executes admitted effects atomically.
5. Verify. Run oracles + slop gates in the sandbox. Write evidence pack.
6. If green → Ship (directory + tarball + evidence + journal slice).
7. If red and repair_cycles left → Repair (recompile context with fail records, same door).
8. If red and repair_cycles exhausted → REPAIR_EXHAUSTED. Partial tree remains. ship returns it marked failed. No silent done.

| Budget | Default if omitted | Counts |
| --- | --- | --- |
| repair_cycles | 3 | Verify fails that trigger another Produce. |
| wall_clock_s | 3600 | Admit → terminal. Kernel clock. |
| model_calls | 40 | Kernel model_call effects. Admit/compile on first SKU cost 0. |
| fetch_bytes_per_pass | 32768 | Sum of fetch_handle bytes in one pass. |
| map_tokens | 2000 | Structural map packer budget. |

Subscriptions are quota, not USD. “Money” is not a first-ship unit. Adapters that report remaining quota may expose it on status. Hitting 0 is BUDGET_EXCEEDED (or unbound if the vendor says so).

> **Crash recovery is not an exception** (lock)
>
> Resume from the work-order journal: last admitted effect is the checkpoint. In-flight write is atomic (temp + rename) so resume never sees a half file. Context is recompiled. Journal is for recovery and audit, not bit-identical replay of Produce.

---

## 15. Exception policy

*locked — Closed list. Anything not on it is factory work. GRANT_INSUFFICIENT maps here.*

| Code | When | Human job |
| --- | --- | --- |
| SPEC_INCOMPLETE | Spec lacks a typed done_when item, constraint, or fact the factory cannot invent. Includes GRANT_INSUFFICIENT when an oracle cannot be met inside the grant + legal auto-expand. | Finish the spec. |
| SPEC_CONTRADICTION | Two requirements cannot be true together, the spec requires what doctrine forbids, or a waiver key is present. | Resolve. |
| MISSING_AUTHORITY | Credential, license, deploy right, or payment the factory cannot mint. Includes clone-from-remote and image push on first SKU. | Grant or refuse. |
| UNCERTAIN_EFFECT | External effect cannot be reconciled; never blind-retry. | Judge or authorize a reconcile path. |
| NEVER_DO | Proposed work hits spec never_do or factory welded never_do, and no remaining path satisfies the oracles. | Confirm kill or rewrite spec. |
| BUDGET_EXCEEDED | repair_cycles, wall_clock_s, or model_calls ceiling hit. | Raise, cut scope, or kill. |
| REPAIR_EXHAUSTED | Verify still red after repair_cycles. | Rewrite spec, raise budget, or kill. |
| KILL | Principal stops the line. | Stop. Residual state journaled. |

> **NEVER_DO is not HIL on every rejected thought** (note)
>
> A refused effect that is not required to satisfy an oracle is journaled and the line continues. Raise NEVER_DO only when every remaining path hits the predicate. P8.

Not exceptions (killed as operating mode): ordinary code review / LGTM; plan approval before every pass; style nits the spec did not name and doctrine does not gate; model doubt that an oracle or gate can resolve; asking permission to run tests, open a branch, or write files the work order already grants; crash recovery; choosing among equivalent implementations the spec does not care about and doctrine already ranked; “does this look like slop?” as a human question.

Uncertain is never retried blind. Repair is not a loop that pages a human every cycle.

---

## 16. Welded never_do

*locked — Factory-level hard stops, independent of the product spec. Dual-use is not unsaid.*

Spec never_do is product law. Factory never_do is plant law. Both apply. The principal cannot waive factory never_do.

* Read or write vault, journal, kernel, or other work orders from the product sandbox.
* Network from the product sandbox unless an egress grant names the host (first SKU: never).
* Effects whose paths escape the product tree.
* Disable, skip, or shadow doctrine gates.
* Put access tokens, refresh tokens, or API keys in the product tree, the model-visible pass, CLI stdout, or the evidence pack.
* Open a browser on the server.
* Scrape a vendor login.
* Mint credentials.

> **Dual-use** (lock)
>
> The factory will build what a complete spec names, including software the principal should not want, unless a factory never_do detector matches. First ship detectors are the list above plus SLOP_SECRET. Broader malware classifiers are a packet. The principal is the ethicist for product purpose. The factory is the ethicist for the plant’s own hide.

---

## 17. Model adapters

*first-ship — Same door, same vault, fail closed. First ship is grok + codex. glm waits for a real device-code grant.*

Thinking passes go out through a model-call port. Stations name a role (produce), not a brand. Admin binds which adapter fills the role.

| Adapter | First ship | Bind | Notes |
| --- | --- | --- | --- |
| grok | Yes | OAuth 2.0 device authorization / vendor machine-code. Headless poll. | xAI Grok subscription. Device-code is real (accounts.x.ai / grok login --device-auth). URLs and client ids are packet data. |
| codex | Yes | Same grant type. | OpenAI Codex / ChatGPT subscription device-code is real. Binding it from a third-party plant is a ToS kill risk. Treat vendor refuse as unbind + MISSING_AUTHORITY, not a scrape fallback. |
| glm | No | Unfit until a device/machine-code subscription bind exists. | GLM Coding Plan is documented as API key + browser “Continue with Z.ai.” That is killed by this constitution. Do not add a key flag to unblock it. |

**17.1 Device-code only for named adapters.** Operator completes the code on another device. Access + refresh land in the vault only. Adapter refreshes before expiry without a new device-code.

**17.2 Refresh fail.** Unbound, fail closed, audit. No silent spend on a dead token. Produce does not start.

**17.3 Rotate.** New device-code. In-flight model_call settles. New token active. Old secret wiped.

**17.4 Hygiene.** Tokens never enter the model-visible journal, CLI output, evidence pack, argv, or process lists. CLI never takes a raw access token, refresh token, or API key as a flag.

**17.5 Unbound refuse.** Produce with no bound adapter for the role is refused. No model_call. No files written. P18.

Killed: pasting a subscription cookie or session; browser/scraped login on the server; raw Codex App Server as a product dependency; API keys in serve flags, env files in the factory tree, or chat; field/stations picking models or keys; a first-ship adapter that cannot bind headless; wrapping Codex CLI as the produce worker.

> **Later packet** (open)
>
> A metered-key adapter may exist behind the same port for private/OpenAI-compatible endpoints. It is not how grok or codex bind, and it is not first ship. glm joins the locked name list when the vendor grant exists.

---

## 18. Secrets vault

*locked — Adapter tokens and principal-supplied product secrets. Never in the pass.*

**18.1 Two classes.** Adapter secrets (bind). Product secrets (principal grant, named, for a later SKU’s runtime). First SKU has no product secrets.

**18.2 Injection.** Kernel may inject a product secret into a sandboxed run as an env handle only if the work order names it. The value never enters context compile, journal bodies, or evidence.

**18.3 Handles in the pass.** The pass may see secret:<name> exists. It may not see the bytes.

---

## 19. Runtime and CLI

*locked — Headless serve. Unix socket. CLI on the box. Remote = SSH. No first-ship web UI.*

The factory runs on a remote headless server. There is no local interactive desktop as the runtime. The operator surface is a CLI. Chrome, if it ever earns a place, is a client of the same commands.

> **Transport** (lock)
>
> serve binds a Unix socket (default $XDG_RUNTIME_DIR/darkfactory.sock or /var/run/darkfactory/factory.sock). CLI talks to that socket. Principal is the connecting uid. Remote access is SSH to the box, then the CLI. First ship has no network API, no TLS service, no browser. A second serve process fails on the instance flock.

| Command | Who | Does |
| --- | --- | --- |
| serve | ops | Start the instance. No display. No browser. Takes the flock. Journal dir as flag (path), never a token. |
| bind <grok|codex> | admin | Device-code start + poll. Prints user_code and verification_uri. Operator finishes on another device. No token on stdout. |
| unbind <adapter> | admin | Drop the vault secret. In-flight model_call settles. Fail closed after. |
| rotate <adapter> | admin | New device-code. Old token retiring, then wiped. |
| status | principal / admin | Line state, adapter bind (yes/no, never secret), budget remaining, current work order, open exceptions. |
| admit <spec> | principal | Submit a spec file. Starts the line or raises. |
| kill | principal | Stop. In-flight writes finish atomically or roll back. Not-started effects never start. Journal killed. |
| exceptions | principal | List open exceptions. |
| exception <id> <answer> | principal | Answer one. Resume or stay halted per the answer schema (packet: grant | refuse | patch-spec). |
| ship | principal | Retrieve the last shipment (product + evidence). Failed partials are marked failed, still retrievable. |
| journal [--tail] [--pass <id>] | principal / admin | Append-only log. No secrets. |
| evidence | principal | Current evidence pack without shipping. |
| grant | principal | Current grant: paths, repair left, oracles. |
| context show <pass-id> | principal / admin | The compiled working set that fed that pass (the actual prefix, not a recap). Operator window, not HIL. |

Headless law: serve does not open a browser. bind does not open a browser on the server. The operator’s phone or laptop opens verification_uri. The server only polls.

Second admit while a line is live is refused (not queued). Queueing is a later packet.

---

## 20. Journal and work order

*locked — Append-only. Resume, replay-of-kernel, audit. Produce is not replay-identical.*


*Work order (frozen at admit).*

```json
{
  "id": "wo_…",
  "spec_hash": "sha256:…",
  "doctrine_hash": "sha256:…",
  "baseline_tree_hash": "sha256:…",
  "sku": "first",
  "grants": [
    { "id": "g1", "paths": ["**"], "oracle_ids": ["unit", "binary", "entry", "no_todos"], "allow_run": false }
  ],
  "oracles": ["/* copy of spec done_when */"],
  "budgets": { "repair_cycles": 3, "wall_clock_s": 3600, "model_calls": 40, "fetch_bytes_per_pass": 32768, "map_tokens": 2000 },
  "state": "admitted | producing | verifying | repairing | shipping | shipped | exception | killed"
}
```

Journal records, in order, at least: admit (spec_hash), doctrine pin, work-order compile, context compile (pointer + hashes, not the window), proposed effect, door decision, execute (content hash), verify record, exception, kill, ship. Context traces are pointers into the compile store.

Kernel sequencing (the loop in §14) is a deterministic state machine and can replay. Produce outputs cannot. Do not steal Temporal activity replay for the worker.

---

## 21. Product contract

*locked — The factory returns a shipment, not a chat. Failed partials are marked failed.*

* Product tree (the workspace).
* Tarball of that tree (stable mtime epoch, sorted, hashed).
* Evidence pack: each oracle id pass/fail + hashes; each doctrine gate pass/fail; overall bit.
* Work-order journal slice for this wo_id.
* Context traces: compile pointers per pass.
* Exception log (empty on a clean ship).

“Correctly” means every oracle is green and every ship-blocking doctrine gate is green. Not that a model said it looks right. ship on a red evidence pack still returns the partial, with overall=fail. Callers must read the bit.

---

## 22. Welded kernel

*locked — Load-bearing only. Flesh unloads clean. First ship is this list plus one Produce worker.*

1. Spec store — versioned, principal-writable, station-read-only.
2. Doctrine — factory law. Versioned with the factory. Pinned on the work order.
3. Context compile — fresh working set before every Produce pass.
4. Work-order journal — append-only. Resume, audit.
5. Admission door — spec + doctrine + work order + budget + egress + sandbox.
6. Effect executor — atomic writes, sandboxed run, model_call.
7. Station dispatch — one grant, Produce cannot widen spec/budget/doctrine.
8. Evidence store — oracles + gates. Only path to done.
9. Exception raise — closed list.
10. Kill — principal override. In-flight settle. Not-started never start.
11. Budget ceiling — halt with partial shipment. No silent spend multipliers.
12. Secrets vault — credentials never enter the model-visible journal.
13. Model-call port — grok / codex behind one door. Device-code. Unbound fails closed.
14. Product sandbox — tree isolation, network deny, vault unreadable.
15. CLI — Unix socket. The only first-ship operator surface. Headless.
16. Instance lock — one serve, one line.

Flesh (harness, coder worker binary, FTS, tree-sitter vendor, later UI, later SKUs) mounts behind ports and must unload clean.

> **First ship** (lock)
>
> Kernel + CLI + context compile + doctrine gates + device-code bind for grok and codex + produce port + one Produce worker + sandbox + typed-oracle verify. Not seven model stations. Not glm. Not a web UI.

---

## 23. First proofs

*locked — Proofs prove the line is dark and that slop cannot ship. P1 is bounded by the first SKU.*

A demo that pages a human to “approve the plan” or “does this look clean?” fails the product. Proofs run against the first SKU unless noted.

| Proof | Must show |
| --- | --- |
| P1 Clean ship | First-SKU spec → shipment, zero HIL, every oracle green, every ship-blocking gate green. |
| P2 Incomplete spec | Missing or prose-only done_when → SPEC_INCOMPLETE, no code written. |
| P3 Contradiction | Two impossible constraints, or a waiver key → SPEC_CONTRADICTION, no ship. |
| P4 Verify fail + repair | First Produce fails evidence, Repair passes, still zero HIL. |
| P5 Repair exhausted | Persistent fail → REPAIR_EXHAUSTED, partial journal, ship overall=fail, no silent done. |
| P6 Kill | Principal kill mid-Produce: not-started effects never start; in-flight write is atomic; no further effects. |
| P7 Crash | Kill the Produce worker mid-job; resume ships without HIL; context recompiled. |
| P8 Never-do | Produce proposes a forbidden effect; door refuses; line continues unless every remaining path is blocked, then NEVER_DO. No HIL on a discarded thought. |
| P9 Naked produce | Produce without a fresh context compile is refused. No files written. (Covers stale reuse.) |
| P10 Slop ship | A change that meets a naive oracle but trips a slop gate does not ship; Repair or REPAIR_EXHAUSTED. |
| P11 Doctrine waiver | A spec field that tries to skip doctrine is refused at admit. |
| P13 Raw dump | A tool that returns a large body never puts that body in the pass; summary + handle only; fetch-by-handle still works and respects the byte cap. |
| P14 Think-in-code | A count/search job is done by a program that prints the answer, not by loading the files into the pass. Violation refuses the pass. |
| P15 Map budget | Structural map stays inside map_tokens and still names the imported neighbor the grant needs. Dropping that neighbor fails compile. |
| P16 Headless serve | serve starts on a box with no display. No browser opened. Instance flock holds. |
| P17 Device-code bind | bind grok and bind codex print user_code + verification_uri; poll → vault; no token on stdout. |
| P18 Unbound refuse | Produce with unbound adapters is refused. No model_call. No files written. |
| P19 Token hygiene | Vault secret never appears in journal, CLI output, evidence, or process argv. |
| P20 Rotate | Re-bind wipes the old secret; in-flight settles; new calls use the new token. |
| P21 Oracle independence | Produce-written tests that pass while a work-order oracle fails → no ship. |
| P22 Sandbox | A product test that tries to read the vault / journal / network is denied. Factory still live. Secret not in pass or evidence. |
| P23 Sequential instance | Second serve or second admit while a line is live → refused. |
| P24 Typed admit | Prose-only done_when → SPEC_INCOMPLETE. |
| P25 Delta slop | Baseline TODO does not fail a feature-add; a new TODO does. |
| P26 Grant widen | Produce proposes a path outside the grant that is not a legal auto-expand → door refuse, no file write. |

P9 subsumes 0.3’s P12 (stale context). Bind hygiene remains three proofs because they fail for different reasons (print, leak, rotate).

---

## 24. Examples

*locked — One admissible spec. The rejects that 0.3 would have argued about.*


*Admissible — first SKU. A tiny CLI that prints a health line and adds two numbers.*

```yaml
spec_version: "1.0"
purpose: >
  A command-line calculator that adds two integers and exposes a
  --health flag for the factory probe.
principal:
  id: "uid:1000"
in_scope:
  - "Rust binary named add"
  - "add <a> <b> prints the decimal sum on stdout and exits 0"
  - "--health prints ok and exits 0"
out_scope:
  - "GUI, network, persistence, other operations"
never_do:
  - "network calls"
  - "write files outside the product tree"
done_when:
  - id: unit
    kind: command
    run: cargo test --offline
    expect: { exit: 0, timeout_s: 180 }
  - id: add
    kind: probe
    build: cargo build --release --offline
    run: ./target/release/add 2 3
    expect: { exit: 0, stdout_contains: "5" }
  - id: health
    kind: probe
    build: cargo build --release --offline
    run: ./target/release/add --health
    expect: { exit: 0, stdout_contains: "ok" }
  - id: no_residue
    kind: not_present
    pattern: "TODO|FIXME|placeholder|lorem|example\.com"
    in: delta
constraints:
  language: rust
  license: "Apache-2.0 OR MIT"
budgets:
  repair_cycles: 3
  wall_clock_s: 1800
  model_calls: 20
```


*Reject — SPEC_INCOMPLETE. Prose-only done_when.*

```yaml
spec_version: "1.0"
purpose: "A calculator."
principal: { id: "uid:1000" }
in_scope: ["calculator"]
out_scope: []
never_do: []
done_when:
  - "it works"
constraints: { language: rust, license: MIT }
```


*Reject — SPEC_CONTRADICTION. Waiver key.*

```yaml
spec_version: "1.0"
purpose: "A calculator."
principal: { id: "uid:1000" }
in_scope: ["calculator"]
out_scope: []
never_do: []
done_when:
  - id: unit
    kind: command
    run: cargo test --offline
    expect: { exit: 0 }
constraints: { language: rust, license: MIT }
skip_doctrine: true
```


*Reject — SPEC_CONTRADICTION. Spec requires slop doctrine forbids.*

```yaml
spec_version: "1.0"
purpose: "A calculator."
principal: { id: "uid:1000" }
in_scope:
  - "leave TODO comments for the next team"
  - "add an unused utils module just in case"
out_scope: []
never_do: []
done_when:
  - id: unit
    kind: command
    run: cargo test --offline
    expect: { exit: 0 }
constraints: { language: rust, license: MIT }
```

---

## 25. Locked vs open

*open — If a sentence cannot become a check or a refused effect, it is not factory law.*

| Locked in 0.4 | Still a packet |
| --- | --- |
| Typed spec schema, unknown-key refuse, waiver-key refuse | Exact YAML parser / JSON twin |
| Oracle kinds: command, probe, file, not_present, hash | More kinds (http, screenshot) with later SKUs |
| Effect algebra and default-deny egress | Additional effect types |
| Product sandbox capability cut | Which isolator (landlock, bwrap, firecracker) |
| Produce is the only required model station; Verify is a program | Compile-graph as a bounded model for brownfield DAGs |
| Deterministic ship-blocking gates listed in §8 | SLOP_DUP detector; comment-NLI |
| Produce port protocol | Other worker binaries after the in-process Go worker in PACKET_1.md |
| First SKU + sequential instance + Unix-socket CLI + tarball | Git push, image, HTTP service SKU, queueing |
| grok + codex device-code bind | Vendor URLs and client ids; glm when the grant exists; metered-key port for private endpoints |
| Doctrine pin, delta slop, default budgets, kill atomicity, fetch cap, think-in-code law | FTS implementation; tree-sitter library vendor |
| Factory welded never_do | Broader malware classifiers |
| Kernel vs station split | Whether a later Magnus instance hosts this factory as a domain |

> **Do not leave these “open” again** (refuse)
>
> Coder protocol, Verify being a model, sandbox, oracle ownership, glm as a locked first adapter, unbounded P1, free-text done_when, unnamed effects.

---

## 26. Packet 1

*first-ship — Locked in PACKET_1.md. Not a punch list. Not deferred.*

Packet 1 is [PACKET_1.md](./PACKET_1.md). It names Go, the tree, the instance layout, the schemas under `schema/`, the example specs under `examples/`, the door, the proof harness, and the build order.

Packet 1 turns green: **P1–P6, P9, P11, P16–P19, P21, P23, P24, P26** against `examples/add.yaml`.

Packet 2 (not this rev): P7, P8 remaining-path, P10, P13–P15, P20, P22, P25.

> **What not to do in packet 1** (note)
>
> Do not add a web UI, plan card, or “does this look clean?” Do not import Magnus, Temporal, alphavector, or context-mode as the OS. Do not wrap Cursor / Claude Code / Codex CLI as the kernel. Do not add metered API keys for grok/codex to unblock. Do not add more stations. Do not put a model in Verify. Do not expand the exception list to get P4 to pass.

---

## 27. Changelog from 0.3

*locked — Intent preserved. Slogans replaced with schemas. A few sentences deleted because they were dead letter.*

| 0.3 | 0.4 |
| --- | --- |
| “Best product that spec allows” | Smallest complete product. Size is gates, not a bakeoff. |
| Free-text done_when | Closed oracle kinds. Unknown kind → SPEC_INCOMPLETE. |
| Produce writes product; Verify runs tests | Work-order oracles authored at admit. Produce cannot certify itself. |
| Seven stations including Admit/Context/Verify as workers | Kernel programs + Produce. Repair is Produce with fail records. |
| “Immediate” kill | In-flight writes atomic or rolled back; not-started never start. |
| SLOP_LIE, SLOP_DUP ship-blocking | Demoted to Produce-prefix taste until a program exists. |
| Gates on “shipped files” | Gates on work-order delta vs baseline. P25. |
| glm locked as first adapter | Unfit until device-code exists. grok + codex only. |
| Coder implementation fully open | Protocol locked. Binary is a packet. Unwrapped IDE agents unfit. |
| Unbounded P1 | First SKU. Sequential instance. Tarball shipment. |
| CLI without transport | Unix socket, uid principal, SSH for remote. journal / evidence / grant / context show. |
| Improve station, one sentence | Deleted. Spec patches are a new admit. |
| Pick the smaller of two shapes | Deleted. Produce emits one candidate. |
| Money budget | Quota / model_calls / wall_clock. Subscriptions are not USD. |
| Context fetch unbounded | fetch_bytes_per_pass cap. |
| Think-in-code as a proof only | Law: violation refuses the pass. |
| Dual-use unsaid | Welded never_do. Principal owns product purpose; factory owns the plant’s hide. |

Unchanged on purpose: closed HIL list; spec cannot waive doctrine; doctrine cannot invent product; context is kernel law; device-code; no pasted keys; no server-side browser; crash recovery is not HIL; no first-ship web UI; no Cursor; no context-mode-as-OS; evidence owns truth.
