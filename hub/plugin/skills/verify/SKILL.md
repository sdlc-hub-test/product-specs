---
description: "QA's AI-assisted check of a feature on staging: each criterion on each platform, then the verdicts and the bugs."
argument-hint: "<slug>"
disable-model-invocation: true
allowed-tools: mcp__plugin_hub_hub__hub_qa
---
The feature is "$ARGUMENTS".

1. Call `hub_qa` for the criteria, the platforms, the open cells and the bugs.
2. For each open criterion and platform, check it on staging with the tools this machine has (Playwright for web, Maestro for mobile), or walk the person through it. Report what you saw.
3. For a failure, propose a bug with its criterion, platforms, owning team and severity; file it with `hub_bug` only after the person confirms it.
4. Propose the verdicts (pass, fail with its bug, or na). Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "save these verdicts". Then call `hub_verdicts`.
5. When every cell passes or does not apply, tell the person they can sign off verify with `/hub:signoff verify <slug>`.
