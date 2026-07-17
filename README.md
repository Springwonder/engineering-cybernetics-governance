# Engineering Cybernetics Governance Skill

A portable Agent Skill for governing AI-agent learning, memory, reusable procedures, and daily review through an engineering-cybernetics lens.

The central rule is simple:

> Stable cross-task principles belong in memory; reusable control procedures belong in Skills; one-off states and unverified hypotheses stay in logs or experiments.

## What this is

This repository translates selected principles from H. S. Tsien / 钱学森's *Engineering Cybernetics* into a modern operational framework for AI agents:

- define goals and acceptance criteria;
- observe real evidence instead of trusting self-reports;
- distinguish structural defects from disturbances and noise;
- update procedures through bounded, reversible feedback;
- check stability, coupling, delay, cost, privacy, and rollback;
- prevent memory pollution and Skill proliferation;
- treat “no change” as a valid daily-review outcome.

## What this is not

- It is not a claim that people are machines or should be controlled.
- It does not treat the user as the controlled object; it governs the Agent and technical workflow.
- It does not attribute modern AI terms such as Agent Skills, LLM memory, software observability, or CI to Qian's original text.
- It does not claim that the 1954 book already contained the complete later theories of Kalman controllability/observability, mature system identification, LQR, or modern fault-tolerant control.
- It does not redistribute the underlying book or any scanned/OCR copy.

## Repository layout

```text
SKILL.md
references/
  primary-source-and-deployment.md
  historical-boundaries-and-agent-mapping.md
LICENSE
CITATION.cff
```

## Use

Install or copy this directory into the Skill location used by your Agent framework, then load `engineering-cybernetics-governance` for:

- end-of-day evidence review;
- deciding whether an experience belongs in memory, a Skill, a log, or an experiment;
- evaluating system changes and candidate tools;
- designing bounded adaptation and rollback;
- auditing whether an Agent's “self-improvement” is evidence-backed.

The exact installation path varies by framework. The Skill itself is framework-agnostic Markdown.

## Core daily loop

```text
Target
→ observed state
→ deviation
→ disturbance / uncertainty
→ bounded control action
→ verification
→ residual error
→ next observation point
```

If evidence is insufficient, do not create a new rule, Skill, or memory.

## Evidence and attribution

Primary references:

- H. S. Tsien, *Engineering Cybernetics*, McGraw-Hill, 1954.
- 钱学森著，戴汝为、何善堉译，《工程控制论（新世纪版）》，上海交通大学出版社，2007，ISBN 9787313043252.
- Z. Gao, “Engineering cybernetics: 60 years in the making,” *Control Theory and Technology* 12, 97–109 (2014), https://doi.org/10.1007/s11768-014-4031-0.

The AI-agent mappings and knowledge-governance workflow in this repository are modern operational deductions, not quotations from the book and not endorsed by the authors or publishers of the cited works.

## License

The original Skill text and operational framework in this repository are released under the MIT License. The cited books and papers remain under their respective copyrights and are not included.
