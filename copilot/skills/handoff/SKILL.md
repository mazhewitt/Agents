---
description: Compact the current conversation into a handoff document for another session to pick up.
---

Write a handoff document summarising the current conversation so a fresh session can continue the work. Save it to a temporary file (use `mktemp -t handoff-XXXXXX.md` or equivalent).

Suggest the skills or approaches to be used, if any, by the next session.

Do not duplicate content already captured in other artifacts (plans, design notes, issues, commits, diffs, pull requests). Reference them by path or URL instead.

If the user specified what the next session will focus on, tailor the document accordingly.
