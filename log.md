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
- Source: `raw/data/probe-project-plan-2025.csv`
- Summary: [[sources/probe-project-plan-2025]]
- Pages touched: [[working-papers/progress]], [[index]], [[log]]
- New pages created: [[sources/probe-project-plan-2025]]
- Contradictions flagged: Project scope is 57 working papers (not 23 as initially understood). 02.xx How-To docs are in progress (not finalised as previously assumed).

## [2026-04-07] update | Success Community entity + corrections
- Created [[entities/success-community]] — publishing platform for finalised docs and videos
- Confirmed: V5 .docx files are draft How-To documents currently in progress (02.xx Finalisation section)
- Resolved open question about Success Community platform
