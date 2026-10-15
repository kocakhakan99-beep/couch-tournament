# Roadmap and Implementation Plan
No calendar estimates. Advance by evidence, not elapsed time. Only M0 is authorized by the first prompt.

| Milestone | Deliverable | Dependency / exit gate |
|---|---|---|
| M0 Foundation | offline shell, catalog, in-memory room, independent role panels, checks | foundation acceptance passes; no game implemented |
| M1 Contracts | freeze minimal protocol, authority validation, projections, deterministic utilities | protocol and privacy tests pass |
| M2 Design | approve platform interaction direction and first game's full design | owner approval recorded; unresolved rules closed |
| M3 First game | one approved game playable in local harness | complete session and edge-case tests; local playtest |
| M4 Offline robustness | static-build smoke tests, reset/reconnect semantics, optional export spike | offline behavior verified and limitations documented |
| M5 Multi-context | same-browser tab adapter if useful | authority-loss and snapshot tests; no physical-device claim |
| M6 LAN phones | local network authority, browser controllers, device matrix | real phones pass join/action/reconnect/privacy checks |
| M7 Cast | sender/receiver, hardware lifecycle, public display | real Cast tests and documented compatibility |
| M8 AirPlay | separate mirroring/compatibility investigation | supported paths documented; no private screen exposure |
| M9 Hosted beta | deployment, server security, monitoring, accounts only if needed | professional review and operational readiness |
| M10 Catalog growth | more approved games using stable contracts | each game has its own design and evidence |

## M0 task slices
FND-001: one-prompt foundation shell described in prompts/01_FOUNDATION.md.
FND-002: address only recorded foundation defects; no scope expansion.

## M1 task slices
CORE-001: finalize typed envelopes and role-bound connection port.
CORE-002: command validation, authority permissions and deduplication.
CORE-003: public/private projection and resync tests.
Each slice uses a feature spec; do not merge into a speculative framework rewrite.

## M2 task slices
DES-001: platform host/controller/display interaction design.
DES-002: first game concept and complete rules.
DES-003: first game screen/state mapping and test examples.
Approval is required before M3, not before the neutral technical shell.

## M3 task slices
GAME-001: pure rules plus fixtures/tests.
GAME-002: controller/display views against approved projections.
GAME-003: complete local session, failure cases and playtest record.

## Priority proposal
Would You Rather is the suggested inexpensive first game, but is NOT approved for implementation. Social suspicion and Silicon Valley rivalry are potential flagships. Tactics, audio and continuous action remain later scopes. The owner may change ordering without silently approving game designs.

## Stop conditions
Missing design, failing privacy boundary, unclear rules, repeated repair loop, unmeasured infrastructure expansion or conflicting documentation. Record the blocker and the smallest decision/task that resolves it.
