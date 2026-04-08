---
title: "Tweet Insights Index"
type: overview
created: 2026-04-07
updated: 2026-04-08
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

- [[tweets/aiedge-claude-skills-guide]] — Ultimate guide to building and optimising Claude Skills (AI Edge, 2026-03-25)
- [[tweets/explorax-20-agentic-skills]] — 20 agentic skills in .md format for Claude, ChatGPT & Gemini (m0h, 2026-04-01)
- [[tweets/farzapedia-personal-wiki]] — Personal wiki as agent knowledge base (Farza, 2026-04-04)
- [[tweets/coreyganim-claude-code-hidden-features]] — 5 hidden Claude Code features: /batch, agent teams, TaskCompleted hook, /loop + skills, channels (Corey Ganim, 2026-04-07)

## Recommendation Summary

| # | From | Recommendation | Effort | Impact |
|---|------|---------------|--------|--------|
| 1 | [[tweets/aiedge-claude-skills-guide]] | Follow 4-step build process for Probe skills (use Skill-Creator) | Low | High |
| 2 | [[tweets/aiedge-claude-skills-guide]] | Apply reverse prompting when building Probe-specific skills | Low | Medium |
| 3 | [[tweets/aiedge-claude-skills-guide]] | Use Skills 2.0 evals as quality gates for pipeline stages | Medium | High |
| 4 | [[tweets/explorax-20-agentic-skills]] | Create a "Visual Script Writer" skill for Stage 2 pipeline | Medium | High |
| 2 | [[tweets/explorax-20-agentic-skills]] | Create a "Tone & Style Enforcer" for Probe consistency | Low | High |
| 3 | [[tweets/explorax-20-agentic-skills]] | Adopt the "Skill Creator" meta-pattern for project-specific skills | Low | Medium |
| 4 | [[tweets/explorax-20-agentic-skills]] | Explore caption/subtitle generation for Stage 4 videos | Medium | Medium |
| 8 | [[tweets/farzapedia-personal-wiki]] | Add more unstructured sources (notes, meetings, learnings) | Low | Medium |
| 9 | [[tweets/farzapedia-personal-wiki]] | More aggressive auto-update on ingest across related pages | Medium | High |
| 10 | [[tweets/farzapedia-personal-wiki]] | Add visual/media tracking (screenshots, storyboards) | Medium | Medium |
| 11 | [[tweets/farzapedia-personal-wiki]] | Query-driven page creation in questions/ | Low | High |
| 12 | [[tweets/coreyganim-claude-code-hidden-features]] | Use `/batch` for parallel Stage 1→2 generation across audit phases | Medium | Very High |
| 13 | [[tweets/coreyganim-claude-code-hidden-features]] | Implement `TaskCompleted` hook for pipeline quality gates | Medium | High |
| 14 | [[tweets/coreyganim-claude-code-hidden-features]] | Set up `/loop` with wiki lint skill for continuous health checks | Low | High |
| 15 | [[tweets/coreyganim-claude-code-hidden-features]] | Design agent team workflow for multi-agent How-To document review | High | Very High |
| 16 | [[tweets/coreyganim-claude-code-hidden-features]] | Combine `/batch` + `TaskCompleted` hook for quality-gated batch generation | High | Very High |

## Related

- [[concepts/four-stage-pipeline]] — the production workflow recommendations may target
- [[2-working-papers/progress]] — current project status
