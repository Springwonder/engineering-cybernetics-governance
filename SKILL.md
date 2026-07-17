---
name: engineering-cybernetics-governance
description: Use Qian Xuesen's Engineering Cybernetics as the primary framework for turning work evidence into stable memory, reusable Skills, experiments, and daily feedback control. Use for end-of-day reviews, experience distillation, system improvement, and deciding what belongs in memory versus Skills.
version: 1.0.0
created_by: agent
platforms: [windows, linux, macos]
metadata:
  hermes:
    tags: [control-theory, feedback, skills, memory, daily-review, qian-xuesen]
---

# Engineering Cybernetics Governance

Use this as a practical translation of Qian Xuesen's *Engineering Cybernetics*, not as a claim that an AI workflow is literally a physical control system.

## Authority and evidence levels

Use this order:

1. Qian Xuesen, *Engineering Cybernetics* (McGraw-Hill, 1954); Chinese New Century edition (Shanghai Jiao Tong University Press, 2007).
2. Direct execution evidence: tool output, tests, logs, user corrections, repeated outcomes.
3. Maintained Hermes documentation and source code.
4. Modern control/system literature.
5. Analogy or hypothesis — label it explicitly and test it before promotion.

Do not attribute modern terms such as Agent Skills, LLM memory, observability, or software CI directly to Qian. They are modern mappings.

### Historical boundary

Do not claim that the 1954 book already contained today's complete theories of controllability, observability, system identification, optimal control, or fault-tolerant control.

- The book directly treats input/output behavior, feedback, multivariable and noninteracting control, delay, random inputs, automatic optimization, adaptation, and error control.
- Kalman's formal controllability/observability theory appeared in 1959 and later.
- Mature system-identification and fault-tolerant-control terminology developed later.
- In this Skill, “observable” means operationally evidenced by logs/tests/artifacts, and “controllable” means Hermes has a real action path and permission. These are modern engineering checks, not claims about Qian's original vocabulary.

## Controlled-system card

Before changing the system, define:

```text
Purpose / reference r: desired outcome and acceptance criterion
Plant P: process or workflow being influenced
State x: minimum variables needed to describe its condition
Observation y: measurable evidence (tests, logs, feedback, artifacts)
Control u: action we can actually take
Disturbance d: external change, uncertainty, noise, model drift
Constraints C: privacy, safety, cost, time, reversibility
Loss J: error + cost + risk + complexity
Sampling/review interval: when feedback is observed
Stop/rollback condition: when intervention must halt
```

If the outcome cannot be observed or the proposed intervention cannot influence it, do not pretend control exists. First add measurement, run a bounded experiment, or leave it as an open question.

## Daily closed-loop workflow

### 1. Observe — collect evidence, not narrative

Collect only evidence from the day:

- artifacts created or changed;
- commands/tests and actual outcomes;
- user corrections and explicit feedback;
- failures, retries, rollback events;
- recurring friction;
- cost, latency, safety or privacy signals.

Do not infer success from a plan or a plausible response.

### 2. Identify — update the model

For each meaningful event, record:

- expected output;
- actual output;
- error/deviation;
- likely disturbance;
- whether the current workflow model was wrong or incomplete;
- confidence and evidence source.

One event is a sample, not a law. Separate noise from repeatable structure.

Track candidate evidence with: observation count, independent task count, successes, counterexamples, applicable conditions, likely confounders, and confidence.

Promotion heuristic (not a rigid law):

- one observation → daily log only;
- two similar observations → candidate;
- repeated independent reproduction, or one high-cost incident with a clear mechanism → update/create a Skill;
- cross-task long-term stability plus user confirmation → consider core memory.

High-impact safety facts and explicit durable user decisions may be promoted immediately when the mechanism/scope is clear; do not wait for repeated harm.

### 3. Classify the learning

Route each candidate to exactly one primary store:

#### Core memory / Hindsight — only stable bottom-layer logic

Admit only when all are true:

- cross-task and likely useful months later;
- declarative, compact, and not a step-by-step procedure;
- supported by repeated evidence, an explicit durable user decision, or a high-authority source;
- reduces future steering or prevents a serious repeated failure;
- does not duplicate an existing memory;
- includes scope/conditions when not universal.

Examples: durable preferences, stable environment facts, invariant safety boundaries, validated decision principles.

#### Skill — reusable control policy or procedure

Use for:

- triggers and applicability conditions;
- ordered actions or commands;
- expected observations and thresholds;
- failure branches, rollback and verification;
- known disturbances and platform pitfalls;
- evidence/citations and version assumptions.

A Skill is a controller/policy, not a diary.

#### Daily log / Obsidian — state trajectory and evidence

Use for one-day facts, outputs, decisions, unresolved items, measurements, and links to artifacts.

#### Session history — raw conversation

Do not duplicate the transcript into memory or Skills.

#### Experiment backlog — unverified hypothesis

A one-off workaround, guess, or attractive idea remains an experiment until repeated or tested.

### 4. Synthesize or update Skills

Do not create one Skill per incident. Prefer updating the narrowest existing Skill.

A valid Skill must contain:

```text
Trigger
Goal / controlled variable
Inputs and prerequisites
Procedure / control action
Observable feedback
Success threshold
Disturbances and failure branches
Safety constraints
Rollback / stop condition
Verification
Evidence / version
```

Skill changes require evidence. If today's evidence contradicts an old Skill, preserve the reason for the change. Do not erase historical rationale silently.

### 5. Stability and coupling check

Before adopting a change, ask:

