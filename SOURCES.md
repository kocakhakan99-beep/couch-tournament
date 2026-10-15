# Technical Sources and Verification Notes
Checked: 2026-10-15. These sources support platform constraints, not promised project performance or cost. Recheck relevant documentation when implementing an integration.

- S1: [Vite production build documentation](https://vite.dev/guide/build). Ordinary build produces a static-hosting bundle; relative base controls generated asset paths. It does not establish universal direct-file execution.
- S2: [MDN Broadcast Channel API](https://developer.mozilla.org/en-US/docs/Web/API/Broadcast_Channel_API). Communication is limited to matching origin/storage partition browsing contexts; it is not a physical-device network transport.
- S3: [Google Cast custom Web Receiver documentation](https://developers.google.com/cast/docs/web_receiver/basic). Custom receiver is hosted HTML5, registration is required, published receiver needs TLS-capable hosting and the SDK must not be self-hosted.

Project architecture, milestone order, gates and credit policies are recommendations tailored to this project, not external factual claims. No current provider pricing or model ranking is asserted here.
