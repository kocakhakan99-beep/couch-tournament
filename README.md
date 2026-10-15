# Party Platform: Starting Documentation Pack
Version: 0.1 | Date: 2026-10-15 | Owner: Hakan | Status: foundation planning approved; game designs pending

## Purpose
Build a coherent offline-first party-game platform with browser-phone controllers and a shared display. Maximize useful implementation per AI credit through small, complete tasks, explicit contracts, executable checks and navigable documentation. No claim of guaranteed one-prompt success or fixed AI cost is made.

## Start here
1. Read AGENTS.md.
2. Read docs/INDEX.md and docs/STATUS.md.
3. Read docs/PRODUCT.md, docs/ARCHITECTURE.md and docs/OFFLINE_AND_DEVICES.md.
4. Use prompts/01_FOUNDATION.md for the first implementation only.
5. Use docs/ROADMAP.md for subsequent milestones and templates/FEATURE_SPEC.md for each feature.
6. Do not implement a game until its concept and interaction design are approved using templates/GAME_DESIGN.md.

## What this pack is
Repository-ready Markdown documentation and implementation prompts. It is not a running application. Commands, interfaces and folder structures are proposed implementation requirements, not claims that code already exists or tests have passed.

## Starting decision
Use a single TypeScript project with React and Vite, plain CSS, Vitest and a small runtime validation library such as Zod. This replaces the earlier Next.js/Supabase-first recommendation for this offline stage. Do not add a backend, database, Cast SDK, accounts, payments or cloud dependency yet. Record dependency versions in the generated lockfile; do not invent latest versions.

## Design later
The foundation uses neutral functional styling. Platform visual design and every game's design will be approved separately. Rules, transport and view projections must remain independent of styling so design updates do not require rewriting game logic.

## Offline definition
The initial target is a browser application served by a local static/dev server with no internet required after dependencies are installed. Opening index.html directly from the filesystem is a separate export milestone, not an implied capability. Actual phones on a LAN need a network transport milestone. See docs/OFFLINE_AND_DEVICES.md.

## Navigation
The full document map is docs/INDEX.md. Each implementation must update the relevant specification, tests, status and implementation log. Documentation describes verified reality, not optimistic completion.
