# Architecture Decision Register

## ADR-001: offline-first static frontend
Status: adopted planning default.
Decision: Vite/React/TypeScript instead of the earlier Next.js/Supabase-first approach.
Reason: current priority is local browser testing without hosted services.
Consequence: networking, persistence and hosting are deferred, not eliminated.

## ADR-002: one authority, role-specific projections
Status: adopted planning default.
Decision: rules owned by one authority; UI receives authorized projections through a client port.
Reason: prepare for private phone controls and public Cast display.
Consequence: local mode is logically separated but not secure against browser inspection.

## ADR-003: games require approved design
Status: adopted.
Decision: no game code before approved concept/rules and interaction map.
Reason: prevent expensive implementation of guessed mechanics.
Consequence: catalog entries remain blocked; technical fixtures do not bypass the gate.

## ADR-004: distinguish offline modes
Status: adopted.
Decision: local HTTP first; direct-file export, LAN devices and Cast are separate milestones.
Reason: different capabilities and constraints must not be conflated.
Consequence: no misleading 'phone/Cast ready' claims from a local harness.

New decisions use templates/ADR.md. Record superseded decisions rather than silently erasing history.
