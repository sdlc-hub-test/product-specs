---
description: "Runs your next step on a feature through the engine, after the hub checks the gate. Use when the person wants to work on a feature."
argument-hint: "[slug] [step]"
allowed-tools: mcp__plugin_hub_hub__hub_next mcp__plugin_hub_hub__hub_status mcp__plugin_hub_hub__hub_record
---
Call `hub_next` with the slug and, if given, the step from "$ARGUMENTS" (in that order).

- If it reports an error, show it and stop. Do not run any stage the hub did not give you.
- Otherwise run the engine command it gives exactly as written, with the hub's prompt as context, and follow that stage to its end.
- When the stage has run to its end, call `hub_record` with the slug and the step, so the site shows it finished.
- When the answer says the gate needs a sign-off, tell the person and stop: only they sign, with `/hub:signoff`.
