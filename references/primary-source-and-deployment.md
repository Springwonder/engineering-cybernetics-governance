# Primary-source evidence and deployment notes

## Source identity

Primary text used in the originating implementation:

- 钱学森著，戴汝为、何善堉译，《工程控制论（新世纪版）》，上海交通大学出版社，2007，ISBN 9787313043252.
- English original: H. S. Tsien, *Engineering Cybernetics*, McGraw-Hill, 1954.
- Supporting retrospective: Z. Gao, “Engineering cybernetics: 60 years in the making,” *Control Theory and Technology* 12, 97–109 (2014), DOI 10.1007/s11768-014-4031-0.

The 2007 PDF encountered was a 328-page image-only scan. Metadata and page count were verified before interpretation. A selective RapidOCR pass over front matter, contents, and representative control chapters produced enough text to ground the governance framework without claiming full-book coverage.

## Directly supported principles

The Chinese preface states that engineering cybernetics:

- studies interactions among different parts of a system and the overall state of motion;
- focuses on portions of cybernetics directly useful for engineering design of controlled systems;
- organizes and summarizes design principles from engineering practice into theory, revealing commonality across fields;
- enables a broader view and more systematic observation of problems.

The contents directly cover input/output and transfer functions, feedback servomechanisms, feedback design criteria, multiloop systems, and delayed systems.

## Modern mappings — label as deductions

Mappings from reference, plant, state, observation, control, disturbance, stability, delay, coupling, and cost to Hermes tasks, memory, Skills, Cron, logs, and user feedback are modern operational deductions. Never present “Agent Skills,” “LLM memory,” or software observability as terminology from Qian’s original work.

## Scanned-book extraction pattern

For a long image-only technical book:

1. Verify bibliographic identity, metadata, page count, and whether a text layer exists.
2. OCR the preface and table of contents first to establish scope and authorial intent.
3. OCR representative chapter openings and passages relevant to the intended application.
4. Preserve page markers in OCR output for traceability.
5. Quote only passages actually inspected; label broader synthesis as inference.
6. Escalate to full-book OCR only if selective extraction leaves a material evidence gap.

This reduces cost and OCR noise while keeping claims traceable.

## Daily review deployment pattern

When attaching this governance method to a scheduled daily closeout:

- load the governance Skill alongside the logging/Obsidian Skill;
- require direct evidence from artifacts, tests, logs, tool output, and explicit feedback;
- prohibit scheduled jobs from automatically rewriting core memory;
- have the job propose memory candidates for review;
- prefer updating an existing Skill over creating a new one;
- create no Skill when no validated reusable learning exists;
- report target, observed state, deviation, disturbance, action, verification, residual error, and next observation point;
- test-run the scheduled job and read back its actual output before declaring success.

## Important operational lesson

A daily Skill review is a feedback controller, not a content-production quota. “No Skill change” is a valid output when evidence is insufficient. Forcing a change every day would amplify noise and cause policy oscillation.