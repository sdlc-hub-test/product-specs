---
description: "QA's final check: pass the feature to release, or return it to verify with the reason and the bugs."
argument-hint: "<slug>"
disable-model-invocation: true
allowed-tools: mcp__plugin_hub_hub__hub_qa
---
The feature is "$ARGUMENTS".

1. Call `hub_qa` and show the criteria still open, the open bugs and the latest CI runs.
2. Ask the person: pass to release, or return to verify? For a return, ask for the reason and which open bugs it is about.
3. Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "pass" or "return".
4. Call `hub_decide` and show the answer as it is.
