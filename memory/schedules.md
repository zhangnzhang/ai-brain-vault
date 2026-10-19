# Schedules — registry of scheduled agent tasks

> **Read this before creating any scheduled task** so you don't create a duplicate. Update it whenever a task is created, paused or removed.

| Task | Frequency (local time) | Cron | Task ID | Status / what it does |
|---|---|---|---|---|
| Inbox processing | Mondays 9:00 | `0 9 * * 1` | `{{id}}` | Running — processes `inbox/` into `knowledge/` |
| Monthly vault hygiene | 1st of month 9:00 | `0 9 1 * *` | `{{id}}` | Running — size limits, broken links, stale projects, index drift |
