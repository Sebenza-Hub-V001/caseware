---
title: "Claude Cowork as Chief of SEO — 20-Prompt Audit System (Sarvesh Shrivastava)"
type: entity
created: 2026-04-12
updated: 2026-04-12
tags: [tweets, ai, claude-cowork, prompt-library, context-loading, seo, off-domain]
sources: [bloggersarvesh-claude-cowork-seo-tweet]
status: active
confidence: medium
---

# Claude Cowork as Chief of SEO — 20-Prompt Audit System

## Tweet

> **Sarvesh Shrivastava** (@bloggersarvesh) — 25 March 2026
>
> Tweet body is a single link to an X Article:
>
> **"My Chief of SEO, Claude Cowork"**
>
> Preview: *"I've built a 20-part prompt system inside Claude Cowork that audits your entire Google presence, finds every gap your competitors are exploiting, and hands you a ranked execution plan. Claude Cowork is now my Chief of SEO."*
>
> Source: [x.com/bloggersarvesh/status/2036795618090520592](https://x.com/bloggersarvesh/status/2036795618090520592)

> ⚠️ **Confidence: medium.** The X Article body could not be retrieved directly (authenticated-session wall). The summary below draws on the tweet preview metadata from the X syndication API and on corroborating coverage of Shrivastava's "Claude Cowork SEO" playbook across related tweets and third-party write-ups. Update this page if the full article becomes available.

## Key Insight

**The real innovation is not the SEO prompts — it's the workspace architecture.** Shrivastava treats Claude Cowork as a context-loaded project where all stable reference data is uploaded once and every task-specific prompt is a thin file in a "prompt library" that assumes that context is already present.

The pattern, stripped of the SEO domain:

1. **Context files loaded once, never repeated.** Business identity, competitor list, Google Business Profile details, target keywords — all live as files in the Cowork project, so every prompt starts with the same background.
2. **Competitor files as first-class inputs.** One file per competitor means every audit prompt can implicitly run comparative analysis without re-specifying targets.
3. **Prompt library of one-file-per-task.** Twenty focused prompts, each one a single markdown file, each one implicitly "knowing" the business because of (1).
4. **Ranked execution plan as the canonical output shape.** Every prompt is instructed to return a prioritised spreadsheet of specific actions sorted by impact — not prose, not vague advice.
5. **The agent is framed as a named role.** "Chief of SEO" is not just marketing — it's a discipline: the agent stays in character, so every output has a consistent voice and decision lens.

The SEO content itself is out of scope for this wiki. The architecture is what transfers.

## Probe Project Relevance

**Moderate — off-domain but architecturally aligned.** SEO/GBP audits have nothing to do with CaseWare Probe, ISA standards, or audit working papers, so there is no content reuse here. But the **Cowork-as-prompt-library pattern maps cleanly onto how we already work**:

- Our `CLAUDE.md` + the working paper document folder structure (`2-working-papers/{phase}/{doc-folder}/`) is our version of "load context once, never repeat." Each folder already bundles the CaseView source, the How-To draft, and the wiki page in one place so any prompt scoped to that folder implicitly knows the document.
- Our planned Skills layer (see [[tweets/aiedge-claude-skills-guide]] and [[tweets/explorax-20-agentic-skills]]) is our version of the "one-file-per-task prompt library."
- What we **don't yet have** is Shrivastava's discipline of *writing every prompt to assume the context is already loaded* and *forcing every output into a ranked-execution-plan shape*. Our tweet-derived recommendation tables (effort × impact) are close to the ranked-execution-plan format, but we don't apply it consistently to pipeline outputs themselves.

Compared to neighbouring tweets:

- [[tweets/aiedge-claude-code-obsidian-guide]] makes the same "context lives in files" argument from the Claude Code + Obsidian angle. Shrivastava is making it from the Claude Cowork (hosted Projects) angle. Both are compatible — the vault is the source of truth, Cowork is an alternative surface for running prompts against parts of it.
- [[tweets/nickspisak-claude-managed-agents]] is the production-deployment version of the same idea: load context into an agent, give it a role, run repeatable tasks.
- [[tweets/explorax-20-agentic-skills]] and [[tweets/aiedge-claude-skills-guide]] cover the "one-file-per-task" side from the Skills angle.

This tweet is the **role + context-loading + output-shape** angle on the same stack, applied to a completely unrelated domain. That makes it useful precisely because it's off-domain: it confirms the architecture generalises.

## Recommendations

| # | Recommendation | Effort | Impact | Affected Pages |
|---|---------------|--------|--------|---------------|
| 1 | **Write Probe skills to assume the working paper folder context is pre-loaded.** Every skill we build for the pipeline (Visual Script Writer, How-To Formatter, Wiki Page Generator) should explicitly state in its description that the current working paper folder — with CaseView source, draft, and wiki page — is its input, rather than re-specifying it per invocation. This is Shrivastava's "context loaded once, never repeated" rule applied to our folder convention. | Low | Medium | [[concepts/four-stage-pipeline]], [[tweets/aiedge-claude-skills-guide]] |
| 2 | **Adopt a "ranked execution plan" output contract for pipeline skills.** Where a skill is producing review output, reviewer feedback, or next-action suggestions, force it to emit a prioritised table (action, rationale, effort, impact) instead of prose. This is already the shape we use for tweet recommendation tables — push it downstream into the pipeline itself, so reviewers of a How-To draft get a ranked punch list, not a paragraph. | Low | Medium | [[2-working-papers/progress]], [[3-pipeline/index]] |
| 3 | **Consider named "role" framing for the main Probe skills.** "Chief of SEO" is a framing trick but a useful one — naming an agent role makes its decision lens consistent across runs. Candidate roles for the Probe pipeline: *Methodology Reviewer*, *ISA Compliance Checker*, *Visual Script Director*. Low-cost naming convention change, not new infrastructure. | Low | Low | [[concepts/four-stage-pipeline]], [[tweets/explorax-20-agentic-skills]] |
| 4 | **Retrieve the full article once an authenticated session is available.** The concrete prompt structure, file-loading conventions, and any tooling specifics are behind the X Article wall. Re-ingest when retrievable. | Low | Low | this page, [[log]] |

No SEO-specific recommendations — the domain is not in scope for CaseWare Probe.

## Open Questions

- What exact directory / file conventions does Shrivastava use inside Claude Cowork for the context files and prompt library? Are there naming rules we could borrow?
- Does the 20-prompt system have a "meta" prompt that composes the others, or are they all run independently? Our pipeline currently runs stages independently — a meta-orchestrator would be a candidate pattern if the article endorses one.
- Does the "ranked execution plan" output include estimated effort alongside impact? Our recommendation tables do; it would be nice to confirm alignment.

## Related

- [[tweets/aiedge-claude-code-obsidian-guide]] — "context lives in files" from the Claude Code + Obsidian angle (same idea, different surface)
- [[tweets/aiedge-claude-skills-guide]] — the Skills layer that implements the "one-file-per-task prompt library" discipline
- [[tweets/explorax-20-agentic-skills]] — 20 agentic skills in markdown, the closest direct analogue to Shrivastava's 20-prompt library
- [[tweets/nickspisak-claude-managed-agents]] — production deployment of context-loaded, role-scoped agents
- [[tweets/farzapedia-personal-wiki]] — the personal-wiki-as-agent-knowledge-base pattern, same family of ideas
- [[concepts/four-stage-pipeline]] — where the "assume context is loaded" discipline would apply
- [[CLAUDE]] — the schema file that defines our context-loading conventions

- [[tweets/index]]

## References

- Raw: `raw/tweets/2026-03-25-bloggersarvesh-claude-cowork-seo.md`
- Tweet: [x.com/bloggersarvesh/status/2036795618090520592](https://x.com/bloggersarvesh/status/2036795618090520592)
- Linked X Article: `x.com/i/article/2036485396385890304` ("My Chief of SEO, Claude Cowork")
- Related post (same author, same playbook): [x.com/bloggersarvesh/status/2042232870891340012](https://x.com/bloggersarvesh/status/2042232870891340012)
