---
name: hub-release
description: "Ops walks the release checklist of a feature and records the smoke check and the rollout. It never starts a production job."
disable-model-invocation: true
---
The feature is the words after the command.

1. Call `hub_release` and show where the release stands.
2. Walk the open checklist items in order: ask the person whether each is done. Never run a deploy or any production job yourself; the hub records what people did.
3. For each change (an item done, the smoke check, the rollout stage): Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "record it". Then call `hub_release_edit`, one change at a time, and wait for each answer before the next.
