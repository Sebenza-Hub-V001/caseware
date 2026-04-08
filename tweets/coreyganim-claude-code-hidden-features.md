---
title: "Claude Code Hidden Features — 5 That Change Everything"
type: entity
created: 2026-04-08
updated: 2026-04-08
tags: [tweets, ai, claude-code, agents, automation, batch-processing, hooks, skills, productivity]
sources: [coreyganim-tweet]
status: active
---

# Claude Code Hidden Features — 5 That Change Everything

## Tweet

> **Corey Ganim** (@coreyganim) — 7 April 2026
>
> Me when I find out Claude Code has been hiding these features:
>
> 5 that change everything:
>
> 1. **Channels:** `claude --channels plugin:telegram` and now Claude is reachable by DM. CI fails at 2am, Claude diagnoses it and pings you the fix on Telegram. Reply "do it" and it's done.
>
> 2. **/batch:** One command spawns 5-30 parallel agents, each in its own git worktree. `/batch migrate src/ from Solid to React` and you get back a stack of PRs, not a 4000-line diff.
>
> 3. **Agent teams:** Teammates that talk to each other, not just to you. One finds a security issue, tells the architecture agent, devil's advocate pushes back. You watch and jump in when needed.
>
> 4. **TaskCompleted hook:** A shell script that vetoes Claude calling its own work "done." Tests still failing? Exit code 2 sends it back to work. Quality enforcement without you watching.
>
> 5. **/loop + skills:** `/loop 20m /simplify focus on auth module`. Every 20 minutes Claude runs your skill automatically. PR reviews, security checks, doc linting, all on a timer while you work.
>
> Full breakdown of all 10 features in the article.
>
> Engagement: 105 likes · 11 retweets · 265 bookmarks · 29K views
>
> Source: [x.com/coreyganim/status/2041596621591629915](https://x.com/coreyganim/status/2041596621591629915)

## Key Insight

Claude Code has advanced orchestration features that go far beyond single-agent prompting. The five highlighted here — **Channels**, **/batch**, **Agent teams**, **TaskCompleted hook**, and **/loop + skills** — collectively enable autonomous, quality-gated, parallelised workflows. The pattern is: give Claude Code not just tasks, but infrastructure to self-organise, self-check, and run continuously.

## Feature Breakdown

### 1. Channels (`--channels plugin:telegram`)

Claude Code becomes reachable via external messaging platforms (Telegram, Slack, etc.). Enables asynchronous human-in-the-loop workflows: Claude notifies you of problems, you approve fixes via DM reply.

### 2. /batch (Parallel Agent Worktrees)

Spawns 5-30 parallel agents, each in its own git worktree. A single command fans out work across multiple files or modules and returns a stack of focused PRs instead of a monolithic diff. Designed for large-scale migrations, refactors, and repetitive transformations.

### 3. Agent Teams (Multi-Agent Collaboration)

Agents that communicate laterally — not just with the user. Enables patterns like: finder agent → architecture agent → devil's advocate agent. The user observes and intervenes only when needed, rather than orchestrating every handoff.

### 4. TaskCompleted Hook (Quality Enforcement)

A shell script that intercepts Claude's "done" signal. If the hook returns a non-zero exit code (e.g., tests still failing), Claude is sent back to continue working. Automated quality gate without human monitoring.

### 5. /loop + Skills (Scheduled Automation)

Combines `/loop` (time-based scheduling) with skills (reusable instruction packages). Claude runs a specified skill at fixed intervals — PR reviews, security checks, doc linting, all on a timer while you work on other things.

## Probe Project Relevance

**Very high relevance.** Three of these five features directly address bottlenecks in the [[concepts/four-stage-pipeline]], and two align with recommendations already captured from prior tweets.

### /batch → Parallel Working Paper Processing

The Probe project has **57 working papers**, each progressing through the same four-stage pipeline. Currently each is processed sequentially. `/batch` could parallelise Stage 1 (How-To Doc) and Stage 2 (Visual Script) generation across multiple working papers simultaneously — e.g., `/batch generate visual scripts for all 02.xx finalisation papers`. This could compress weeks of sequential work into hours.

- Directly affects: [[2-working-papers/progress]], [[3-pipeline/index]]

### TaskCompleted Hook → Pipeline Quality Gates

This is the enforcement mechanism for the "Skills 2.0 evals as quality gates" recommendation from [[tweets/aiedge-claude-skills-guide]]. A `TaskCompleted` hook could verify:
- How-To documents meet [[concepts/ooxml-document-structure]] formatting standards
- Visual scripts include all required metadata (Video Details table, section transitions)
- ISA standard references are valid and cross-referenced against [[concepts/isa-standards]]
- No working paper wiki page is left without bidirectional links

If any check fails, Claude goes back and fixes it automatically — no human review needed for mechanical quality.

### /loop + Skills → Continuous Wiki & Pipeline Maintenance

Builds directly on recommendations from [[tweets/explorax-20-agentic-skills]] and [[tweets/aiedge-claude-skills-guide]]. Concrete applications:

- `/loop 30m /lint-wiki` — continuous wiki health checks (addresses issues in [[questions/wiki-health]])
- `/loop 1h /check-pipeline-progress` — automated progress tracking updates to [[2-working-papers/progress]]
- `/loop 20m /simplify focus on working-papers` — ongoing code/content quality passes

### Agent Teams → Review & Quality Assurance

A multi-agent review workflow for How-To documents:
- **Content agent** — generates the How-To document from the CaseView PDF
- **ISA compliance agent** — verifies all relevant ISA requirements from [[1-standards/2-isa/]] are addressed
- **Formatting agent** — checks [[concepts/ooxml-document-structure]] compliance
- **Devil's advocate agent** — challenges assumptions, flags gaps in practical guidance

This maps naturally to the Probe project's need for consistent quality across 57 documents produced by a small team.

### Channels → Pipeline Notifications (Lower Priority)

Less directly applicable, but could enable: when a `/batch` run of How-To document generation completes, Claude sends a Telegram message summarising results and requesting review. Useful once the pipeline is more automated.

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Use `/batch` for parallel Stage 1→2 generation** — batch-process visual scripts for completed How-To documents across an entire audit phase at once, instead of one at a time. | Medium | Very High | [[concepts/four-stage-pipeline]], [[2-working-papers/progress]], [[3-pipeline/index]] |
| 2 | **Implement a `TaskCompleted` hook for pipeline quality gates** — enforce OOXML formatting, ISA cross-referencing, and wiki link completeness before any stage is marked done. | Medium | High | [[concepts/ooxml-document-structure]], [[concepts/isa-standards]], [[concepts/four-stage-pipeline]] |
| 3 | **Set up `/loop` with wiki lint skill** — run automated wiki health checks on a timer to catch orphan pages, broken links, and stale content continuously. | Low | High | [[questions/wiki-health]], [[tweets/index]] |
| 4 | **Design agent team workflow for How-To document review** — content + ISA compliance + formatting agents reviewing each other's work reduces human review burden across 57 documents. | High | Very High | All working paper pages, [[concepts/four-stage-pipeline]] |
| 5 | **Combine `/batch` + `TaskCompleted` hook** — batch-generate documents with automatic quality enforcement, so only compliant outputs are accepted. | High | Very High | [[concepts/four-stage-pipeline]], [[3-pipeline/index]] |

## Open Questions

- Does `/batch` support custom per-agent instructions, or does each agent get the same prompt? If custom, each working paper could receive its specific CaseView PDF as context.
- Can `TaskCompleted` hooks call external validators (e.g., a Python script checking OOXML structure), or are they limited to shell commands?
- Is there a practical upper limit on `/batch` parallelism? 57 simultaneous agents may hit resource constraints.
- How do agent teams share state — through files, or through a message-passing protocol?

## Related

- [[tweets/aiedge-claude-skills-guide]] — how to build the skills that `/loop` would run; Skills 2.0 evals = the logical precursor to `TaskCompleted` hooks
- [[tweets/explorax-20-agentic-skills]] — the 20 skills that could be scheduled via `/loop`; Visual Script Writer skill is prime `/batch` candidate
- [[tweets/farzapedia-personal-wiki]] — wiki-as-knowledge-base pattern; `/loop /lint-wiki` keeps it healthy automatically
- [[concepts/four-stage-pipeline]] — the production workflow that `/batch` and agent teams could accelerate
- [[concepts/ooxml-document-structure]] — formatting standards a `TaskCompleted` hook should enforce
- [[concepts/isa-standards]] — ISA compliance checks for agent team review workflow
- [[2-working-papers/progress]] — current pipeline status that `/batch` could accelerate
- [[3-pipeline/index]] — pipeline dashboard affected by batch processing
- [[questions/wiki-health]] — wiki health issues that `/loop /lint` would address

- [[tweets/index]]

## References

- Source: [x.com/coreyganim/status/2041596621591629915](https://x.com/coreyganim/status/2041596621591629915)
