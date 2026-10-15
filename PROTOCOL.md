# Room and Client Protocol v0.1
Status: proposed contract; refine in the protocol milestone before a game uses it.

## Commands
A command envelope contains protocolVersion, roomId, sessionId where relevant, commandId, expectedRevision when required, type and payload. The authenticated/bound connection supplies actor identity; never trust an actorId supplied by the payload.

## Authority processing
1. Validate schema, size and protocol version.
2. Resolve connection role and player identity.
3. Check room/session membership and action permissions.
4. Check phase and optional revision precondition.
5. Check commandId deduplication within the session.
6. Apply the action once, advance revision and produce projected views.
7. Return an acknowledgement or structured rejection.

## Rejections
Examples: INVALID_COMMAND, UNAUTHORIZED, WRONG_PHASE, STALE_REVISION, ROOM_NOT_FOUND, SESSION_ENDED, DUPLICATE_COMMAND. A duplicate returns the recorded outcome without applying the action twice. Document deduplication retention limits before networking.

## View envelope
protocolVersion, roomId, sessionId, revision, viewKind, public room metadata and the role-specific view. Never include full canonical state in client snapshots. Display receives no player secrets; a controller receives only its own permitted secrets.

## Delivery
Client connections expose send(command), subscribe(view/error), getConnectionState() and close(). Exact TypeScript signatures are frozen by the protocol task. UI does not know whether the connection is in-memory, same-browser or networked.

## Resync
On connect/reconnect request a complete authorized snapshot. Ignore older revisions. Retry an unacknowledged command using the same commandId. Do not guess that a timeout means the action failed. Timers are based on authoritative deadlines, not trusting a client's countdown.

## Local limitations
The in-memory harness has logical privacy, not a security boundary: a person with browser developer tools can inspect local state. Same-browser messaging is also not secure against other same-origin scripts. Production privacy requires server authority and authenticated role-scoped delivery.

## Future identity
Room code locates a room; it is not a host credential. Host, player reconnect and display access credentials must be distinct. No host secrets in a QR join link. Networking design must define expiry, revocation and safe storage before implementation.
