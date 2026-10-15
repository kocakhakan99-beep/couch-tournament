# Game Module Contract

## Mandatory entry gate
An approved docs/games/<id>/DESIGN.md exists with owner, version, approval date, concept, complete rules, state transitions, private/public data, controller/display interaction map and acceptance examples. Status must be approved. A catalog entry alone is not permission to code.

## Minimal responsibilities
- Metadata: stable id, title, player limits, design version and implementation status.
- Initial state from validated configuration and player roster.
- Action validation and deterministic state transition.
- Public display projection.
- Per-player controller projection.
- Host projection limited to host-authorized information.
- End condition and result summary.
- Controller and display renderers consuming projections, not canonical state.

## Rules
Keep rules pure and testable without a browser. Treat roster/session changes explicitly. Use platform lifecycle and connection interfaces rather than making new room systems. Content is bundled locally at this stage. No runtime AI generation or remote assets.

## Required tests
Initial state; valid/invalid actions; phase transitions; private-data exclusion; player limits; win/end conditions; deterministic outcomes; duplicate handling at authority boundary; reconnect snapshots; complete happy-path session; key edge cases specified in design.

## Catalog status
concept -> design_pending -> design_approved -> implementing -> local_testable -> device_tested -> cast_tested -> released.
Each status needs evidence. Do not label local_testable as device_tested. A module may declare required capabilities; the launcher blocks unavailable capabilities with a clear reason.

## Scope rule
Build one approved game as a vertical slice. Do not implement multiple themes, modes or faction rosters unless the active feature spec explicitly includes them.
