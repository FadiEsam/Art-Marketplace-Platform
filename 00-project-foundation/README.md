# Project Foundation

## Purpose

The Project Foundation defines the fundamental direction, boundaries, assumptions, constraints, stakeholders, and decisions of the Art Marketplace Platform before detailed requirements and implementation begin.

This phase establishes a common baseline for the project and provides the context required for the subsequent requirements and system design phases.

---

## Objectives

The Foundation phase aims to:

* Define the overall purpose and vision of the project.
* Establish the initial project scope and MVP boundaries.
* Identify project stakeholders and their responsibilities.
* Document assumptions and constraints.
* Establish a shared project vocabulary.
* Record important architectural and business decisions.
* Define the criteria required to complete the Foundation phase.

---

## Foundation Documents

| Document                | Purpose                                                                             |
| ----------------------- | ----------------------------------------------------------------------------------- |
| `project-charter.md`    | Defines the project purpose, vision, goals, stakeholders, and high-level direction. |
| `project-scope.md`      | Defines what is included in and excluded from the project and MVP.                  |
| `project-objectives.md` | Defines product, business, technical, and educational objectives.                   |
| `stakeholders.md`       | Identifies stakeholders and their interests or responsibilities.                    |
| `assumptions.md`        | Documents assumptions made during project planning.                                 |
| `constraints.md`        | Documents known technical, business, legal, operational, and project constraints.   |
| `glossary.md`           | Defines important terms and terminology used throughout the project.                |
| `gate.md`               | Defines the completion criteria and approval conditions for the Foundation phase.   |

---

## Foundation Principles

The project follows these principles during the Foundation phase:

1. **Define before implementing**

   Important project decisions should be understood before implementation begins.

2. **Control the MVP**

   Features should be included only when they are necessary to validate the core marketplace workflow.

3. **Document important decisions**

   Significant technical and business decisions should be recorded rather than left implicit.

4. **Avoid premature overengineering**

   The architecture should support expected growth without implementing unnecessary complexity.

5. **Maintain traceability**

   Project objectives should eventually be traceable through requirements, design, implementation, and testing.

6. **Use phase gates**

   A phase should not be considered complete until its defined completion criteria have been satisfied.

7. **Record uncertainty explicitly**

   Decisions that depend on future validation, external providers, legal requirements, or business decisions should remain documented as TBD rather than being assumed.

---

## Foundation Outputs

At the completion of this phase, the project should have:

* A defined project purpose.
* A documented MVP boundary.
* Identified stakeholders.
* Documented assumptions.
* Documented constraints.
* A shared project glossary.
* A decision history.
* A Foundation Gate evaluation.
* A clear starting point for the Requirements phase.

---

## Phase Status

**Current Status:** Completed / Pending Gate Verification

**Next Phase:** `01-requirements/`

The Requirements phase may begin once the Foundation Gate has been successfully passed.

---

## Related Project Documents

The Foundation phase is connected to the following project-level documents:

* `../README.md`
* `../ROADMAP.md`
* `../CHANGELOG.md`
* `../LICENSE`

These documents provide project-level context, while the files in this directory define the detailed foundation baseline.

---

## Change Management

Changes to the Foundation baseline should be documented when they affect:

* Project scope.
* MVP boundaries.
* Major stakeholders.
* Fundamental assumptions.
* Important constraints.
* Architectural direction.
* Major business rules.
* Previously accepted decisions.

Significant changes should be recorded in `decision-log.md` and reflected in the relevant Foundation document.

---

## Completion Rule

The Foundation phase is considered complete only when the criteria defined in `gate.md` have been reviewed and the phase has received a **PASS** or an explicitly accepted **CONDITIONAL PASS**.

A failed gate requires corrective work before progressing to the Requirements phase.
