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

## [2026-04-07] ingest | ISA 700-810 Standards (Reporting Series)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf`, pages 593-784
- New pages created: [[standards/isa-700]], [[standards/isa-701]], [[standards/isa-705]], [[standards/isa-706]], [[standards/isa-710]], [[standards/isa-720]], [[standards/isa-800]], [[standards/isa-805]], [[standards/isa-810]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements, Key Definitions, Application to Probe Working Papers, Related Standards
- ISA-to-working-paper mappings documented: ISA 700 → 02.50, 02.40; ISA 701 → 02.00, 02.55; ISA 710 → 17.10; ISA 705, 706, 720, 800, 805, 810 → none yet
- Total standards pages now: 25 (added ISA 700, 701, 705, 706, 710, 720, 800, 805, 810)
- Contradictions flagged: none

## [2026-04-07] ingest | ISA 500-620 Standards (Evidence, Estimates, Going Concern, Group Audits)
- Source: `raw/iaasb-handbook/IAASB-2025-Handbook-Volume-1.pdf`, pages 363-592
- New pages created: [[standards/isa-500]], [[standards/isa-501]], [[standards/isa-505]], [[standards/isa-510]], [[standards/isa-520]], [[standards/isa-530]], [[standards/isa-540]], [[standards/isa-550]], [[standards/isa-560]], [[standards/isa-570]], [[standards/isa-580]], [[standards/isa-600]], [[standards/isa-610]], [[standards/isa-620]]
- Pages touched: [[index]]
- Each standard page includes: Objective, Scope, Key Requirements (all "shall" statements), Key Definitions, Application to Probe Working Papers, Related Standards with wiki-links
- ISA-to-working-paper mappings documented: ISA 500 (12.20), ISA 510 (17.10), ISA 540 (10.31, 10.51), ISA 550 (10.51, 12.10, 12.30, 18.10), ISA 560 (02.10), ISA 570 (02.20, 02.22), ISA 600 (11.20G), ISA 610 (12.21), ISA 620 (10.55, 12.10)
- ISA 501, 505, 520, 530, 580 have no specific Probe working paper mappings yet
- Total standards pages now: 39 (previous 25 + 14 new)
- Contradictions flagged: none

## [2026-04-07] ingest | IAASB 2025 Handbook Volumes 2-5 (Non-ISA Standards)
- Sources: Extracted text from Volumes 2-5 of IAASB 2025 Handbook
- New pages created: [[standards/isa-for-lce]], [[standards/issa-5000]], [[standards/isre-2400]], [[standards/isre-2410]], [[standards/isae-3000]], [[standards/isae-3400]], [[standards/isae-3402]], [[standards/isae-3410]], [[standards/isae-3420]], [[standards/isrs-4400]], [[standards/isrs-4410]]
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
