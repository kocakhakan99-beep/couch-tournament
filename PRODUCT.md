# Product Requirements

## Vision
A browser-controlled party platform: private choices on phones, shared drama on a TV or browser display. Familiar social games and original short multiplayer experiences share one room system.

## Priorities
1. Correct, understandable rules and private-information boundaries.
2. Efficient, coherent implementation with small complete tasks.
3. Offline local testing before hosted multiplayer or casting.
4. Separate host, controller and display responsibilities from the beginning.
5. Approved design concepts before any game implementation.
6. Reusable foundations without building a universal game framework prematurely.

## Foundation scope
A functional catalog shell with blocked game entries, neutral styling, a local room harness, host/display/controller panels, simulated players and diagnostics. No playable games. No branding/design system decision beyond accessible functional defaults.

## Roles
Host: room setup and permitted session controls; not automatic access to every player's secrets.
Controller: a participant's private view and permitted actions.
Display: public-only read model; no authority over scoring or rules.
Authority: validates actions and owns canonical state. Initially local; later server-side.

## Non-goals now
Production Cast, AirPlay integration, physical multi-phone networking, accounts, payments, matchmaking, persistence services, live audio, real-time racing/fighting, eight-faction content production and finished visual design.

## Success criteria
The first shell can create/reset a local room, simulate 2-4 participants, display public roster and readiness, and show independent controller panels without gameplay. A later approved game can run through the same module boundary without importing network or casting APIs.

## Design gate
A game is blocked until both its concept/rules and its controller/display interaction design are approved. Final art may follow later, but unresolved rules, hidden information and screen responsibilities cannot be deferred to a coding agent. All current games start blocked.
