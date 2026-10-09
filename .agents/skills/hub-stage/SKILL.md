---
name: hub-stage
description: "Runs one stage of the plain engine for a feature: the prompt in .hub/engines/plain/<stage>.md. hub_next hands it over."
---
The arguments are the words after the command: the stage, then the feature slug.

Read `.hub/engines/plain/<stage>.md` and follow it for that feature: `<slug>` in the prompt is the feature's slug. Write only the files it names. If there is no such prompt, say so and stop.
