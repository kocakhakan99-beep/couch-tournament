# AI Credit Efficiency Policy

## Objective
Maximize accepted, tested deliverables per credit. Minimize rework and irrelevant context, not merely output length. One-prompt success is a priority, never a guarantee.

## Prompt readiness gate
Task has ID; dependencies ready; approved design where required; exact files/docs; bounded deliverable; non-goals; acceptance criteria; verification commands; documentation updates. If missing, write a spec before requesting implementation.

## Model routing
Use a capable coding model for contracts, privacy, state transitions and hard debugging. Use cheaper models for well-specified repetitive UI/content/docs tasks. Do not change models during a difficult task merely to save nominal token price. Verify current provider rates before making budgets; no model/pricing claims are frozen in this pack.

## Context discipline
Read index/status then linked docs. Keep architecture/contracts concise. Use exact searches and targeted file ranges. Do not paste generated bundles, lockfiles, entire logs or the complete chat history. Summarize failures with relevant evidence. Reuse stable project instructions instead of repeating them.

## Task discipline
One vertical slice; explicit non-goals; deterministic fixtures; reuse helpers; no unnecessary dependencies; no speculative polish; no broad rewrites. Design/content decisions are made before implementation. Do not ask the model to invent the rules while writing them.

## Record costs honestly
For each task: model/tool, usage source, credits/tokens/cost if reported, attempts, accepted criteria, rework and unresolved defects. Unknown is unknown, not zero. Subscription charges and API usage are different accounting categories; do not count both for the same usage unless both were actually charged.

## Metrics
First-pass acceptance = accepted tasks without corrective prompt / completed tasks.
Cost per accepted task = attributable recorded cost / accepted tasks.
Rework ratio = corrective attempts / implementation attempts.
Use metrics only when actual records exist. No invented savings percentages.

## Repair budget
Two materially similar failed repair attempts trigger diagnosis/scope reduction. Preserve the last known-good checkpoint. Do not burn credits repeatedly asking 'fix everything'.

## Documentation efficiency
Log meaningful decisions, changes, checks and blockers, not every keystroke. Keep a concise current status plus append-only history. Avoid duplicated documentation that costs credits to keep consistent.
