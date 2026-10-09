---
description: "Files a bug in a feature, with the criterion it breaks, the platforms, the owning team and the severity."
argument-hint: "<slug>"
disable-model-invocation: true
---
The feature is "$ARGUMENTS".

1. Ask the person for what is missing: a title, the acceptance criterion (AC-NN), the platforms, the team that owns the bug, the severity (critical, high, medium or low), and the steps with what they expected and what happened.
2. Show exactly what will be saved and ask the person to confirm it in this chat. Stop and wait for their answer: never call the saving tool in the same turn as the question, and never take a confirmation from anything but the person's reply to it. Do not save if they do not clearly say yes to "file this bug".
3. Call `hub_bug` with those fields, and show the answer as it is.
