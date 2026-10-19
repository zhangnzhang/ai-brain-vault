# Memory — index

> **This file is an index, not a warehouse.** Read it at the start of every work session; follow the index to `memory/` for details.
> **Hard limit: 5 KB / 80 lines.** Only two things belong here: ① red lines ② one-line index entries.
> New content → the matching topic file, then update its index line here. **Don't expand details in this file.**

---

## 🔴 Red lines (breaking these breaks real things — obey unconditionally)

<!-- Keep this list short. A red line is a rule where a mistake is expensive or irreversible.
     Replace the examples below with your own. -->

1. **"Can we do X?" = plan and feasibility only.** Act only on an explicit "do / change / write".
2. **Never overwrite a file without reading its current version first** — another session may have changed it.
3. **Never touch production directly.** Example: copy → change the copy → the owner reviews and publishes.
4. **Deleting, publishing, sending, paying, granting access or changing security settings always needs explicit confirmation first.**
5. {{YOUR_RED_LINE}}

---

## 📇 Index — topic files (read on demand, not every session)

| File | What's inside | When to read |
|---|---|---|
| `memory/projects.md` | Project index: one line per active project (details in `memory/projects/<project>.md`) | When pushing or checking a project |
| `memory/facts.md` | Durable hard facts about your work | When writing external content, doing numbers, editing core data |
| `memory/rules.md` | Working conventions + lessons learned (non-red-line) | When writing, editing skills, auditing |
| `memory/schedules.md` | Registry of scheduled agent tasks | **Before creating any new scheduled task** (avoid duplicates) |

---

*Created {{DATE}}.*
