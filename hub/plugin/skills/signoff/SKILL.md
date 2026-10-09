---
description: "Records your sign-off of a step's gate through a merge request in your name."
argument-hint: "<step> <slug>"
disable-model-invocation: true
---
The arguments are "$ARGUMENTS": the step, then the feature slug.

1. Call `hub_status` for the feature and show where it is, so the person sees what they sign.
2. Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "sign off <step> of <slug>".
3. Call `hub_signoff` with the step and the slug, and show the answer as it is. The sign-off merges by itself when hub-guard passes.
