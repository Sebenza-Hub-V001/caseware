---
title: "Claude Code + Obsidian — Ultimate Guide (AI Second Brain)"
type: entity
created: 2026-04-09
updated: 2026-04-09
tags: [tweets, ai, claude-code, obsidian, knowledge-management, wiki, second-brain]
sources: [aiedge-claude-code-obsidian-tweet]
status: active
confidence: medium
---

# Claude Code + Obsidian — Ultimate Guide (AI Second Brain)

## Tweet

> **AI Edge** (@aiedge_) — 8 April 2026
>
> Tweet body is a single link to an X Article:
>
> **"Claude Code + Obsidian Ultimate Guide (build an AI second brain)"**
>
> Preview: *"Claude Code + Obsidian is the most powerful AI combo I've ever used. I literally built an AI second brain that contains everything I think, read, write, research online, and more. It contains my…"*
>
> Source: [x.com/aiedge_/status/2041908011078447222](https://x.com/aiedge_/status/2041908011078447222)

> ⚠️ **Confidence: medium.** The linked X Article body could not be retrieved (requires authenticated session). The summary below draws on the tweet's preview text, the known `aiedge_` playbook from [[tweets/aiedge-claude-skills-guide]], and the broader "Claude Code + Obsidian second brain" pattern as documented by multiple contemporary guides. Update this page if the full article becomes available.

## Key Insight

**Claude Code + Obsidian is a file-system-native knowledge base for an AI agent.** The pattern is:

1. Keep everything as plain markdown in an Obsidian vault on disk.
2. Point Claude Code at the vault root.
3. Encode schema, conventions, and operations in a `CLAUDE.md` at the root.
4. Let the agent read, write, cross-link, and restructure pages directly via the file system — no RAG, no embeddings, no API retrieval workarounds.
5. Every new ingestion updates related pages or creates new ones, so the wiki self-evolves.

The result is an agent-native "second brain" where context lives in files rather than in model memory, and every session builds on the work of the last one.

## Probe Project Relevance

**Very high — we are already the reference implementation of this pattern.** The CaseWare Probe wiki is literally a Claude Code + Obsidian setup with:

- A vault of plain markdown files on disk
- A root `CLAUDE.md` that defines schema, directory layout, frontmatter rules, and the Ingest / Query / Lint / Evolve / Filing / Tweets operations
- An `index.md` catalog and a `log.md` append-only activity log
- `[[wiki-links]]` between every entity, concept, standard, working paper, source, and tweet
- Bidirectional cross-referencing as a hard rule
- Self-evolving behaviour on ingest — a new source touches multiple pages and spawns new ones

The tweet is reinforcement, not news. But it is useful as external validation of the architectural choices already baked into this repository, and the `aiedge_` author is the same person behind [[tweets/aiedge-claude-skills-guide]], whose Claude Skills guide we already treat as a primary methodology source. Pairing the two gives a coherent `aiedge_` stack: **Obsidian vault for memory + Claude Skills for repeatable capabilities.**

Compared to [[tweets/farzapedia-personal-wiki]], which establishes the wiki-as-agent-knowledge-base pattern from the *personal knowledge* angle, this tweet is the *Claude Code tooling* angle on the same idea — the two are complementary and both describe the architecture this project already uses.

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Pair Claude Code + Obsidian with the Skills layer.** The same author's [[tweets/aiedge-claude-skills-guide]] argues Skills are the productivity unlock; this tweet argues the vault is the memory. Treat them as one stack and make sure every Probe-specific skill references the vault paths it depends on (e.g. a "Visual Script Writer" skill should point at `2-working-papers/{phase}/{doc-folder}/`). | Low | High | [[tweets/aiedge-claude-skills-guide]], [[concepts/four-stage-pipeline]] |
| 2 | **Audit `CLAUDE.md` against the guide's "context lives in files" principle.** Our `CLAUDE.md` already encodes schema, operations, and filing rules. Review it to ensure nothing important is being deferred to model memory that should live in a file (e.g. domain glossaries, reviewer conventions, common pitfalls). | Low | Medium | [[CLAUDE]], [[concepts/four-stage-pipeline]] |
| 3 | **Add a `memory.md` or equivalent session-continuity page.** The broader Claude Code + Obsidian pattern uses a `memory.md` alongside `CLAUDE.md` to carry running context across sessions (decisions taken, open threads, current focus). We have `tasks/todo.md` and `tasks/lessons.md`, but no single "what the agent should remember about the current state of play" page. Consider either promoting `overview.md` into this role or adding a dedicated file. | Low | Medium | [[overview]], [[tasks/todo]], [[tasks/lessons]] |
| 4 | **Open the article.** This recommendation table is provisional until the full X Article is read. The author is already a trusted source on this project — fetch the article manually (authenticated session) and re-ingest so we can extract concrete setup steps, file conventions, and any tooling they use that we don't. | Low | Medium | this page, [[log]] |

## Open Questions

- What does the actual `aiedge_` vault structure look like? Does it match ours, or are there filing patterns worth copying?
- Does the guide recommend specific Obsidian plugins (Dataview, Templater, etc.) that would improve navigation of this wiki?
- Does the guide endorse a dedicated `memory.md` file, and if so, what belongs in it?

## Related

- [[tweets/aiedge-claude-skills-guide]] — same author, skills-layer companion to this tweet
- [[tweets/farzapedia-personal-wiki]] — the wiki-as-agent-knowledge-base pattern from the personal-notes angle
- [[tweets/coreyganim-claude-code-hidden-features]] — Claude Code tooling that slots into this stack
- [[tweets/nickspisak-claude-managed-agents]] — production deployment path for vault-scoped agents
- [[CLAUDE]] — the schema file that makes this vault agent-readable
- [[overview]] — current state of the Probe wiki
- [[concepts/four-stage-pipeline]] — the production workflow this architecture supports

- [[tweets/index]]

## References

- Raw: `raw/tweets/2026-04-08-aiedge-claude-code-obsidian-guide.md`
- Tweet: [x.com/aiedge_/status/2041908011078447222](https://x.com/aiedge_/status/2041908011078447222)
- Linked X Article: `x.com/i/article/2041263299497791488` ("Claude Code + Obsidian Ultimate Guide (build an AI second brain)")
