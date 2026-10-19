# ai-brain-vault

English | [简体中文](README.zh-CN.md)

A plain-Markdown template that gives your AI agents (Claude, Codex, Cursor, …) a **shared long-term memory and a set of working rules** — without the memory turning into a mess over time.

Drop it into an Obsidian vault (or any folder), fill in a few placeholders, and point your agents at it.

## Why

Most "AI memory" setups fail in one of three ways:

- **Amnesia** — every session starts from zero.
- **Bloat** — everything gets dumped into one giant file that is loaded every time, burning tokens and burying what matters.
- **Pollution** — the agent writes its guesses into memory, and they quietly become "facts".

This template is a small set of conventions that fixes all three.

## What you get

| Idea | How it works |
|---|---|
| **Triage gate** | The agent first decides whether a message is *work*. Only work loads memory. Personal questions get a normal answer, with no work context dragged in. |
| **Index-based memory** | `memory.md` is a tiny index + red lines (≤ 80 lines). Details live in topic files that are opened only when a task needs them. |
| **Two-tier writes** | Low-risk updates (project status, index lines) are written directly. High-risk ones (facts, rules, red lines, the constitution) are proposed first and written only after you approve. |
| **Session-end proposals** | After real work, the agent lists "things worth remembering" with a destination for each. Nothing is saved without your OK. |
| **One brain, many agents** | Claude, Codex and future tools all read the same files. No tool keeps its own copy of the facts. |
| **Inbox workflow** | Drop articles and screenshots into `inbox/`; the agent distills them into dated, sourced notes and files the originals away. |
| **Dated, sourced knowledge** | Every note carries `published_at` / `snapshot_at` / `content_status`, so agents can tell old evidence from current advice. |
| **Vault map** | `MAP.md` tells every agent what lives where and when to read it, so nothing is preloaded "just in case". |

## Structure

```
.
├── AGENTS.md              # Constitution: triage gate, identity, memory & knowledge rules
├── CLAUDE.md              # Thin entry point for Claude → points to AGENTS.md
├── memory.md              # Index + red lines (read every work session)
├── MAP.md                 # Map of the vault
├── memory/
│   ├── projects.md        # One line per project: where it's stuck, whose move
│   ├── projects/          # Full state of each project
│   ├── facts.md           # Durable hard facts (high-risk)
│   ├── rules.md           # Conventions + lessons learned (high-risk)
│   └── schedules.md       # Registry of scheduled agent tasks
├── knowledge/
│   ├── _index.md          # Index of all notes, with dates
│   └── sop/note-template.md
├── inbox/                 # New material waiting to be processed
└── logs/                  # Work logs + backups before risky changes
```

## Quick start

1. Click **Use this template** (or download the ZIP) and put the folder where you want your vault.
2. Search for `{{` and replace the placeholders — at minimum `{{OWNER_NAME}}`, `{{YOUR_WORK_DOMAIN}}` and `{{NORTH_STAR_GOAL}}` in `AGENTS.md`.
3. Edit the red lines in `memory.md` to match the things that would really hurt if an agent got them wrong.
4. Open the folder as a project in your agent:
   - **Claude** (Claude Code / Cowork): `CLAUDE.md` is picked up automatically.
   - **Codex** and other agents that read `AGENTS.md`: works as-is.
   - Anything else: add a two-line entry file that points to `AGENTS.md`.
5. Start working. After the first real session, accept or reject the agent's memory proposals — that is how the brain grows.

## Tips

- Keep `AGENTS.md` and `memory.md` short. They are loaded every session; everything else is loaded on demand.
- Each rule should live in exactly one file. Everywhere else, link to it.
- Once a month, ask your agent for a hygiene pass: size limits, broken links, duplicated rules, stale projects, index drift.
- Never put passwords, API keys or tokens in the vault.

## License

[MIT](LICENSE)
