# First Implementation Prompt: FND-001
Copy the text below into your coding agent after placing this documentation pack in an empty project repository. This is intentionally a foundation task, not a prompt to build the whole product.

---
Implement FND-001: the offline party-platform foundation only.

Read AGENTS.md, docs/STATUS.md, docs/INDEX.md, docs/PRODUCT.md, docs/ARCHITECTURE.md, docs/OFFLINE_AND_DEVICES.md and docs/TESTING.md. Inspect the repository before scaffolding; preserve these documents. If existing code conflicts, report it rather than overwrite blindly.

Use one React + strict TypeScript + Vite project with plain CSS, Vitest, ESLint and only minimal necessary dependencies. Pin resolved dependencies through a lockfile. No Next.js, backend, database, cloud service, accounts, payments, Cast SDK, microphone, remote fonts or runtime API calls.

Build:
1. A neutral functional platform shell with catalog metadata for the concepts in docs/GAME_CATALOG.md. Every game is visibly blocked: Design required. Do not implement any playable game.
2. A local diagnostic harness with separate HostPanel, PublicDisplayPanel and ControllerPanel components. The host creates/resets a room and adds 2-4 simulated players. Each controller can change its own readiness. Display shows public roster/readiness only. This is platform plumbing, not gameplay.
3. A small in-memory room authority and role-bound client connection interface. UI sends commands; it never mutates canonical room state. Separate public and per-controller projections. Keep this minimal; do not implement the entire future protocol in this task.
4. Two independent room instances must not share state. Unknown-player/invalid readiness commands must be rejected without mutation. Do not put canonical state in a global UI singleton.
5. Narrow-screen-friendly controller layout, semantic labels, keyboard focus and clear errors. No final visual design or animations.
6. Tests for create/reset, independent rooms, readiness permission, invalid action and public projection excluding private controller fixture fields. A fixture can contain a private marker solely to test projection; do not build cards, scoring or rounds.
7. Scripts: dev, build, preview, typecheck, lint and test. Bundle all runtime assets locally. Document local-server offline testing; do not claim direct-file HTML or real-phone networking works.
8. Update README with actual setup/check commands, docs/STATUS.md with actual progress and docs/IMPLEMENTATION_LOG.md with evidence. Record unrun checks explicitly.

Acceptance: the harness works locally, all game entries remain blocked, role components and authority are separated, tests/checks pass where execution is available, no runtime external services, and documentation accurately reflects reality.

Out of scope: any game, real phone networking, BroadcastChannel adapter, production reconnect, Cast/AirPlay integration, single-file export, polished design, authentication, persistence, payment, generic plugin engine or extra roadmap milestones.

Work through this bounded task without requesting confirmation between steps. Do not invent missing game rules. If environment limitations prevent a check, deliver the completed portions and report exactly what was not verified. Do not suppress failing checks.

Final report: files changed; acceptance checklist; commands/results; limitations; docs updated; suggested checkpoint commit; next eligible task. Do not claim a commit unless actually authorized and created.
---
