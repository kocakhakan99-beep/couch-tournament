# Documentation Index

## Always read
- ../AGENTS.md: agent workflow and credit discipline.
- STATUS.md: current milestone, blockers and next task.
- This index: choose the minimum relevant context.

## Read by task
| Task | Required documents |
|---|---|
| Foundation shell | PRODUCT, ARCHITECTURE, OFFLINE_AND_DEVICES, TESTING, first prompt |
| Room authority or protocol | ARCHITECTURE, PROTOCOL, SECURITY, TESTING |
| Game concept | PRODUCT, GAME_CATALOG, GAME_DESIGN template |
| Game implementation | approved game design, GAME_MODULE_CONTRACT, PROTOCOL, feature spec, TESTING |
| Visual design update | DESIGN_CHANGE_PROCESS, approved platform/game design, affected feature specs |
| Transport or phone support | OFFLINE_AND_DEVICES, PROTOCOL, SECURITY, ROADMAP |
| Cast/AirPlay | OFFLINE_AND_DEVICES, SECURITY, SOURCES, dedicated integration design |
| Cost review | CREDIT_POLICY, IMPLEMENTATION_LOG, active feature spec |

## Full pack
PRODUCT.md; ARCHITECTURE.md; PROTOCOL.md; GAME_MODULE_CONTRACT.md; OFFLINE_AND_DEVICES.md; ROADMAP.md; TESTING.md; SECURITY.md; CREDIT_POLICY.md; DESIGN_CHANGE_PROCESS.md; GAME_CATALOG.md; STATUS.md; IMPLEMENTATION_LOG.md; DECISIONS.md; SOURCES.md.

## Templates and prompts
- ../templates/FEATURE_SPEC.md
- ../templates/GAME_DESIGN.md
- ../templates/IMPLEMENTATION_ENTRY.md
- ../templates/ADR.md
- ../prompts/01_FOUNDATION.md
- ../prompts/FEATURE_IMPLEMENTATION.md
- ../prompts/DESIGN_APPROVAL.md

## Documentation size policy
STATUS stays short and current. Append history to IMPLEMENTATION_LOG; split by milestone when needed. Link to authoritative definitions instead of copying them. One concept has one canonical definition. Do not maintain parallel contradictory specifications.
