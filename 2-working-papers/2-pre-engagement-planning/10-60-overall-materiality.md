---
title: "Overall Materiality Assessment"
type: entity
created: 2026-04-07
updated: 2026-04-07
tags: [working-papers, pre-engagement, probe]
sources: [caseview-10-60]
ref: "10.60"
pipeline-stage: how-to-doc
status: active
---

# Overall Materiality Assessment

## Purpose

This single-page working paper documents the determination of overall materiality, performance materiality, and the trivial misstatement threshold for the audit engagement. It uses multiple financial bases with predefined percentage ranges to calculate a materiality range, from which the auditor selects the final materiality figure.

## Key Fields & Sections

### Bases for Materiality Assessment
A table with the following columns per basis:
- **Min %** — Lower bound of acceptable percentage
- **Max %** — Upper bound of acceptable percentage
- **Current year (2023)** — Financial statement figure
- **Prior year (2022)** — Comparative figure

The five standard bases are:

| Basis | Min % | Max % |
|-------|-------|-------|
| Revenue | 0.5% | 1.0% |
| Net profit before tax | 5.0% | 10.0% |
| Shareholders' equity | 2.0% | 5.0% |
| Total assets | 1.0% | 2.0% |
| Total liabilities | 1.0% | 2.0% |

### Reasons for Bases Used (Q1-6)
Free-text fields to document the rationale for:
1. Why current year figures are used as the basis
2. Why revenue is used
3. Why net profit before tax is used
4. Why shareholders' equity is used
5. Why total assets are used
6. Why total liabilities are used

### Materiality Calculation
- **Calculated range** — System calculates the range based on selected parameters (e.g. R520,000 to R1,100,000)
- **Overall materiality (Q1)** — Final materiality amount selected by the auditor
- **Reasons for materiality value selected (Q2)** — Justification for the chosen figure within the range
- **Performance materiality (Q3)** — Derived from overall materiality and desired audit risk
  - Linked to Desired Audit Risk set in [[2-working-papers/2-pre-engagement-planning/10-20]]
- **Clearly trivial threshold (Q4)** — Amount below which misstatements are considered clearly trivial

### Header Fields
- Planning by / Reviewed by / Performed by / Final review sign-off fields
- Year end date

## ISA References

- ISA 320 — Materiality in Planning and Performing an Audit (determination of materiality and performance materiality)
- ISA 450 — Evaluation of Misstatements (clearly trivial threshold)
- ISA 315 — Identifying and Assessing the Risks of Material Misstatement (materiality informs risk assessment)

## Completion Guidance

- Complete after [[2-working-papers/2-pre-engagement-planning/10-20]] (which sets the Desired Audit Risk) and after financial data is available
- The system auto-calculates the range based on the trial balance figures and the min/max percentages
- The auditor must exercise professional judgement in selecting the final materiality within (or sometimes outside) the calculated range
- Document reasons for each basis used — do not leave the reason fields blank
- Performance materiality is typically 50-75% of overall materiality depending on audit risk:
  - Very low audit risk = lower performance materiality percentage
  - Higher audit risk = higher performance materiality percentage
- The clearly trivial threshold is typically 5% of overall materiality (or lower for very low audit risk)
- Overall materiality flows into [[2-working-papers/3-planning-risk-assessment/11-10]] where it appears as performance materiality per COTABD
- Consider whether specific materiality is needed for particular COTABDs (set in [[2-working-papers/3-planning-risk-assessment/11-10]])
- If the materiality basis changes from prior year, document the reason

## Probe Project

Artifacts for working paper 10.60:

- CaseView source: [[raw/caseview-documents/2-pre-engagement-planning/10.60 Overall Materiality Assessment CaseView Document.pdf]]

## Related

- [[entities/caseware-working-papers]]
- [[entities/probe-audit-premium-plus]]
- [[concepts/four-stage-pipeline]]
- [[2-working-papers/2-pre-engagement-planning/10-20]] — Engagement evaluation (sets Desired Audit Risk used for performance materiality)
- [[2-working-papers/2-pre-engagement-planning/10-51]] — Types and volumes of transactions (financial data context)
- [[2-working-papers/3-planning-risk-assessment/11-10]] — Risk analysis summary (materiality applied per COTABD)
- [[2-working-papers/1-finalisation/02-40]] — Evaluation of misstatements (materiality used to evaluate detected misstatements)

- [[2-working-papers/2-pre-engagement-planning/index]]

## References

- CaseView source: [[raw/caseview-documents/2-pre-engagement-planning/10.60 Overall Materiality Assessment CaseView Document.pdf]]
