# Historical boundaries and AI-agent translation notes

Use this reference when applying *Engineering Cybernetics* to Hermes knowledge governance.

## Directly supported by the 1954/2007 book

The book directly treats:

- input, output, and transfer functions;
- feedback servomechanisms and design criteria;
- multivariable and noninteracting control;
- delayed systems and random inputs;
- nonlinear and switching control;
- automatic search for optimum operating points;
- filtering, self-stabilization, adaptation, redundancy, and error control.

The original preface frames engineering cybernetics as a technical science that extracts common design principles from different engineering practices, studies interactions among system parts and overall behavior, and seeks methods that can directly improve engineering design.

## Terms that require historical care

Do not claim the 1954 book already contained today's complete formal theories of:

- Kalman controllability and observability;
- mature system identification;
- LQR/dynamic-programming optimal control;
- modern fault-tolerant control.

Kalman's formal controllability/observability work appeared in 1959 and later. In the governance Skill, “observable” and “controllable” are modern operational checks:

- observable: logs, tests, artifacts, or feedback are sufficient to determine success and diagnose deviation;
- controllable: Hermes has a real action path, permission, and bounded intervention capable of moving the process toward the goal.

## Safe AI-agent mapping

This is an engineering analogy, not a quotation from Qian:

| Engineering concept | Agent-governance mapping |
|---|---|
| reference/goal | acceptance criterion |
| plant/process | workflow or agent system |
| state | minimum recoverable task/configuration state |
| observation | tool output, tests, logs, user correction |
| control action | reversible workflow/config/Skill change |
| disturbance | network, version, ambiguity, prompt injection, model drift |
| residual | expected-versus-actual behavior |
| adaptation | evidence-backed Skill adjustment |
| fault tolerance | retry, idempotency, backup, rollback, degraded mode |

Govern the Agent and technical workflow—not the user's behavior. Improving observability never justifies collecting unnecessary private data.

## Evidence promotion heuristic

Track observation count, independent task count, successes, counterexamples, applicable conditions, confounders, and confidence.

- one observation: log only;
- two similar observations: candidate;
- repeated independent reproduction, or one high-cost incident with a clear mechanism: Skill change;
- cross-task long-term stability plus explicit user confirmation: core-memory candidate.

This is not a rigid sample-count law. Explicit durable user decisions and high-impact safety facts may be promoted immediately when their scope and mechanism are clear.

## Sources

- H. S. Tsien, *Engineering Cybernetics*, McGraw-Hill, 1954.
- 钱学森著，戴汝为、何善堉译，《工程控制论（新世纪版）》，上海交通大学出版社，2007，ISBN 9787313043252.
- Z. Gao, “Engineering cybernetics: 60 years in the making,” *Control Theory and Technology* 12, 97–109 (2014), https://doi.org/10.1007/s11768-014-4031-0.
