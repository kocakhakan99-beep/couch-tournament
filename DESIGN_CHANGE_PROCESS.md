# Design Gates and Later Documentation Updates

## Two approval levels
Platform interaction/visual design: navigation, host/controller/display layouts, accessibility, responsive behavior, visual tokens.
Game design: concept, rules, roles, information, state transitions, input/display map, failure behavior and examples.
A neutral technical shell can precede visual design. No game can precede its approved concept and interaction design.

## Approval record
Owner: Hakan. Record design id, version, status, approval date and explicit approval evidence. An agent may propose but must not approve its own game design. Pending questions block implementation if they affect rules, privacy or interactions.

## Change process
1. Record proposed change and reason.
2. Identify affected rules, protocol, UI, tests and docs.
3. Classify as presentation-only or behavioral.
4. Update the canonical design and version.
5. Obtain approval for behavioral changes or changed scope.
6. Update affected feature specs and roadmap dependencies.
7. Implement a bounded change with regression checks.
8. Record evidence and remove obsolete instructions.

## Documentation impact checklist
PRODUCT; ARCHITECTURE if boundaries change; PROTOCOL if messages/views change; GAME_MODULE_CONTRACT if shared responsibilities change; game DESIGN; feature spec; TESTING; STATUS; IMPLEMENTATION_LOG; ADR for lasting decisions.
Do not edit every document mechanically: mark unaffected documents as unchanged in the feature record.

## Compatibility
A visual refresh must not accidentally change scores, timing, permissions or hidden information. Behavioral changes require new tests. Network protocol changes require explicit version/compatibility handling before multiple clients depend on them.
