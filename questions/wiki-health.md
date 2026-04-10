---
title: "Wiki Health Check"
type: question
created: 2026-04-07
updated: 2026-04-07
tags: [lint, health-check, maintenance]
status: active
---

# Wiki Health Check

> Lint run: 2026-04-07 | Total pages: ~100 | Sources: 2

## Orphan Pages

No orphan pages found. All wiki pages have at least one inbound `wiki link` from another page.

## Missing Pages (Broken Links)

No broken wiki-links found. All `wiki link` targets resolve to existing `.md` files.

## Missing Working Paper Wiki Pages

18 working papers tracked in [[2-working-papers/progress]] do not have their own wiki page. These are papers that appear in the project plan but were not among the CaseView PDFs ingested.

### Pre-Engagement (missing pages)
- [ ] 10.30 — Discussions with those charged with governance (has a wiki page at [[2-working-papers/2-pre-engagement-planning/10-31-discussions-with-tcwg/10-31-discussions-with-tcwg Wiki Page]] but 10.30 is listed separately in progress tracker)
- [ ] 10.50G — Plan extent of risk assessment procedures (Group)
- [ ] 10.52 — Preliminary analytical review
- [ ] 10.53 — Understanding of accounting estimates

### Planning & Risk Assessment (missing pages)
- [ ] 11.21 — Laws and regulations

### Audit Planning (missing pages)
- [ ] 12.20G — Further audit work at component level (Group)
- [ ] 12.22G — Use of component auditors (Group)
- [ ] 12.23G — Component performance materiality (Group)
- [ ] 12.26 — Use of another practitioner

### Leadsheets & Working Papers (all 14 missing pages)
- [ ] 90.10 — Blank work program
- [ ] 90.20 — Substantive testing worksheet
- [ ] 90.30 — Controls testing worksheet
- [ ] 405.11 — Attendance at physical inventory count
- [ ] 420.11 — Cash count work program
- [ ] 430.11 — Receivables direct confirmation
- [ ] 430.61 — Receivables confirmation summary
- [ ] 750.11 — Wage payout work program
- [ ] 750.60 — Director's remuneration certificate

> **Note:** Three additional Leadsheets items (Sections work programs, General work programs, Probe Firm settings, All Probe features, Minutes/01.60) appear in the tracker. Minutes has a page at [[2-working-papers/1-finalisation/01-60-minutes/01-60-minutes Wiki Page]]; the others have no reference number and no wiki page.

## One-Way Links (Missing Backlinks)

The following pages link outward to targets that do not link back. This is a known pattern for hub pages like [[concepts/isa-standards]] which links to all 30+ working papers — most working papers do not link back to the ISA standards concept page (they link to specific standard pages instead, which is acceptable).

### Structural backlink gaps worth fixing
- [ ] [[entities/success-community]] links to [[concepts/four-stage-pipeline]], but the pipeline page does not link back to Success Community
- [ ] [[entities/success-community]] links to [[entities/caseware-working-papers]], but that page does not link back
- [ ] [[concepts/ooxml-document-structure]] links to [[entities/caseware-working-papers]], but that page does not link back

### Acceptable one-way links (hub-to-leaf pattern)
- [[concepts/isa-standards]] links to ~30 working paper pages — these link to specific ISA standard pages instead (acceptable)
- [[entities/success-community]] links to [[2-working-papers/progress]] — the progress page is a tracker, not expected to link back to every entity

## Empty Directories / Unfiled Content Types

- [ ] `procedures/` — Empty. No step-by-step workflows documented yet. Candidate: the review handoff process between team members.
- [ ] `comparisons/` — Empty. No side-by-side analyses filed.
- [ ] `decisions/` — Empty. No decision records filed. Candidate: the decision to use V5 document template, pipeline design choices.
- [ ] `questions/` — This is the first page in this directory.

## ISA Standards Without Working Paper Mappings

These ISA standards have wiki pages but no specific Probe working paper mappings identified:

- [ ] [[1-standards/2-isa/isa-265-internal-control-deficiencies]] — Communicating Deficiencies in Internal Control (firm-level)
- [ ] [[1-standards/2-isa/isa-501-specific-audit-evidence]] — Audit Evidence for Selected Items
- [ ] [[1-standards/2-isa/isa-505-external-confirmations]] — External Confirmations
- [ ] [[1-standards/2-isa/isa-520-analytical-procedures]] — Analytical Procedures
- [ ] [[1-standards/2-isa/isa-530-audit-sampling]] — Audit Sampling
- [ ] [[1-standards/2-isa/isa-580-written-representations]] — Written Representations
- [ ] [[1-standards/2-isa/isa-705-modified-opinions]] — Modifications to the Auditor's Opinion
- [ ] [[1-standards/2-isa/isa-706-emphasis-of-matter]] — Emphasis of Matter Paragraphs
- [ ] [[1-standards/2-isa/isa-720-other-information]] — Other Information
- [ ] [[1-standards/2-isa/isa-800-special-purpose-frameworks]] — Special Purpose Frameworks
- [ ] [[1-standards/2-isa/isa-805-single-financial-statements]] — Single Financial Statements
- [ ] [[1-standards/2-isa/isa-810-summary-financial-statements]] — Summary Financial Statements

> Some of these (ISA 501, 505, 530) likely map to Leadsheets working papers (430.xx confirmations, sampling worksheets) once those pages are created.

## Stale Content

- [ ] [[sources/caseware-probe-project-overview]] still describes a "three-stage" pipeline in its key claims and refers to "V1 → V2 → Video Script" rather than the corrected four-stage pipeline. The frontmatter was not updated after the pipeline correction.

## Summary

| Category | Issues |
|----------|--------|
| Orphan pages | 0 |
| Missing link targets | 0 |
| Missing working paper pages | 18 |
| Backlink gaps (structural) | 3 |
| Empty directories | 4 |
| Unmapped ISA standards | 12 |
| Stale content | 1 |
| **Total issues** | **38** |

## References

- [[index]]
- [[2-working-papers/progress]]
- [[concepts/isa-standards]]
- [[overview]]
