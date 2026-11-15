# Stakeholder Analysis: OOP Coffee Machine

## Metadata
| Key | Value |
| --- | --- |
| ID | SA-001 |
| CrossReference | [BC-001] |
| Language | en |
| Domain | education |

## Version History
| Date | Status | Author | Reviewer | Change | Commit |
| --- | --- | --- | --- | --- | --- |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Initial version | [c24f412] |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Accepted after RC-002 (Go) | [c24f412] |
| 2026-11-15 | Accepted | Jens Tirsvad Nielsen | AI as stand-in for S01 | Added concern IDs CN-001 to CN-006 (QC-SA-001 criterion 9), a conflict about author and reviewer being one person, the baseline phase in the communication table and the traceability; set the domain to education; reviewed in autonomous mode, not independent | pending |

---

## Purpose

Identifies who is affected by the coffee machine repository and how closely
each party is managed. Method: Mendelow's power/interest grid, with concerns
mapped to FURPS+.

## Stakeholder Summary Table

| ID | Name | Role/Title | Organization | Power Level | Interest Level | Quadrant | Primary Concern (Business Language) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| S01 | Jens Tirsvad Nielsen | Course participant; Product Owner, developer and reviewer | Tirsvad | HIGH | HIGH | Manage Closely | Finish the assignment with clean code, tests and documentation |
| S02 | Udemy coursists | Fellow course participants | Udemy course community | LOW | HIGH | Keep Informed | Readable, runnable code with the assignment's function names, and README instructions to run it |
| S03 | GitHub viewers | Repository browsers | Public | LOW | LOW | Monitor | A clear repository description, topics and README, and no runtime dependencies |

## Power/Interest Classification Rationale

- **Manage Closely (S01):** decides scope, writes and reviews everything.
- **Keep Informed (S02):** cannot change the project but depends on its usability; the README is the channel.
- **Monitor (S03):** casual visitors with no influence; the repository presentation is enough.

## Primary Concerns and FURPS+ Mapping

| Concern ID | Stakeholder | Concern | FURPS+ attribute |
| --- | --- | --- | --- |
| CN-001 | S01 | Complete, tested assignment solution | Functionality, Reliability |
| CN-002 | S01 | Traceable steps via pull requests | Supportability |
| CN-003 | S02 | Assignment function names kept | Functionality |
| CN-004 | S02 | Run instructions that work | Usability |
| CN-005 | S03 | Clear description, topics and README | Usability |
| CN-006 | S03 | No runtime dependencies | Implementation constraint, Supportability |

## Communication Requirements

| ID | Channel | Frequency | Deliverable | Phase / Milestone |
| --- | --- | --- | --- | --- |
| S01 | Chat and pull request review | Per phase | Working-tree changes and PRs | MIL-001, MIL-002, MIL-003, MIL-004 |
| S02 | README | Once, updated on change | Setup, run and test instructions | MIL-003 |
| S02, S03 | Wiki in English, Danish and Malay | Once, updated on change | Wiki pages | MIL-004 |
| S03 | Repository description, topics, README | Once | Repository presentation | MIL-003 |

## Conflicting Interests and Mitigations

| Conflict | Stakeholders | Mitigation |
| --- | --- | --- |
| S02 wants assignment names, while clean Python style prefers other names | S01, S02 | Keep the assignment's method names; follow the style rules elsewhere |
| The author and the reviewer of the baseline documents are the same person (S01), so the review is not independent | S01 | The AI assistant acts as stand-in reviewer for S01; every review record says `Mode: autonomous, not independent` and the end-of-run summary lists it for challenge |

## Traceability Analysis

### Business Goal Alignment

| Stakeholder | Concern | Business Case objective |
| --- | --- | --- |
| S01 | Complete, tested solution (CN-001, CN-002) | [BC-001] objectives 1 and 2 |
| S02 | Runnable instructions, assignment names (CN-003, CN-004) | [BC-001] objective 3 |
| S03 | Presentable repository, no runtime dependencies (CN-005, CN-006) | [BC-001] objective 4 |
| S01, S02, S03 | A project that follows the common baseline of the framework, with a wiki in three languages | [BC-001] objective 5 |

## Sign-Off

| Stakeholder ID | Decision | Date |
| --- | --- | --- |
| S01 | Pending review | |

---

[BC-001]: ./business-case.md
[c24f412]: https://git.tirsystem.com/Tirsvad-Udemy-100_days_of_code/016-oop_coffee_machine/commit/c24f41207fb15f39b0ad6501e1f3126d3bd9232e
