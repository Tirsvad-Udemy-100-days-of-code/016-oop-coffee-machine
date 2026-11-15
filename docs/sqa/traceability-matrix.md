# Traceability Matrix

## Metadata
| Key | Value |
| --- | --- |
| ID | TM-001 |
| CrossReference | [BC-001] |

## Version History
| Date | Status | Author | Reviewer | Change | Commit |
| --- | --- | --- | --- | --- | --- |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Initial version | [c24f412] |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Added RC-007 (source code review) to the MIL-002 row | [26d87d0] |
| 2026-11-15 | Accepted | Jens Tirsvad Nielsen | AI as stand-in for S01 | Accepted; added MIL-004, the wiki, the concern coverage and the new review records RC-008 to RC-015; set the domain to education; reviewed in autonomous mode, not independent | pending |

---

## Purpose

Tracks backward and forward links between artifact instances so that traceability is measurable. A row is added or updated whenever an artifact instance is created or reviewed.

## Traceability Table

| Artifact Instance | Type | Language | Domain | Upstream (Backward Link) | Downstream (Forward Link) | Last Reviewed (RC-ID) |
| --- | --- | --- | --- | --- | --- | --- |
| [BC-001] | Business Case | en | education | - | [SA-001], [PP-001], [MIL-004] | [RC-008] |
| [SA-001] | Stakeholder Analysis | en | education | [BC-001] | [PP-001] | [RC-009] |
| [PP-001] | Project Plan | en | education | [BC-001], [SA-001] | [MIL-001], [MIL-002], [MIL-003], [MIL-004] | [RC-010] |
| [MIL-001] | Milestone | en | education | [BC-001], [PP-001] | - | [RC-011] |
| [MIL-002] | Milestone | en | education | [BC-001], [PP-001] | - | [RC-012] |
| [MIL-003] | Milestone | en | education | [BC-001], [PP-001] | - | [RC-013] |
| [MIL-004] | Milestone | en | education | [BC-001], [PP-001] | - | [RC-014] |
| Source code (`src/`, `tests/`) | Source code | - | - | [MIL-002] | - | [RC-007] |
| Wiki | Wiki | en, da, ms | education | [BC-001] | - | [RC-015] |

## Concern Coverage

| Concern (CN-ID) | Views that answer it | Decisions (ADR) | Quality check (TP) | Status |
| --- | --- | --- | --- | --- |
| CN-001 | [MIL-002] (criteria 1 to 5) | - | - | Covered |
| CN-002 | [PP-001] (every phase ends in a pull request), [MIL-004] (criterion 6) | - | - | Covered |
| CN-003 | [MIL-002] (criteria 1 to 3) | - | - | Covered |
| CN-004 | [MIL-003] (criteria 1 and 2), [MIL-004] (criterion 3) | - | - | Covered |
| CN-005 | [MIL-003] (criteria 1 and 4), [MIL-004] (criterion 3) | - | - | Covered |
| CN-006 | [MIL-001] (criterion 3) | - | - | Covered |

## Open Inconsistencies

| # | Views | Inconsistency | Found in (RC-ID) | Status | Resolved in |
| --- | --- | --- | --- | --- | --- |
| - | - | none found | - | Closed | - |

## Coverage Notes

- `-` in Upstream means foundational; in Downstream, nothing is built on it yet.
- No KPI, use case, user story or design artifact exists: the course supplies the design, so the tasks in the milestones are plain tasks. The source code is reviewed in [RC-007] and not again in MIL-004.
- The domain of every artifact is `education` since MIL-004; the earlier review records [RC-001] to [RC-007] state the former domain `it` as it was at the time.

---

[BC-001]: ../business-case.md
[SA-001]: ../stakeholder-analysis.md
[PP-001]: ../project-plan.md
[MIL-001]: ../milestones/mil-001-setup.md
[MIL-002]: ../milestones/mil-002-core.md
[MIL-003]: ../milestones/mil-003-docs.md
[RC-001]: reviews/rc-001-business-case.md
[RC-002]: reviews/rc-002-stakeholder-analysis.md
[RC-003]: reviews/rc-003-mil-001.md
[RC-004]: reviews/rc-004-mil-002.md
[RC-005]: reviews/rc-005-mil-003.md
[RC-006]: reviews/rc-006-project-plan.md
[RC-007]: reviews/rc-007-source-code-mil-002.md
[c24f412]: https://git.tirsystem.com/Tirsvad-Udemy-100_days_of_code/016-oop_coffee_machine/commit/c24f41207fb15f39b0ad6501e1f3126d3bd9232e
[26d87d0]: https://git.tirsystem.com/Tirsvad-Udemy-100_days_of_code/016-oop_coffee_machine/commit/26d87d0d0ee63eaefa32e6a71142cfa5397361c7
[MIL-004]: ../milestones/mil-004-framework-baseline.md
[RC-008]: ./reviews/rc-008-business-case.md
[RC-009]: ./reviews/rc-009-stakeholder-analysis.md
[RC-010]: ./reviews/rc-010-project-plan.md
[RC-011]: ./reviews/rc-011-milestone-001.md
[RC-012]: ./reviews/rc-012-milestone-002.md
[RC-013]: ./reviews/rc-013-milestone-003.md
[RC-014]: ./reviews/rc-014-milestone-004.md
[RC-015]: ./reviews/rc-015-wiki.md
