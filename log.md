# Activity Log

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
- New pages created: [[sources/caseware-probe-project-overview]], [[entities/caseware-working-papers]], [[entities/probe-audit-premium-plus]], [[entities/probe-audit-manual]], [[concepts/four-stage-pipeline]], [[concepts/isa-standards]], [[concepts/ooxml-document-structure]], [[working-papers/progress]]
- New directories created: standards/, working-papers/, procedures/
- Contradictions flagged: none (first source)

## [2026-04-07] update | Pipeline corrected to four stages
- Corrected pipeline from three stages to four: How-To Doc → Visual Script → Visual Recording → Professional Video
- "V5" refers to document version, not pipeline stage count
- Renamed [[concepts/four-stage-pipeline]] (was three-stage-pipeline)
- Updated [[working-papers/progress]] with all 23 working papers (all at How-To Doc V5)
- Updated cross-references across 8 wiki pages

## [2026-04-07] ingest | Probe Documents Project Plan 2025
- Source: `raw/project-plans/probe-project-plan-2025.csv`
- Summary: [[sources/probe-project-plan-2025]]
- Pages touched: [[working-papers/progress]], [[index]], [[log]]
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
- New pages created: [[standards/isa-300]], [[standards/isa-315]], [[standards/isa-320]], [[standards/isa-330]], [[standards/isa-402]], [[standards/isa-450]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements (all "shall" statements), Key Definitions, Application to Probe Working Papers (mapped to specific CaseWare working paper refs), Related Standards with wiki-links
- ISA-to-working-paper mappings documented: ISA 300 (3 WPs), ISA 315 (11 WPs), ISA 320 (5 WPs), ISA 330 (6 WPs), ISA 402 (1 WP), ISA 450 (2 WPs)
- Contradictions flagged: none

## [2026-04-07] ingest | ISA Standards from IAASB 2025 Handbook Volume 1 (batch 2)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf` (extracted text at /tmp/iaasb-vol1.txt)
- New pages created: [[standards/isqm-1]], [[standards/isqm-2]], [[standards/isa-200]], [[standards/isa-210]], [[standards/isa-220]], [[standards/isa-230]], [[standards/isa-240]], [[standards/isa-250]], [[standards/isa-260]], [[standards/isa-265]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements, Key Definitions, Application to Probe Working Papers, Related Standards
- ISA-to-working-paper mappings documented: ISA 200 (1 WP), ISA 210 (2 WPs), ISA 220 (6 WPs), ISA 240 (10 WPs), ISA 250 (4 WPs), ISA 260 (2 WPs), ISA 265 (0 — firm-level communication standard)
- ISQM 1 and ISQM 2 are firm-level quality management standards (not directly mapped to individual working papers)
- Total standards pages now: 16 (ISQM 1-2, ISA 200, 210, 220, 230, 240, 250, 260, 265, 300, 315, 320, 330, 402, 450)
- Contradictions flagged: none
