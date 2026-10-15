# Offline, Browser, Phone and Cast Plan

## Three different meanings of offline
A. Local HTTP browser testing: no internet after installation/build; a local server serves bundled assets. This is the initial target.
B. Double-click HTML export: a self-contained artifact opened through file protocol. Separate optional milestone with explicit browser tests.
C. Offline LAN multiplayer: several physical devices on the same network using a local authority and network transport. Separate milestone; not provided by A or B.

## Initial harness
One browser page contains separate host, public display and 2-4 controller panels. All use the same client port and in-memory authority. Label this simulated multi-client operation. No claim of real smartphone support yet. Controller layout is narrow-screen friendly from the start.

## Same-browser tabs
A later adapter may use BroadcastChannel for same-origin, same-storage-partition contexts [S2]. It does not connect separate phones or a Chromecast. Keep one explicit authority tab. Loss of that tab pauses the session; failover is out of scope initially. Never broadcast canonical private state to a common channel.

## Physical phone milestone
Add a small local server with a network transport after protocol tests. Bind safely for LAN access, show host LAN address, document firewall/network assumptions, validate commands and bind identities server-side. Test actual iOS/Android browsers, refresh, sleep/backgrounding and reconnect. Plain HTTP LAN access is not a substitute for secure contexts when microphone features are added.

## Build/export
Vite's ordinary production build targets static hosting; relative base paths adjust asset URLs but do not prove file-protocol compatibility [S1]. Initial build must work from a local static server. If a single-file export is approved, bundle scripts/styles/assets, remove runtime fetch/module-path assumptions and test direct opening explicitly. Do not add export tooling to the first task.

## Cast milestone
Dedicated sender/receiver integration. Receiver renders public view and connects to the authority; phones connect separately. Production receiver hosting and registration are required, and the receiver SDK is externally sourced [S3]. Consequently the initial offline harness is not a fully offline Cast product. Test real devices, receiver lifecycle, rendering limits, session resume and public-only data.

## AirPlay milestone
Investigate separately. Start with public display mirroring from a host device; never mirror private controls. Do not promise Cast-equivalent receiver behavior. Verify supported host/device/browser combinations before publishing compatibility claims.

## Capability matrix
| Mode | Initial scope | Claim allowed |
|---|---|---|
| Single-page harness | yes | simulated host/display/controllers |
| Local static build | first milestone | offline browser testing after installation |
| Same-browser tabs | later | same-browser multi-context testing |
| Actual phones | later | only after LAN/device tests |
| Direct HTML file | optional later | only after export tests |
| Chromecast | larger later project | only after hardware tests |
| AirPlay | separate later project | only verified combinations |
