# Business Case: OOP Coffee Machine

## Metadata
| Key | Value |
| --- | --- |
| ID | BC-001 |
| CrossReference | [SA-001], [PP-001], [MIL-004] |
| Language | en |
| Domain | education |

## Version History
| Date | Status | Author | Reviewer | Change | Commit |
| --- | --- | --- | --- | --- | --- |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Initial version | [c24f412] |
| 2026-10-07 | Deprecated | Jens Tirsvad Nielsen | S01 | Fixed Cost-Benefit justification and added completion constraint<br>Accepted after RC-001 (Go) | [c24f412] |
| 2026-11-15 | Accepted | Jens Tirsvad Nielsen | AI as stand-in for S01 | Added objective 5, success criterion 6, a scope item, a constraint and a risk for the baseline phase MIL-004; set the domain to education; the baseline phase is allowed to be committed and merged in autonomous mode; spelled out abbreviations; reviewed in autonomous mode, not independent | [5278b45] |

---

## Executive Summary

The Udemy course "100 Days of Code: The Complete Python Pro Bootcamp" asks
participants to build an object-oriented coffee machine program that uses
`Menu`, `CoffeeMaker` and `MoneyMachine` classes. This project delivers that
assignment as a small, readable, runnable Python repository that other course
participants and GitHub visitors can use as a reference solution.

## Methodological and Standards Foundation

Quality characteristics follow ISO/IEC 25010:2023. Planning follows the
framework in `framework/`: Business Case, Stakeholder Analysis, Project Plan,
milestones, tasks synced as issues, then code. Code follows the
`coding-conventions` skill (Python) and is reviewed against its
`qc-programming-*` checklist.

## Problem Statement

The course assignment is solved privately in the lesson editor. There is no
reproducible repository with tests, documentation and run instructions that a
fellow participant can clone and run, or that a GitHub visitor can browse.

## Business Opportunity

A clean, tested and documented repository lets participants compare solutions
and lets viewers find ideas, at the cost of a few hours of work.

## Objectives

1. Deliver a coffee machine program with the assignment's class and method names.
2. Cover the behaviour with automated pytest tests.
3. Document how to set up, run and test the project on Windows, Debian Linux and macOS.
4. Publish the repository with a description, topics and a README.
5. Bring the finished project to the common baseline of the framework: the adopted framework release, a wiki in English, Danish and Malay, the README in the framework template, complete licence metadata, a traceability matrix and review records ([MIL-004]).

## Scope

### In Scope

- Python 3.13+ package under `src/`, tests under `tests/`, documents under `docs/`.
- `pyproject.toml`, Python `.gitignore`, `constants.py`, Doxygen comments and a `Doxyfile`.
- A README following the course template, including `.venv` and `pip` instructions.
- Repository description and topics on the git host.
- The baseline phase [MIL-004]: framework release, wiki in English, Danish and Malay, README in the framework template, licence metadata, traceability matrix and review records. It changes no behaviour of the program.

### Out of Scope

- Runtime dependencies, a GUI or a database.
- Committing, pushing or merging by the assistant (the Product Owner does this), except in the baseline phase: there the Product Owner has authorised the assistant to commit, push, open the pull request and merge it in autonomous mode.
- Any change to `src/` or `tests/` in the baseline phase.
- Reading or testing the `.env` file from the project code.

## Expected Benefits

### Tangible Benefits

- A runnable program and a passing test suite.
- A README that reproduces setup in under five minutes.

### Intangible Benefits

- Practice of object-oriented design and a documented workflow.
- A reference other participants can learn from.

## Strategic Alignment

The project supports the Product Owner's learning goal of completing the
100 Days of Code bootcamp with a professional working method.

## Success Criteria

| # | Criterion | Target | Measure |
| --- | --- | --- | --- |
| 1 | Tests pass | 100 % of tests green | `pytest` exit code 0 |
| 2 | Runtime dependencies | 0 | `[project] dependencies` in `pyproject.toml` is empty |
| 3 | Setup reproducible | README steps work on a clean clone | Product Owner follows the README once |
| 4 | Assignment names kept | `get_items`, `find_drink`, `is_resource_sufficient`, `make_payment`, `make_coffee`, `report` present | Review of source |
| 5 | Repository presentable | Description and at least 3 topics set | Check on the git host |
| 6 | The baseline phase is done ([MIL-004]) | Wiki pages in 3 languages, `framework/scripts/check-readme.sh` exits with code 0, 100 % of the continuous integration (CI) checks of the pull request pass | Files in `docs/wiki/`, the script exit code and the pull request status on the git host |

## Risks

| Risk | Impact | Mitigation |
| --- | --- | --- |
| Token in `.env` leaks into the repository | High | `.env` stays in `.gitignore`; the code never reads it; it is used only for the sync tool |
| Tests drift from the assignment behaviour | Medium | Tests are written from the assignment text and reviewed against `qc-programming-python` |
| Doxygen is not installed on a viewer's machine | Low | The README documents the optional install; docs are not needed to run |
| The author is also the reviewer of the baseline documents | Medium: a defect is missed because the review is not independent | Every review record says `Mode: autonomous, not independent`, and the end-of-run summary lists it for challenge |

## Assumptions

- Python 3.13 or newer is available on the Product Owner's machine.
- The git host accepts the API token in `.env` for the sync.

## Constraints

- Python greater than 3.13, `venv`, `pytest`, `pyproject.toml`.
- Constants live in `constants.py`; source comments use Doxygen style.
- Folder structure `src/`, `tests/`, `docs/`; pull requests per step.
- Target completion 2026-10-16, the end of the last phase in [PP-001].
- The baseline phase [MIL-004] is finished within one week, by 2026-11-22.

## Cost–Benefit Assessment

| Costs | Benefits |
| --- | --- |
| A few hours of the Product Owner's time; no licence or hosting cost | Reusable reference repository and a documented working method |

The assessment is qualitative on purpose: this is a personal learning project with no revenue, budget or monetary cost to quantify.

## Stakeholders

| Stakeholder ID (SA) | Interest in this project |
| --- | --- |
| S01 | Completes the assignment with a professional method |
| S02 | Wants readable, runnable code and instructions |
| S03 | Wants a clear description, topics and README |

## Recommendation

Proceed — the scope is small, has no runtime dependencies and gives a lasting reference repository.

---

[SA-001]: ./stakeholder-analysis.md
[PP-001]: ./project-plan.md
[c24f412]: https://git.tirsystem.com/Tirsvad-Udemy-100_days_of_code/016-oop_coffee_machine/commit/c24f41207fb15f39b0ad6501e1f3126d3bd9232e
[MIL-004]: ./milestones/mil-004-framework-baseline.md
[5278b45]: https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/016-oop-coffee-machine/commit/5278b4588919b4665f72ef3eb43a7bb30d4d6c8d
