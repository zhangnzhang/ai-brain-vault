---
title: Note template and front matter schema
source: this vault
source_type: sop
published_at: unknown
snapshot_at: YYYY-MM-DD
content_status: current
tags: [sop, template]
---

> Summary: every knowledge note uses this front matter, a one-sentence summary, then the body — so agents can judge source, freshness and relevance before reading the whole thing.

## Front matter fields

| Field | Meaning | Example |
|---|---|---|
| `title` | Human-readable title | `Checkout page best practices` |
| `source` | Where it came from (URL, book, person, "own experiment") | `https://example.com/article` |
| `source_type` | `article` / `research` / `case-study` / `own-data` / `sop` / `reference` / `notes` | `research` |
| `published_at` | When the source was published (`unknown` if not known) | `2025-03-14` |
| `snapshot_at` | When it was captured into this vault | `2026-01-02` |
| `content_status` | `current` / `outdated` / `disputed` | `current` |
| `tags` | Free tags for search | `[checkout, ux]` |

## Why two dates

`published_at` tells you how old the *claim* is; `snapshot_at` tells you when *you* captured it. A 2019 statistic captured last week is still a 2019 statistic.

## Template

```markdown
---
title:
source:
source_type:
published_at:
snapshot_at:
content_status: current
tags: []
---

> Summary: one sentence on what this note says and when it is useful.

## Key points
- Keep numbers, percentages and source links exactly as in the original.

## Notes / caveats
- Sample size, context, anything that limits how far this generalizes.
```
