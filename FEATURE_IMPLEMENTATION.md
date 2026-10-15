# Reusable Feature Implementation Prompt

Implement <TASK-ID> using <feature-spec-path> only.
Read AGENTS.md, docs/STATUS.md, docs/INDEX.md, the feature specification and its linked contracts/design. Inspect only relevant code. Verify dependencies and design approval before game work.

Deliver the smallest complete implementation satisfying the spec. Preserve unrelated behavior. No extra dependencies, later milestones or speculative refactors. Follow authority/private-view boundaries. Add targeted tests, run required checks and update the spec, STATUS and IMPLEMENTATION_LOG. Record architectural decisions only when needed.

If a game design is not approved, do not implement that game. If checks fail, diagnose the actual error; follow the repair budget. Do not disable checks or claim unrun tests passed.

Report acceptance results, files, verification evidence, documentation updates, known limitations, recorded cost if available and next eligible task.
