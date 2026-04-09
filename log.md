# Activity Log

## [2026-04-09] tweet | Nick Spisak — Claude Managed Agents: Deploy Your First One in Under 10 Minutes
- Source: https://x.com/NickSpisak_/status/2041949191887262164
- Tweet page: [[tweets/nickspisak-claude-managed-agents]]
- Raw: `raw/tweets/2026-04-08-nickspisak-claude-managed-agents.md`
- Key insight: Claude Managed Agents is Anthropic's hosted platform for production agents — four primitives (Agent, Environment, Session, Events), built-in tool execution, per-tool permission scoping (`always_allow` / `always_ask`), MCP connectivity, and a one-command Claude Code onboarding (`start onboarding for managed agents in Claude API`). Pricing is Claude API token rates + $0.08 per session-hour.
- Relevance: Very high — replaces the local Claude Code + custom hooks automation pattern (see coreyganim tweet) with a managed platform; enables phase-scoped and document-scoped agents for the Probe pipeline; `always_ask` is a native quality gate
- Recommendations: 5 (run onboarding, phase-scoped agents, always_ask gates, document-scoped pilot agent, session-hour cost model)
- Pages touched: [[tweets/index]], [[index]], [[log]]

## [2026-04-08] tweet | RoundtableSpace — The Most Important Prompt for Debugging
- Source: https://x.com/RoundtableSpace/status/2035631314691387534
- Tweet page: [[tweets/roundtablespace-debugging-prompt]]
- Key insight: Structured 8-step debugging methodology (understand → hypothesise → isolate → verify → fix minimally → test → prevent → reason like a detective) with explicit rules against hallucination and premature solutions
- Relevance: Moderate — debugging skill applicable to pipeline automation errors; "verify before fixing" principle maps to TaskCompleted hook design
- Recommendations: 2 (Pipeline Debugger skill, verify-before-fixing in TaskCompleted hooks)
- Pages touched: [[tweets/index]], [[index]], [[log]]

## [2026-04-08] audit | Welcome.md — Remove Sebenza Hub references
- File: [[Welcome]]
- Issue: Welcome page title and heading referenced "Sebenza Hub" instead of the CaseWare Probe Project
- Fix: Changed frontmatter title and `#` heading from "Welcome to Sebenza Hub" to "Welcome to CaseWare Probe Project"
- No other files in the vault contained Sebenza Hub references

## [2026-04-08] tweet | Corey Ganim — Claude Code Hidden Features (5 That Change Everything)
- Source: https://x.com/coreyganim/status/2041596621591629915
- Tweet page: [[tweets/coreyganim-claude-code-hidden-features]]
- Key insight: Claude Code has advanced orchestration features — /batch (parallel agents in worktrees), agent teams (lateral agent communication), TaskCompleted hook (quality gates), /loop + skills (scheduled automation), and channels (messaging platform integration)
- Relevance: Very high — /batch could parallelise working paper processing across 57 documents; TaskCompleted hook is the enforcement mechanism for pipeline quality gates; /loop enables continuous wiki health checks
- Recommendations: 5 (batch processing for pipeline stages, TaskCompleted quality gates, /loop wiki linting, agent team review workflow, combined batch + hook pattern)
- Pages touched: [[tweets/index]], [[index]], [[log]]

## [2026-04-08] ingest | Project Plan CSV — Full Spreadsheet Import
- Source: `raw/project-plans/probe-project-plan-2025.csv`
- New page: [[3-pipeline/project-plan-tracker]] — Full detailed tracker with all 31 columns from master CSV
- Organised by audit phase (5 sections) with sub-tables per pipeline stage (4 stages)
- Includes team assignments summary and key deadlines table
- Pages touched: [[3-pipeline/index]], [[index]]
- Cross-referenced: [[2-working-papers/progress]], [[concepts/four-stage-pipeline]], [[sources/probe-project-plan-2025]]

