# AI Edge Tweet — Claude Code + Obsidian Ultimate Guide — Raw Content

> Source: https://x.com/aiedge_/status/2041908011078447222
> Author: AI Edge (@aiedge_)
> Date: 2026-04-08T15:56:21Z
> Media: 1 image (1668x667)

## Tweet Text

The tweet body is a single short-link to an attached X Article.

Linked article (X Article ID 2041263299497791488):

> **Title:** Claude Code + Obsidian Ultimate Guide (build an AI second brain)
>
> **Preview:** "Claude Code + Obsidian is the most powerful AI combo I've ever used. I literally built an AI second brain that contains everything I think, read, write, research online, and more. It contains my..."

## Notes

- Article body could not be retrieved — X Articles require an authenticated session.
- Corroborating context from web search on the topic (not from this specific article, but from the broader "Claude Code + Obsidian second brain" pattern that the article is part of) indicates the common playbook is:
  - Obsidian vault as a folder of plain markdown files on disk (local-first, no RAG, no API calls for retrieval)
  - Claude Code reads/writes the vault directly via the file system
  - A `CLAUDE.md` at the vault root encodes conventions, schema, and operations
  - The wiki "self-evolves": ingesting a new source updates 2–3 related pages or creates new ones
  - Context lives in files, not in model memory — sessions build on prior work through the file tree
