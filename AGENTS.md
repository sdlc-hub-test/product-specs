<!-- sdlc-hub:start -->
## SDLC Hub

This repository holds the specifications and the SDLC Hub. Run `node hub/cli.js serve` to open the site at http://127.0.0.1:4173. The flow, roles and engine are in `.hub/`. Feature documents live in `docs/features/<slug>/`.

Work on a feature through the hub commands, `$hub-<name>` in Codex and `/hub-<name>` in Cursor: `hub-status` shows where every feature is and `hub-next <slug>` runs your next step through the engine after the hub checks the gate. Sign-offs, returns and bugs go through `hub-signoff`, `hub-return` and `hub-bug`, which save them through merge requests in your name. Never edit `.hub/`, `hub/` or `signoffs.yaml` by hand.
<!-- sdlc-hub:end -->
