# Lint Prompt

Read every file in `/wiki` (and `wiki/index.md`). Check for:

- **Orphaned pages** — no other wiki file links to it, and it's not linked from `index.md`.
- **Missing from index** — file exists in `/wiki` but has no line in `index.md`, or vice versa.
- **Contradictions** — two entries claim different things about the same fact.
- **Stale claims** — a claim that a later entry or archive file appears to supersede but the older wording wasn't updated.

Report findings in chat as a list (file, issue, suggested fix). Do not edit anything automatically — fixes go through the normal translate/merge flow so they get reviewed like any other wiki change.
