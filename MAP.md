# MAP — map of the whole vault

> Every agent skims this before starting work: what lives where and when to read it. **Read on demand; never preload.**
> Whoever adds, moves or removes a file updates this map in the same change.

## Inside the vault

| Location | What it is | When to read |
|---|---|---|
| `AGENTS.md` | Constitution: triage gate, identity, memory rules, knowledge rules, tool differences | Every session |
| `CLAUDE.md` | Thin entry point that points to `AGENTS.md` | Loaded automatically by Claude |
| `memory.md` | Memory index + 🔴 red lines | Every work session |
| `memory/projects.md` | Project index: one line per project (where it's stuck + whose move) | When pushing or checking a project |
| `memory/projects/<project>.md` | Full state, open items and decision log of one project | Read **one** after locating it in the index |
| `memory/facts.md` | Durable hard facts | When writing external content or doing numbers |
| `memory/rules.md` | Conventions + lessons | When writing, editing skills, auditing |
| `memory/schedules.md` | Scheduled task registry | Before creating a scheduled task |
| `knowledge/_index.md` | Index of all knowledge notes, grouped by topic, with dates | Before any advice based on the knowledge base |
| `knowledge/sop/note-template.md` | Front matter schema and note template | When adding a new note |
| `inbox/` | New material waiting to be processed | When asked to "process the inbox" |
| `logs/` | Agent work logs + pre-change backups | To check "what happened last time" or to roll back |

## Outside the vault

| Location | What it is | Notes |
|---|---|---|
| `{{PATH_TO_YOUR_WORKSHOP}}` | Workshop: drafts, code, exports, deliverables | The brain stores distilled lessons; raw files stay here |

## Known gaps / to-do

- [ ] {{e.g. "knowledge/_archive/ not created yet — create it the first time a note becomes outdated"}}

*Created {{DATE}}.*
