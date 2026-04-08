---
title: "Farzapedia — Personal Wiki as Agent Knowledge Base"
type: entity
created: 2026-04-07
updated: 2026-04-07
tags: [tweets, ai, knowledge-management, wiki, agents, claude-code]
sources: [farzapedia-tweet]
status: active
---

# Farzapedia — Personal Wiki as Agent Knowledge Base

## Tweet

> **Farza** (@FarzaTV) — 4 April 2026
>
> "This is Farzapedia. I had an LLM take 2,500 entries from my diary, Apple Notes, and some iMessage convos to create a personal Wikipedia for me. It made 400 detailed articles for my friends, my startups, research areas, and even my favorite animes and their impact on me complete with backlinks. But, this Wiki was not built for me! I built it for my agent! The structure of the wiki files and how it's all backlinked is very easily crawlable by any agent + makes it a truly useful knowledge base. I can spin up Claude Code on the wiki and starting at index.md (a catalog of all my articles) the agent does a really good job at drilling into the specific pages on my wiki it needs context on when I have a query..."
>
> Source: [x.com/farzatv/status/2040563939797504467](https://x.com/farzatv/status/2040563939797504467)

## Key Insight

A personal wiki structured with interlinked markdown files and an `index.md` catalog is **far more effective than RAG** as a knowledge base for AI agents. The file-system structure with backlinks is "easily crawlable" by agents like Claude Code. The wiki also **self-maintains** — when new content is added, the system automatically updates 2–3 related articles or creates new ones.

## Probe Project Relevance

This is directly relevant — **we are already doing this**. The CaseWare Probe wiki follows the exact same architecture Farza describes:

- `index.md` as the entry point catalog (we have this)
- Interlinked markdown pages with `[[wiki-links]]` (we have this)
- Agent-driven ingestion that creates and updates multiple pages per source (we do this)
- Structured directories for different content types (we have this)

The Probe wiki is essentially a domain-specific version of Farzapedia, focused on audit methodology rather than personal knowledge. The key difference is Farza built his from unstructured personal notes, while ours is built from structured professional documents (CaseView PDFs, IAASB Handbook, project plans).

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Add more unstructured sources** — Farza's system thrives on diverse inputs (diary, notes, messages). Consider ingesting informal notes, meeting minutes, audit learnings, or client interaction summaries into the wiki. | Low | Medium | [[2-working-papers/progress]], [[tasks/lessons]] |
| 2 | **Auto-update on ingest** — We already do this (updating 2–3 pages when a new source arrives), but could be more aggressive about cross-referencing. When a new How-To draft is added, automatically check all related standards pages and working paper pages for updates. | Medium | High | [[concepts/four-stage-pipeline]], all working paper pages |
| 3 | **Add visual/media tracking** — Farza tracks images and inspiration. For the Probe Project, this could mean tracking screenshots of CaseWare screens, video thumbnails, or visual script storyboards as wiki-linked assets. | Medium | Medium | [[raw/screenshots/]], [[concepts/four-stage-pipeline]] |
| 4 | **Query-driven page creation** — Farza uses his wiki to answer complex queries that span multiple topics. Consider creating a `questions/` workflow where audit questions are filed, answered from wiki content, and the answers themselves become reusable pages. | Low | High | [[questions/wiki-health]] |

## Related

- [[concepts/four-stage-pipeline]] — our production pipeline that benefits from this approach
- [[2-working-papers/progress]] — the structured content this wiki tracks

- [[tweets/index]]

## References

- Raw: `raw/tweets/2026-04-04-farzapedia-personal-wiki.md`
