---
title: "Claude + Obsidian Have to Be Illegal — Zero-Prompt Persistent Context"
type: entity
created: 2026-04-10
updated: 2026-04-10
tags: [tweets, ai, claude-code, obsidian, knowledge-management, wiki, second-brain, persistent-context]
sources: [defileo-claude-obsidian-tweet]
status: active
confidence: medium
---

# Claude + Obsidian Have to Be Illegal — Zero-Prompt Persistent Context

## Tweet

> **Defileo🔮** (@defileo) — 9 April 2026
>
> Tweet body is a single link to an X Article:
>
> **"Claude + Obsidian have to be illegal"**
>
> Preview: *"Claude + Obsidian should be illegal. Let me tell you what my setup does before I explain how to build it. Every morning I open my laptop, Before I type a single word, Claude already knows who I am,"*
>
> Engagement: 998 likes · 18 conversations
>
> Source: [x.com/defileo/status/2042241063612502162](https://x.com/defileo/status/2042241063612502162)

> ⚠️ **Confidence: medium.** The linked X Article body could not be retrieved (requires authenticated session). The analysis below draws on the tweet's preview text, the established Claude Code + Obsidian pattern from [[tweets/aiedge-claude-code-obsidian-guide]] and [[tweets/farzapedia-personal-wiki]], and the broader ecosystem of Claude + Obsidian guides. Update this page when the full article becomes available.

## Key Insight

**Persistent identity eliminates the daily "who am I" tax.** The core claim is a "zero-prompt morning" — a Claude + Obsidian setup where the agent has pre-loaded context about who the user is, what they're working on, and how they think, *before they type a single word*. The wow-factor is the elimination of session start-up friction: no re-explaining, no context dumping, no "here's what happened yesterday."

The mechanism is the same one documented across the growing Claude + Obsidian pattern:
- `CLAUDE.md` at the vault root encodes identity, conventions, and operations
- The vault's file structure (notes, logs, projects) acts as long-term memory
- Each session picks up where the last one left off by reading the file tree

What makes this tweet distinctive from [[tweets/aiedge-claude-code-obsidian-guide]] (architecture-focused) and [[tweets/farzapedia-personal-wiki]] (knowledge-base-focused) is its emphasis on the **user experience**: the feeling that the agent *knows you*.

## Probe Project Relevance

**High — and we're already most of the way there.** The Probe wiki has the structural ingredients for a zero-prompt session:

| What defileo describes | What we have | Gap |
|------------------------|-------------|-----|
| Agent knows who the user is on session start | `CLAUDE.md` encodes identity, schema, conventions | ✅ No gap — `CLAUDE.md` loads automatically |
| Agent knows what user is working on | `tasks/todo.md`, `2-working-papers/progress.md` | Partial — exists but not surfaced as first-read context |
| Agent remembers past sessions | `log.md` (append-only activity log) | Partial — log is chronological but not designed for quick session-start summary |
| Self-evolving: new inputs ripple across vault | Ingest operation updates 2–3+ pages per source | ✅ No gap |
| Zero-prompt morning | Must manually say "check todo" or "what's the status" | ❌ Gap — no auto-summary on session start |

The main gap is **session-start context**: we have the data (`log.md`, `tasks/todo.md`, `overview.md`) but no mechanism to surface it automatically when a new session begins. The agent reads `CLAUDE.md` on start but does not proactively check "what were we working on?"

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Add a `status.md` or `memory.md` session-start file.** A single page that is always kept current with: (a) current focus / active task, (b) last 3 log entries summarised, (c) blockers or decisions pending. Reference it from `CLAUDE.md` as a first-read file. This closes the "zero-prompt morning" gap. | Low | High | [[CLAUDE]], [[overview]], [[tasks/todo]] |
| 2 | **Add a session-start hook or instruction in `CLAUDE.md`.** Add an instruction like "On session start, read `status.md` and greet the user with a brief status update" so that the agent proactively surfaces context without being asked. | Low | High | [[CLAUDE]] |
| 3 | **Keep `status.md` updated automatically.** At the end of every Ingest, Filing, or Tweet operation, append a one-liner to `status.md` summarising what changed. This makes it a rolling "last session" summary that the next session can read instantly. | Low | Medium | [[CLAUDE]], [[log]] |
| 4 | **Retrieve the full article.** As with [[tweets/aiedge-claude-code-obsidian-guide]], the article body may contain concrete setup steps, file templates, or Obsidian plugin recommendations worth extracting. Fetch manually from an authenticated session and re-ingest. | Low | Medium | this page, [[log]] |

## Open Questions

- Does defileo's setup use a `memory.md` or similar session-start file, and what fields does it contain?
- Does the article recommend specific Obsidian plugins (Templater, Dataview, Periodic Notes) for maintaining the session-start context?
- How does the "knows who I am" framing differ from just having a `CLAUDE.md`? Is there an additional identity/profile file?

## Related

- [[tweets/aiedge-claude-code-obsidian-guide]] — architecture-layer companion (same pattern, focuses on vault structure + `CLAUDE.md`)
- [[tweets/aiedge-claude-skills-guide]] — skills-layer companion (vault = memory, skills = capabilities)
- [[tweets/farzapedia-personal-wiki]] — knowledge-base-layer companion (wiki as agent memory, self-evolving pages)
- [[tweets/coreyganim-claude-code-hidden-features]] — Claude Code tooling (hooks, `/loop`) that could power session-start automation
- [[CLAUDE]] — the schema file where session-start instructions would live
- [[overview]] — candidate for promotion to session-start context page

- [[tweets/index]]

## References

- Raw: `raw/tweets/2026-04-09-defileo-claude-obsidian-illegal.md`
- Tweet: [x.com/defileo/status/2042241063612502162](https://x.com/defileo/status/2042241063612502162)
- Linked X Article: `x.com/i/article/2041858771123617793` ("Claude + Obsidian have to be illegal")
