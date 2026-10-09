---
description: "Sends a step back instead of signing it off, with your reason, through a merge request in your name."
argument-hint: "<step> <slug> <reason>"
disable-model-invocation: true
---
The arguments are "$ARGUMENTS": the step, the feature slug, then the reason.

1. If the reason is missing, ask the person what has to change. Use their words.
2. Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "return <step> of <slug>" with the reason.
3. Call `hub_return` with the step, the slug and the reason, and show the answer as it is.
