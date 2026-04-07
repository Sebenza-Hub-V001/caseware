---
title: "Tweet Insights Index"
type: overview
created: 2026-04-07
updated: 2026-04-07
tags: [tweets, ai, insights, probe-project]
status: active
---

# Tweet Insights

> Ingested tweets and their implications for the Probe Project.

## How This Works

1. **Fetch** the tweet content
2. **Extract** the core insight
3. **Create** a tweet page in `tweets/` with:
   - Quoted tweet text
   - Key insight summary
   - **Probe Project relevance** — how it connects to existing How-To documents, visual scripts, videos, or the production pipeline
   - **Recommendations table** — specific, actionable improvements with effort/impact ratings and links to affected wiki pages
   - Skip justification if the tweet isn't relevant (no forced recommendations)
4. **Cross-reference** affected wiki pages if warranted
5. **Update** index.md and log.md

## Tweets

- [[tweets/farzapedia-personal-wiki]] — Personal wiki as agent knowledge base (Farza, 2026-04-04)

## Recommendation Summary

| # | From | Recommendation | Effort | Impact |
|---|------|---------------|--------|--------|
| 1 | [[tweets/farzapedia-personal-wiki]] | Add more unstructured sources (notes, meetings, learnings) | Low | Medium |
| 2 | [[tweets/farzapedia-personal-wiki]] | More aggressive auto-update on ingest across related pages | Medium | High |
| 3 | [[tweets/farzapedia-personal-wiki]] | Add visual/media tracking (screenshots, storyboards) | Medium | Medium |
| 4 | [[tweets/farzapedia-personal-wiki]] | Query-driven page creation in questions/ | Low | High |

## Related

- [[concepts/four-stage-pipeline]] — the production workflow recommendations may target
- [[working-papers/progress]] — current project status
