You are working in a personal second brain — a knowledge management system, not a code project. Your job is to keep the wiki current, useful, and well-organized based on the raw notes the user captures.

Read `README.md` first. This the source of truth for the system. This file gives you the additional context you need to do good work here.

---

## About the User

- **Name:** <change me>
- **Spitzname:** <change me>
- **Role:** <change me>
- **Topics I think about:** <change me>
- **Voice preference:** Sachlich korrekt, verständlich, ordentlich aber nicht spießig
- **Things I don't want in the wiki:** unwahrheiten, ungeprüftes, schwammige Aussagen

---

## Common Tasks

- **Translate raw** → run the prompt in `translate.md` against `/raw`.
- **Project digest** → summarize a `/projects/<name>/` folder into its README.
- **Answer questions** → read `/wiki` and `/archive` to answer ad-hoc questions about my own past thinking. If the answer surfaces something not yet in `/wiki` (a synthesis across entries, a fact only in `/archive`), merge it into the relevant wiki entry (or create one) using the same rules as `translate.md` — don't just answer in chat and let it evaporate.
- **Lint the wiki** → run the prompt in `lint.md` periodically to catch orphaned pages, index drift, contradictions, and stale claims.

---

## Hard Rules

1. **Never delete** anything from `/raw` or `/archive`. Move only, never delete.
2. **Never overwrite** a `/wiki` entry blindly. Always read it first, then merge.
3. **Never modify** `/archive` after a file lands there — it is a permanent record.
4. **Commit after meaningful changes** with a clear message (e.g. `translate: 4 inbox files processed`).
5. **When uncertain, log it in the entry** rather than guessing.
6. **Before creating or editing anything in `/raw`, `/wiki`, or `/projects`, `git fetch` and check for remote changes** — pull/rebase if origin has moved, so you start from a clean, current state. Repeat the check before pushing.
7. **Never let secrets — API keys, passwords, tokens, private keys or similar credentials — into the repo, wiki, or archive.** Check every commit for such content beforehand. If found: don't commit, report the finding in chat instead, and wait for the user to redact it.

   *(DE: Never let secrets — API-Keys, Passwörter, Tokens, private Schlüssel oder ähnliche Zugangsdaten — ins Repo, Wiki oder Archiv gelangen. Vor jedem Commit prüfen, ob solche Inhalte enthalten sind. Falls doch: nicht committen, den Fund stattdessen im Chat melden und auf Redaktion durch den User warten.)*

---

## Wiki Voice and Structure

- Default tone: clear, factual, terse.
- Default languarge: german
- Default timezone: Europe/Berlin
- Preserve my own phrasing when it carries signal — don't sand everything into neutral encyclopedia tone.
- Headings only when the entry is long enough to need them.
- Bullets only when the content is genuinely a list.
- One topic per file. Kebab-case filenames.

---

## Out of Scope

- Web browsing unless I explicitly ask.
- External API calls outside of declared automations.
- Anything touching accounts, payments, or auth.
- Editing files in `/raw` or `/archive`.
