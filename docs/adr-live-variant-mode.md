- `live-server.mjs`; HTTP server (SSE, poll, source file reader)
- `live-poll.mjs`; CLI client for the agent poll/reply loop
- `live-wrap.mjs`; CLI helper that finds elements in source and creates variant wrappers
- `live-browser.js`; Browser script (element picker, action panel, variant cycler, global bar)
 │  ├── GET  /live.js    ; browser script (token injected)        │
 │  ├── GET  /detect.js  ; anti-pattern overlay (backwards compat)│
 │  ├── GET  /events     ; SSE stream to browser (server push)    │
 │  ├── POST /events     ; browser events (generate, accept, etc.)│
 │  ├── GET  /poll       ; agent long-poll (blocks until event)   │
 │  ├── POST /poll       ; agent reply (forwarded to browser SSE) │
 │  ├── GET  /source     ; raw file reader (no-HMR fallback)     │
 │  ├── GET  /health     ; status, port, connected clients        │
 │  └── GET  /stop       ; graceful shutdown                      │