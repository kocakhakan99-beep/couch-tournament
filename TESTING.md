# Testing and Definition of Done

## Required scripts to implement in M0
npm run dev; npm run build; npm run preview; npm run typecheck; npm run lint; npm run test -- --run.
Scripts are requirements until created. Use the repository's actual scripts afterward. Do not claim these already run.

## Test layers
1. Unit: room rules, projections, command validation, game reducers.
2. Integration: connection port -> authority -> authorized snapshots.
3. UI: role-specific controls and accessibility states.
4. Browser smoke: build loading, create/reset, simulated players, responsive panels.
5. Device/hardware: later LAN/Cast milestones, not replaceable by desktop screenshots.

## M0 acceptance
- Install/build/check commands are documented and run where tools allow.
- No runtime cloud calls, remote fonts, CDN assets or API keys.
- Create a local room; add 2-4 simulated participants; change readiness; reset.
- Display receives roster/readiness only, not controller-local fixture data.
- Host/display/controller components are separate.
- Catalog games are visibly blocked pending design; no playable game.
- Two independent rooms do not share state.
- Invalid participant/action is rejected; state remains unchanged.
- Build served locally works with internet disabled after dependencies are available.
- Narrow controller layout remains usable; controls have labels and keyboard focus.
- STATUS/log accurately distinguish automated checks from manual checks not performed.

## Future regression matrix
Duplicate command; stale revision; unauthorized role; wrong phase; out-of-order snapshot; reconnect; host/display loss; room isolation; malformed payload; secret exclusion; deterministic replay where supported.

## Done checklist
Acceptance criteria checked individually; targeted tests added; required regression commands run; no suppressed failures; docs synchronized; remaining limitations stated; checkpoint commit suggested. Tests not run are NOT PASS.

## Evidence format
Command, environment, result, relevant output summary. Browser/device evidence includes browser version/device and actual action performed. No fabricated coverage percentages or performance numbers.
