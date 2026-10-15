# Coding Agent Operating Contract

## Read order and context budget
Always read this file, docs/STATUS.md and docs/INDEX.md first. Then read only the task's feature specification and the relevant contract/design documents linked by the index. Search for exact symbols before opening entire source directories. Do not repeatedly ingest the whole repository or implementation history.

## Non-negotiable rules
- One task, one bounded deliverable. Do not implement later roadmap milestones opportunistically.
- No game implementation without an approved, versioned game concept and interaction design. A fixture that checks room plumbing is not a game and must not become one.
- No new dependency, transport, storage service or architectural rewrite without documenting why it is necessary.
- Keep domain logic independent of React, DOM, network SDKs and persistence.
- Never send canonical private state to a public display and hide it with CSS.
- Use strict TypeScript. No unexplained any, suppressed checks, disabled tests or blanket lint exceptions.
- Validate external commands at the authority boundary. Clients submit intent, not scores or trusted player identities.
- Inject time and randomness into rules. Do not call Date.now or Math.random inside reducers.
- Keep state JSON-serializable. No functions, DOM nodes, class instances or mutable shared references in game state.
- Do not put secrets in source, logs, URLs, screenshots or documentation.
- Preserve unrelated files. No broad formatting or lockfile churn.
- Never claim a command ran, a test passed, a browser was checked or a commit was created unless it actually happened.

## Task procedure
1. Identify task ID, scope, dependencies, design gate and acceptance criteria.
2. Inspect the smallest relevant code and docs. Check current scripts before proposing commands.
3. State a concise plan and assumptions. If a game design is missing, report the gate and work only on authorized non-game tasks.
4. Implement the smallest complete vertical slice. Prefer existing helpers over new abstractions.
5. Add targeted tests; run targeted checks first, then required regression checks.
6. Update the feature record, STATUS and IMPLEMENTATION_LOG. Add an ADR only for a lasting architectural decision.
7. Report files changed, commands and results, remaining limitations, documentation updates and the next eligible task.

## Repair discipline
After a failed check, inspect the actual error before changing code. Do not rewrite unrelated modules. After two materially similar unsuccessful repair attempts, stop the loop, document evidence and propose a smaller task or focused review. This is a credit-control policy, not permission to conceal failure.

## Documentation precedence
Safety/security constraints > approved architecture/protocol > approved game design > approved feature specification > task prompt > notes. A conflicting prompt does not silently supersede approved contracts. Document the conflict and a proposed resolution.

## Delivery standard
A successful task includes code, relevant tests and truthful documentation. A partial task explicitly marks incomplete acceptance criteria. Do not commit unless requested or the task explicitly authorizes it; propose a checkpoint commit message instead.