## [2026-04-08] restructure | CaseWare Document Manager subfolder structure
- Mirrored CaseWare Document Manager hierarchy into `2-working-papers/` and `raw/` directories
- Created subfolders: `finalisation/`, `pre-engagement-planning/`, `planning-risk-assessment/`, `audit-planning/`, `general-working-papers/`, `leadsheets/` (with 7 subsections)
- Moved 39 wiki pages, 41 CaseView PDFs, 23 How-To V5 drafts into correct subfolders
- Updated 345 wiki links + 127 raw artifact links across 93 files
- Empty `leadsheets/` subfolders created for future content (300-900 series)
- Document map saved to memory for future upload routing

## [2026-04-08] restructure | Lifecycle folder layout
- Renamed `standards/` → `1-standards/` (50 standard pages)
- Renamed `working-papers/` → `2-working-papers/` (39 working paper pages)
- Created `3-pipeline/` with [[3-pipeline/index]] — production pipeline dashboard
- Removed empty folders: `comparisons/`, `decisions/`, `presentations/`, `procedures/`
- Removed junk files: `2026-04-06.md`, `Untitled.base`, `README.md`
- Rewrote [[Welcome]] as project hub page
- Updated ~650 wiki links across all files
- Reorganised [[index]] to follow audit lifecycle flow: Standards → Working Papers → Pipeline → Reference → Research

## [2026-04-07] update | Added Presentations folder
- Created `presentations/` directory for presentation materials
- Updated [[index]] with new Presentations section
- Pages touched: [[index]], [[log]]

## [2026-04-07] tweet | Farzapedia — Personal Wiki as Agent Knowledge Base
- Source: https://x.com/farzatv/status/2040563939797504467
- Tweet page: [[tweets/farzapedia-personal-wiki]]
- Key insight: Structured wiki with index.md + backlinks beats RAG for AI agents
- Relevance: High — our wiki already follows this exact architecture
- Recommendations: 4 (add unstructured sources, aggressive auto-update, media tracking, query-driven pages)

## [2026-04-06] bootstrap | Wiki initialised
- Created directory structure: raw/, entities/, concepts/, sources/, comparisons/, decisions/, questions/, tasks/
- Created starter files: index.md, log.md, overview.md
- Wiki is ready for its first source ingestion.

## [2026-04-07] bootstrap | Complete directory structure
- Created missing directories: entities/, concepts/, sources/, comparisons/, decisions/, questions/
- Created missing raw subdirectories: raw/papers/, raw/transcripts/, raw/screenshots/, raw/data/
- Added .gitkeep files to track empty directories in git
- Wiki directory structure now fully matches CLAUDE.md schema

## [2026-04-07] ingest | CaseWare Probe Project Overview
- Source: `raw/articles/caseware-probe-project-overview.md`
- Summary: [[sources/caseware-probe-project-overview]]
- Pages touched: [[index]], [[log]]
- New pages created: [[sources/caseware-probe-project-overview]], [[entities/caseware-working-papers]], [[entities/probe-audit-premium-plus]], [[entities/probe-audit-manual]], [[concepts/four-stage-pipeline]], [[concepts/isa-standards]], [[concepts/ooxml-document-structure]], [[2-working-papers/progress]]
- New directories created: standards/, working-papers/, procedures/
- Contradictions flagged: none (first source)

## [2026-04-07] update | Pipeline corrected to four stages
- Corrected pipeline from three stages to four: How-To Doc → Visual Script → Visual Recording → Professional Video
- "V5" refers to document version, not pipeline stage count
- Renamed [[concepts/four-stage-pipeline]] (was three-stage-pipeline)
- Updated [[2-working-papers/progress]] with all 23 working papers (all at How-To Doc V5)
- Updated cross-references across 8 wiki pages

