# Architecture: Offline First, Multi-Client Ready

## Decision
Single repository and package initially. React + TypeScript + Vite; plain CSS; Vitest. Avoid Next.js, Supabase, monorepo tooling and backend services until a milestone demonstrates the need. These are project recommendations, not assertions of universal superiority.

## Proposed structure
```text
src/
  app/                 # composition, catalog and local harness
  platform/
    domain/            # room types, authority, commands, projections
    ports/             # client connection, clock, randomness interfaces
    adapters/          # in-memory now; local tabs/LAN later
    ui/                # host, controller, display shells
  games/
    catalog.ts         # metadata only for blocked concepts
    <approved-game>/   # rules, views, tests, approved design reference
  shared/              # genuinely shared small utilities
  styles/              # neutral functional styling
  test/                # fixtures; not playable games
```

## Dependency direction
UI -> client connection port -> authority -> room/game domain.
Adapters implement ports. Domain imports no UI or transport. A game never calls Cast, WebSocket, localStorage or fetch directly. The composition root selects adapters.

## Authority model
One room authority serializes accepted commands. Clients cannot mutate its state. Public and player-specific snapshots are projected separately. The local adapter binds a connection to a role/player, mirroring future authenticated connection context without pretending to provide real security.

## Avoid premature generalization
Define only the minimum module contract needed by the first approved game. Do not build an ECS, plugin marketplace, visual rules editor or generic scripting engine. Add shared capabilities only when two concrete modules need them or a current acceptance criterion requires them.

## Determinism
Reducers accept explicit command, authoritative time and random values/context. Rules do not access browser clocks. Tests supply deterministic sequences. Seeded randomness is for reproducible tests, not production secret-card security. Later production randomness and shuffle requirements get a dedicated design.

## Lifecycle
Create room -> lobby -> approved game session -> results -> lobby. Foundation implements create/lobby/reset only. Room and game state versions are explicit. Authority loss in early local mode pauses/ends the local session visibly; do not silently elect another authority.

## Performance
Use projected snapshots initially. Do not implement continuous simulation or input prediction. Add diffs, compression or specialized action-game transport only after measurement. Do not promise Cast performance from desktop tests.

## Design isolation
Use semantic components and CSS variables for basic spacing/color. Rules never depend on visual animation completion. Animation is presentation; the authority determines phase changes. Design changes must preserve protocol and behavior unless an approved change explicitly alters them.
