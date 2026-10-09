---
name: hub-validate
description: "Checks the documents downstream of a feature's spec against it after a change, and reports. Changes nothing."
---
The feature is the words after the command. Read only: edit no file.

1. Read `docs/features/<slug>/spec.md` and its stories (US-NN) and criteria (AC-NN).
2. Read each document that exists downstream: ux-flows.md, screens.md, test-plan.md, sad.md, data-model.md and contracts/ in the same folder.
3. For each document, check every reference to a story, criterion or screen against the spec: missing, changed or no longer existing.
4. Answer with the report only, in Markdown: a `## <file>` heading per document, then `Consistent.` or a list of `- Conflict: <what> Proposed fix: <how>`.
5. In an interactive session, ask whether to save the report; if the person says yes, call `hub_validation` with it. In a headless run, end with the report.