## [2026-04-07] ingest | Probe Documents Project Plan 2025
- Source: `raw/project-plans/probe-project-plan-2025.csv`
- Summary: [[sources/probe-project-plan-2025]]
- Pages touched: [[2-working-papers/progress]], [[index]], [[log]]
- New pages created: [[sources/probe-project-plan-2025]]
- Contradictions flagged: Project scope is 57 working papers (not 23 as initially understood). 02.xx How-To docs are in progress (not finalised as previously assumed).

## [2026-04-07] update | Success Community entity + corrections
- Created [[entities/success-community]] — publishing platform for finalised docs and videos
- Confirmed: V5 .docx files are draft How-To documents currently in progress (02.xx Finalisation section)
- Resolved open question about Success Community platform

## [2026-04-07] ingest | CaseView PDFs — all sections (40 working papers)
- Sources: 41 PDFs + 1 .docx in `raw/caseview-documents/`
- Created 38 new working paper wiki pages in `working-papers/`
- Sections covered: Pre-Engagement (10.xx: 8 pages), Planning & Risk (11.xx: 7 pages), Audit Planning (12.xx: 6 pages), Finalisation (02.xx: 15 pages), Execution (16-18.xx: 3 pages)
- Updated [[concepts/isa-standards]] with comprehensive ISA-to-working-paper map (23 ISAs mapped)
- Updated [[index]] with full working paper listing by section
- Key findings: ISA 315 referenced in 11 working papers, ISA 240 in 10, ISA 330 in 6
- New section discovered: Execution (16.10, 17.10, 18.10) — not in original project plan
- Two duplicate 11.50 PDFs confirmed identical; both referenced on single page

## [2026-04-07] update | Reorganise raw/ for project-specific structure
- Created: raw/caseview-documents/ (original audit program PDFs from CaseView)
- Created: raw/how-to-drafts/ (V5 How-To .docx drafts in progress)
- Created: raw/visual-scripts/ (video narration scripts)
- Created: raw/probe-manual/ (Probe Audit Manual chapters)
- Created: raw/videos/ (recordings and final videos)
- Created: raw/project-plans/ (project tracking spreadsheets)
- Moved probe-project-plan-2025.csv from raw/data/ to raw/project-plans/
- Removed unused generic folders: raw/data/, raw/papers/, raw/transcripts/
- Kept: raw/articles/ (project briefings), raw/screenshots/

