# Security and Privacy Boundaries

## Local prototype
Not a secure multiplayer product. All canonical state may exist in the same browser process. Role projections enforce architecture and test data flow, not resistance to developer tools. Display this limitation in developer documentation.

## Required even locally
Validate commands; render user strings as text; bound nickname/payload sizes; avoid unsafe HTML; separate room/session identity; no secrets or personal data in logs; exclude private fields from public projections; do not add analytics or recordings by default.

## Before physical networking
Server-bound identity; host/player/display credentials; room join rate limits; origin policy; payload limits; connection cleanup; session expiry; command replay/deduplication policy; safe reconnect; explicit trust model. No client-computed scores or client-provided authoritative randomness.

## Before hosted beta
Threat model, TLS, dependency review, secrets management, logging/redaction, backups if persistent, abuse handling, deployment rollback and professional security review. Accounts/payments require separate approved designs. A room code alone must never grant host privileges.

## Sanctioned cheating
Only approved game actions. It does not permit bypassing authentication, reading another player's hidden state through developer tools, exploiting APIs or manipulating the authority. Distinguish game deception from security defects.

## Audio
Separate permission, retention and licensing design. No recording by default. No microphone access in the foundation.