- Could it create oscillation (frequent back-and-forth rule changes)?
- Is feedback delayed, sparse, or noisy?
- Does optimizing one metric damage another subsystem?
- Is the intervention too large for the evidence?
- Can it be rolled back?
- Does it increase hidden coupling between profiles, machines, channels, or credentials?

Prefer small reversible adjustments. Do not tune several coupled variables at once unless effects can be isolated.

### 6. Close the loop

The daily report must state:

```text
Target
Observed state
Deviation
Disturbance / uncertainty
Control action actually taken
Verification result
Residual error / open loop
Memory candidates (normally none)
Skills created/updated (normally few)
Tomorrow's observation point
```

If there is no validated reusable learning, create no Skill and write no memory. Silence is better than knowledge pollution.

## Candidate-tool intake loop

Use this when the user brings a new repository, framework, plugin, memory system, or “toy.” Curiosity is a valuable source of candidate inputs; evaluate the tool without shaming the user or treating exploration itself as recklessness.

1. **Identify the real function** — state the problem it solves, not its marketing category.
2. **Map overlap and missing capability** — compare it with the current execution, memory, document, wiki, graph, and governance layers.
3. **Separate method from implementation** — decide whether to adopt the underlying idea, install the product, run an isolated experiment, defer it, or reject it.
4. **Inspect primary evidence** — repository source, current branch/version, license, dependencies, security model, hooks, telemetry, network/API behavior, tests, and reproducible benchmarks. Treat stars and vendor benchmarks as weak evidence.
5. **Model coupling and side effects** — global Skills/config writes, Git hooks, MCP listeners, credentials, external semantic passes, duplicate state stores, background daemons, and cross-machine/channel conflicts.
6. **Choose the minimum reversible trial** — fixed commit/version, project scope rather than global scope, isolated environment, smallest feature set, no hooks/MCP/daemon/remote export unless the feature itself is under test.
7. **Define comparative questions and go/no-go criteria before running** — compare against the existing baseline on correctness, traceability, latency, cost, privacy, and maintenance burden.
8. **Verify with real output** — do not call an install, build, test, or graph successful without execution evidence. Record blocked/timeout results honestly.
9. **Promote only demonstrated value** — keep as project-level tooling before global integration; remove the isolated trial if it does not beat the baseline.

Preferred verdicts are more precise than “install/don't install”:

```text
adopt now
isolated project trial
absorb the method only
defer until trigger conditions exist
reject due to risk/duplication
```

When reporting, start with the direct verdict, then explain unique value, overlap, risks, minimum trial, and trigger conditions. Be warm and candid: protect the system without making the user feel guilty for bringing ideas.

## Cost and optimality

Do not optimize only for maximum capability. Minimize a practical loss:

```text
J = task error + safety/privacy risk + monetary cost + latency + maintenance burden + cognitive load
```

This is a decision aid, not a mathematically identified objective unless the terms are measured. State trade-offs instead of inventing precision.

## Adaptation rules

- Change policy only after evidence that operating conditions or the model changed.
- Use confidence and scope; do not universalize a local workaround.
- Preserve old facts as history when a new state supersedes them.
- Decay ranking of stale state; do not mechanically delete valuable principles.
- User feedback is a high-value observation, but safety and objective execution evidence still constrain the action.

## Fault tolerance

For consequential automation:

- keep backups or reversible edits;
- validate before activation;
- detect partial failure and duplicate execution;
- isolate credentials and machine responsibilities;
- define degraded operation;
- never let the same token or exclusive channel run from multiple uncontrolled instances.

## Anti-patterns

- Treating every activity as something to control.
- Treating the user as the controlled object; govern the Agent/workflow, not the person's behavior.
- Increasing observability by monitoring everything; collect only the minimum evidence needed, with privacy, consent and permissions first.
- Turning one success into permanent memory.
- Storing commands/procedures in core memory.
- Creating Skills that merely summarize a day.
- Optimizing output volume instead of verified usefulness.
- Adding feedback without observing latency/noise.
- Adding automation when the process is not observable or reversible.
- Calling a modern analogy “Qian Xuesen's original rule.”

## Verification checklist

- [ ] Goal and acceptance criterion are explicit.
- [ ] Actual evidence exists.
- [ ] Observation is sufficient to justify intervention.
- [ ] Memory candidate is stable, declarative, compact and non-procedural.
- [ ] Skill candidate contains trigger, feedback, failures and verification.
- [ ] No duplicate store was created.
- [ ] Change is reversible and bounded.
- [ ] Coupling, delay, noise and disturbances were considered.
- [ ] Final report distinguishes fact, inference and hypothesis.

## Sources

- H. S. Tsien, *Engineering Cybernetics*, McGraw-Hill, 1954.
- 钱学森著，戴汝为、何善堉译，《工程控制论（新世纪版）》，上海交通大学出版社，2007，ISBN 9787313043252.
- Z. Gao, “Engineering cybernetics: 60 years in the making,” *Control Theory and Technology* 12, 97–109 (2014), https://doi.org/10.1007/s11768-014-4031-0.

The daily knowledge-routing and Agent/Skill mappings in this Skill are modern operational deductions, not quotations from the book.

## Supporting references

- `references/primary-source-and-deployment.md` — concise primary-source evidence bank, selective OCR pattern for scanned technical books, and verified deployment pattern for scheduled daily closeouts.
- `references/historical-boundaries-and-agent-mapping.md` — terminology cautions, safe Agent mappings, privacy boundary, and evidence-promotion heuristic. Consult it before attribution claims or promotion into Skills/core memory.
- `references/candidate-tool-evaluation.md` — source-first repository/tool audit checklist, minimum reversible trial template, benchmark skepticism, and warm risk communication for user-discovered “toys.”