## [2026-04-07] ingest | ISA Standards from IAASB 2025 Handbook Volume 1
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf` (extracted text)
- New pages created: [[1-standards/2-isa/isa-300-planning-an-audit]], [[1-standards/2-isa/isa-315-risk-identification]], [[1-standards/2-isa/isa-320-materiality]], [[1-standards/2-isa/isa-330-responses-to-assessed-risks]], [[1-standards/2-isa/isa-402-service-organisations]], [[1-standards/2-isa/isa-450-evaluation-of-misstatements]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements (all "shall" statements), Key Definitions, Application to Probe Working Papers (mapped to specific CaseWare working paper refs), Related Standards with wiki-links
- ISA-to-working-paper mappings documented: ISA 300 (3 WPs), ISA 315 (11 WPs), ISA 320 (5 WPs), ISA 330 (6 WPs), ISA 402 (1 WP), ISA 450 (2 WPs)
- Contradictions flagged: none

## [2026-04-07] ingest | ISA Standards from IAASB 2025 Handbook Volume 1 (batch 2)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf` (extracted text at /tmp/iaasb-vol1.txt)
- New pages created: [[1-standards/1-isqm/isqm-1-quality-management-firms]], [[1-standards/1-isqm/isqm-2-engagement-quality-reviews]], [[1-standards/2-isa/isa-200-overall-objectives]], [[1-standards/2-isa/isa-210-terms-of-engagement]], [[1-standards/2-isa/isa-220-quality-management-audit]], [[1-standards/2-isa/isa-230-audit-documentation]], [[1-standards/2-isa/isa-240-fraud]], [[1-standards/2-isa/isa-250-laws-and-regulations]], [[1-standards/2-isa/isa-260-communication-with-tcwg]], [[1-standards/2-isa/isa-265-internal-control-deficiencies]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements, Key Definitions, Application to Probe Working Papers, Related Standards
- ISA-to-working-paper mappings documented: ISA 200 (1 WP), ISA 210 (2 WPs), ISA 220 (6 WPs), ISA 240 (10 WPs), ISA 250 (4 WPs), ISA 260 (2 WPs), ISA 265 (0 — firm-level communication standard)
- ISQM 1 and ISQM 2 are firm-level quality management standards (not directly mapped to individual working papers)
- Total standards pages now: 16 (ISQM 1-2, ISA 200, 210, 220, 230, 240, 250, 260, 265, 300, 315, 320, 330, 402, 450)
- Contradictions flagged: none

## [2026-04-07] ingest | ISA 700-810 Standards (Reporting Series)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf`, pages 593-784
- New pages created: [[1-standards/2-isa/isa-700-forming-an-opinion]], [[1-standards/2-isa/isa-701-key-audit-matters]], [[1-standards/2-isa/isa-705-modified-opinions]], [[1-standards/2-isa/isa-706-emphasis-of-matter]], [[1-standards/2-isa/isa-710-comparative-information]], [[1-standards/2-isa/isa-720-other-information]], [[1-standards/2-isa/isa-800-special-purpose-frameworks]], [[1-standards/2-isa/isa-805-single-financial-statements]], [[1-standards/2-isa/isa-810-summary-financial-statements]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements, Key Definitions, Application to Probe Working Papers, Related Standards
- ISA-to-working-paper mappings documented: ISA 700 → 02.50, 02.40; ISA 701 → 02.00, 02.55; ISA 710 → 17.10; ISA 705, 706, 720, 800, 805, 810 → none yet
- Total standards pages now: 25 (added ISA 700, 701, 705, 706, 710, 720, 800, 805, 810)
- Contradictions flagged: none

## [2026-04-07] ingest | ISA 500-620 Standards (Evidence, Estimates, Going Concern, Group Audits)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf`, pages 363-592
- New pages created: [[1-standards/2-isa/isa-500-audit-evidence]], [[1-standards/2-isa/isa-501-specific-audit-evidence]], [[1-standards/2-isa/isa-505-external-confirmations]], [[1-standards/2-isa/isa-510-opening-balances]], [[1-standards/2-isa/isa-520-analytical-procedures]], [[1-standards/2-isa/isa-530-audit-sampling]], [[1-standards/2-isa/isa-540-accounting-estimates]], [[1-standards/2-isa/isa-550-related-parties]], [[1-standards/2-isa/isa-560-subsequent-events]], [[1-standards/2-isa/isa-570-going-concern]], [[1-standards/2-isa/isa-580-written-representations]], [[1-standards/2-isa/isa-600-group-audits]], [[1-standards/2-isa/isa-610-internal-auditors]], [[1-standards/2-isa/isa-620-auditors-expert]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements (all "shall" statements), Key Definitions, Application to Probe Working Papers, Related Standards with wiki-links
- ISA-to-working-paper mappings documented: ISA 500 (12.20), ISA 510 (17.10), ISA 540 (10.31, 10.51), ISA 550 (10.51, 12.10, 12.30, 18.10), ISA 560 (02.10), ISA 570 (02.20, 02.22), ISA 600 (11.20G), ISA 610 (12.21), ISA 620 (10.55, 12.10)
- ISA 501, 505, 520, 530, 580 have no specific Probe working paper mappings yet
- Total standards pages now: 39 (previous 25 + 14 new)
- Contradictions flagged: none

## [2026-04-07] ingest | IAASB 2025 Handbook Volumes 2-5 (Non-ISA Standards)
- Sources: Extracted text from Volumes 2-5 of IAASB 2025 Handbook
- New pages created: [[1-standards/6-other/isa-for-lce-less-complex-entities]], [[1-standards/6-other/issa-5000-sustainability-assurance]], [[1-standards/3-isre/isre-2400-review-historical-fs]], [[1-standards/3-isre/isre-2410-review-interim-info]], [[1-standards/4-isae/isae-3000-assurance-engagements]], [[1-standards/4-isae/isae-3400-prospective-financial-info]], [[1-standards/4-isae/isae-3402-service-org-controls]], [[1-standards/4-isae/isae-3410-greenhouse-gas]], [[1-standards/4-isae/isae-3420-pro-forma-financial-info]], [[1-standards/5-isrs/isrs-4400-agreed-upon-procedures]], [[1-standards/5-isrs/isrs-4410-compilation-engagements]]
- Pages touched: [[index]], [[log]]
- Volume 2: ISA for LCE — standalone audit standard for less complex entities (effective Dec 2025)
- Volume 3: ISSA 5000 — new sustainability assurance standard (effective Dec 2026), supersedes ISAE 3410
- Volume 4: ISRE 2400, ISRE 2410 (review engagements); ISAE 3000, 3400, 3402, 3410, 3420 (assurance engagements); ISRS 4400, 4410 (related services)
- Volume 5: Contains Audit Quality Framework and International Framework for Assurance Engagements (frameworks, not standards — no individual standard pages created)
- Note: No IAPNs found in Volume 5; IAPNs may have been removed from the 2025 Handbook edition
- Total standards pages now: 50 (added 11 new pages)
- Cross-references established between all new standards and existing wiki pages
- Contradictions flagged: none

## [2026-04-07] evolve | Overview rewritten
- Overview rewritten from placeholder to full synthesis
- Key content: project description, four-stage pipeline summary, progress tables, team roster, IAASB standards coverage (50 pages), most-referenced ISAs, open areas
- Pages touched: [[overview]]

## [2026-04-07] tweet | AI Edge — Claude Skills Ultimate Guide
- Source: https://x.com/aiedge_/status/2036815449225298369
- Tweet page: [[tweets/aiedge-claude-skills-guide]]
- Key insight: Claude Skills are reusable .md instruction packages — build once, invoke repeatedly. Guide covers 4-step build process, 8 optimisation strategies, and Skills 2.0 features (evals, A/B testing)
- Relevance: High — provides the "how to build" methodology for the skills identified in the exploraX_ tweet; reverse prompting + evals directly applicable to Probe pipeline
- Recommendations: 3 (4-step build process, reverse prompting, Skills 2.0 evals as quality gates)

## [2026-04-07] tweet | exploraX_ — 20 Powerful Agentic Skills for Claude, ChatGPT & Gemini
- Source: https://x.com/explorax_/status/2039269234253934811
- Tweet page: [[tweets/explorax-20-agentic-skills]]
- Key insight: Agentic skills packaged as .md files turn general-purpose LLMs into specialised workers — 20 skills across writing, visual, research, and coding categories
- Relevance: High — Video Script Generator, Content Repurposing, Tone Enforcer, and Skill Creator directly map to the four-stage pipeline
- Recommendations: 4 (Visual Script Writer skill, Tone & Style Enforcer, Skill Creator meta-pattern, caption/subtitle generation)

## [2026-04-07] lint | Wiki health check
- Issues found: 38
- Orphan pages: 0
- Missing link targets: 0
- Missing working paper pages: 18 (mostly Leadsheets section + Group audit papers without CaseView PDFs)
- Structural backlink gaps: 3 (Success Community and OOXML pages missing backlinks from target pages)
- Empty directories: 4 (procedures, comparisons, decisions, questions)
- Unmapped ISA standards: 12 (standards with pages but no working paper mappings)
- Stale content: 1 (source summary still references three-stage pipeline)
- Results filed: [[questions/wiki-health]]
- New pages created: [[questions/wiki-health]]
- Pages touched: [[index]], [[log]]
