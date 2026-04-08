---
title: "20 Powerful Agentic Skills for Claude, ChatGPT & Gemini"
type: entity
created: 2026-04-07
updated: 2026-04-07
tags: [tweets, ai, claude-code, skills, agents, automation, productivity]
sources: [explorax-tweet]
status: active
---

# 20 Powerful Agentic Skills for Claude, ChatGPT & Gemini

## Tweet

> **m0h** (@exploraX_) — 1 April 2026
>
> [Link to article: "20 Powerful Agentic-Skills for Claude, ChatGPT & Gemini"]
>
> Curates 20 agentic skills in `.md` format (the standard for Claude) that can be added to any AI model to boost productivity. Includes a 94-second video guide on implementation.
>
> Engagement: 3,120 likes · 427 retweets · 39 replies · 3.58M views
>
> Source: [x.com/explorax_/status/2039269234253934811](https://x.com/explorax_/status/2039269234253934811)

## Key Insight

Agentic skills — packaged as `.md` files with structured instructions — turn general-purpose LLMs into specialised workers. By dropping a skill file into your agent's context, you effectively give it a new capability without code changes. The 20 skills span writing, visual design, research, and coding, and are designed to be model-agnostic (Claude, ChatGPT, Gemini).

## The 20 Skills

### Writing & Content (5 skills)

| # | Skill | What It Does |
|---|-------|-------------|
| 1 | SCQA Writing Framework | Structures writing using Situation–Complication–Question–Answer |
| 2 | Content Repurposing Engine | Transforms one piece of content into multiple formats |
| 3 | Tone & Style Enforcer | Maintains consistent voice across outputs |
| 4 | Long-Form to Summary Compressor | Distils long documents into concise summaries |
| 5 | Structured Copywriting Skill | Generates copy following proven copywriting frameworks |

### Visual & Infographic (4 skills)

| # | Skill | What It Does |
|---|-------|-------------|
| 6 | Excalidraw Diagram Generator | Creates hand-drawn-style diagrams |
| 7 | Infographic Builder | Produces data-driven visual layouts |
| 8 | Flowchart Decision Builder | Generates decision-tree flowcharts |
| 9 | UI/UX Layout Advisor | Reviews and suggests interface layouts |

### Research & Analysis (7 skills)

| # | Skill | What It Does |
|---|-------|-------------|
| 10 | Deep Research Synthesizer | Conducts multi-source research and synthesises findings |
| 11 | Onchain Transaction Analyzer | Analyses blockchain transactions |
| 12 | Source Validation Skill | Verifies claims against original sources |
| 13 | Competitive Intelligence Skill | Maps competitive landscape and positioning |
| 14 | Knowledge Structuring Skill | Organises unstructured information into frameworks |
| 15 | Video Script Generator | Creates scripts for video content |
| 16 | Video Editing Planner, Hook Generator, Caption & Subtitle Formatter | End-to-end video production planning |

### Coding & Automation (4 skills)

| # | Skill | What It Does |
|---|-------|-------------|
| 17 | Code Review Skill | Reviews code for quality, bugs, and best practices |
| 18 | Workflow Automation Agent | Designs and implements automated workflows |
| 19 | Skill Creator (Meta Skill) | Creates new agentic skills from natural language descriptions |
| 20 | DevOps Assistant | Manages deployment, CI/CD, and infrastructure tasks |

## Probe Project Relevance

**High relevance.** Several of these skills directly map to stages in the [[concepts/four-stage-pipeline]]:

- **Video Script Generator (#15)** — Stage 2 (Visual Script) requires converting How-To documents into presenter scripts. A dedicated skill could standardise and accelerate this conversion across all 57 working papers.
- **Video Editing Planner (#16)** — Stage 3–4 (Visual Recording → Professional Video) would benefit from structured editing plans, hook generation for video intros, and automated caption/subtitle creation.
- **Content Repurposing Engine (#2)** — The pipeline is inherently about repurposing: taking a CaseView PDF and producing a How-To doc, then a script, then a video. A skill tuned for this could reduce manual conversion effort.
- **Long-Form to Summary Compressor (#4)** — Could generate executive summaries of How-To documents for quick reference or for the [[entities/success-community]] platform.
- **Tone & Style Enforcer (#3)** — With 57 working papers being documented, maintaining consistent tone across all How-To documents and visual scripts is critical. This is already partly addressed by the [[concepts/ooxml-document-structure]] for formatting, but a tone/style skill would cover the writing itself.
- **Knowledge Structuring Skill (#14)** — Already effectively what the wiki does (this CLAUDE.md schema), but a dedicated skill could enhance how raw audit content is structured during ingestion.
- **Skill Creator / Meta Skill (#19)** — Could be used to create Probe-specific skills (e.g., a "CaseWare How-To Writer" skill or "ISA Standards Mapper" skill) tailored to the project's exact needs.

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Create a "Visual Script Writer" skill** — Package Stage 2 conversion rules (How-To → script) as an `.md` skill file. Include cues, transitions, metadata table format from existing scripts. | Medium | High | [[concepts/four-stage-pipeline]], [[2-working-papers/progress]] |
| 2 | **Create a "Tone & Style Enforcer" for Probe** — Define the project's writing voice (professional, instructional, concise) and formatting rules as a reusable skill to ensure consistency across 57 How-To docs. | Low | High | All working paper pages |
| 3 | **Adopt the "Skill Creator" pattern** — Use the meta-skill concept to generate project-specific skills as the pipeline matures (e.g., ISA mapper, CaseWare field describer, caption generator). | Low | Medium | [[concepts/four-stage-pipeline]] |
| 4 | **Explore caption/subtitle generation** — For Stage 4 videos, a caption formatter skill could automate transcript-to-subtitle conversion, improving accessibility of training videos on [[entities/success-community]]. | Medium | Medium | [[entities/success-community]], [[concepts/four-stage-pipeline]] |

## Open Questions

- Where are the actual `.md` skill files hosted? The tweet links to an X article but the skills likely live in a GitHub repo (possibly [Orchestra-Research/AI-Research-SKILLs](https://github.com/Orchestra-Research/AI-research-SKILLs) or [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)).
- Would Probe-specific skills be better as Claude Code skills (using the `/skill` format) or as standalone `.md` files in the wiki?

## Related

- [[concepts/four-stage-pipeline]] — the production workflow that several skills directly target
- [[2-working-papers/progress]] — tracking where skills could accelerate throughput
- [[entities/success-community]] — publishing platform that would benefit from caption/summary skills
- [[tweets/farzapedia-personal-wiki]] — related insight on wiki-as-knowledge-base for agents

## References

- Source: [x.com/explorax_/status/2039269234253934811](https://x.com/explorax_/status/2039269234253934811)
