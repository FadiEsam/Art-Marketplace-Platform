# Decision Log

## 1. Purpose

This document records significant decisions made during the development of the Art Marketplace Platform.

The purpose of the decision log is to:

* Preserve the reasoning behind important project decisions.
* Prevent previously resolved questions from being repeatedly revisited.
* Make project decisions traceable.
* Identify decisions that may need to be revisited later.
* Distinguish confirmed decisions from assumptions and unresolved topics.
* Maintain consistency across requirements, design, implementation, testing, and deployment.

Not every implementation detail requires an entry in this document. Decisions should be recorded when they have a meaningful impact on project scope, architecture, security, technology, business behavior, or future development.

---

# 2. Decision Status

Each decision may have one of the following statuses:

| Status     | Meaning                                                              |
| ---------- | -------------------------------------------------------------------- |
| Proposed   | A possible decision has been identified but not approved.            |
| Accepted   | The decision has been approved and should guide subsequent work.     |
| Superseded | A previous decision has been replaced by another decision.           |
| Rejected   | The proposed decision was explicitly rejected.                       |
| TBD        | The subject is intentionally undecided and requires future analysis. |

---

# 3. Decision Record Format

Each significant decision should contain:

* **Decision ID**
* **Date**
* **Title**
* **Status**
* **Context**
* **Decision**
* **Rationale**
* **Consequences**
* **Related Documents**

Decisions should be updated when new information materially changes the original reasoning.

---

# 4. Accepted Decisions

## DEC-001 — Use a Controlled MVP Scope

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform has significant potential for additional features, including AI, social functionality, advanced recommendations, complex marketplace economics, dispute management, and other capabilities.

Implementing all potential features in the first release would increase development time and complexity and make it difficult to determine whether the core marketplace concept works.

### Decision

The project will use a **controlled MVP scope**.

The MVP will focus on the minimum capabilities required to validate the core marketplace workflow.

### Core MVP Workflow

```text
Discovery
   ↓
Request / Purchase
   ↓
Order
   ↓
Payment
   ↓
Production / Delivery
   ↓
Review
   ↓
Revision or Approval
   ↓
Completion
```

### Rationale

A controlled MVP:

* Reduces unnecessary complexity.
* Makes the project measurable.
* Allows the core workflow to be validated.
* Prevents feature creep.
* Supports completion of the project within a realistic scope.

### Consequences

Features outside the MVP must not be added casually.

Additional functionality must either:

* Be classified as future work, or
* Go through a documented scope-change decision.

### Related Documents

* `00-project-foundation/project-scope.md`
* `00-project-foundation/project-objectives.md`
* `ROADMAP.md`

---

## DEC-002 — Requirements Must Precede Implementation

**Date:** Project Foundation
**Status:** Accepted

### Context

Beginning implementation before understanding the required behavior can result in inconsistent architecture, database changes, rework, and uncontrolled scope growth.

### Decision

The project will follow a requirements-first approach.

Requirements must be sufficiently defined before implementation of the corresponding system functionality begins.

### Rationale

This supports:

* Better system design.
* Traceability.
* Reduced rework.
* Clear acceptance criteria.
* More reliable testing.

### Consequences

Implementation work should not be used as a substitute for requirements analysis.

Where requirements are incomplete, the missing requirements should be resolved or explicitly marked as TBD before the affected implementation begins.

### Related Documents

* `01-requirements/`
* `02-system-design/`

---

## DEC-003 — Use Phase Gates

**Date:** Project Foundation
**Status:** Accepted

### Context

The project contains multiple engineering phases. Moving to the next phase without completing the previous one can cause unresolved requirements and design problems to propagate into later work.

### Decision

Each major project phase will contain a `gate.md` document defining completion criteria.

A phase is considered complete only when its Gate criteria have been satisfied.

### Rationale

Phase Gates provide:

* Controlled progression.
* Quality checkpoints.
* Explicit completion criteria.
* Early identification of problems.
* Better learning discipline.

### Consequences

A failed Gate requires corrective work before progression.

The existence of documentation files alone does not mean that a phase is complete.

### Related Documents

All phase-level `gate.md` files.

---

## DEC-004 — Maintain Requirements-to-Test Traceability

**Date:** Project Foundation
**Status:** Accepted

### Context

The project is intended to demonstrate professional software engineering practices, not only application development.

Therefore, requirements should be connected to their implementation and verification.

### Decision

Important requirements will be traceable through:

```text
Objective
   ↓
Requirement
   ↓
Design
   ↓
Implementation
   ↓
Test
   ↓
Result
```

### Rationale

Traceability improves:

* Requirement coverage.
* Test completeness.
* Change impact analysis.
* Documentation quality.
* Project credibility.

### Consequences

The requirements phase will contain a requirements traceability mechanism, and testing documentation will reference the relevant requirements.

### Related Documents

* `01-requirements/requirements-traceability.md`
* `08-quality-assurance/`

---

## DEC-005 — Backend API as the Core Application Interface

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform initially targets the web, but a mobile application is planned as a future platform.

Building business logic exclusively inside the web frontend would make future clients more difficult to support.

### Decision

The backend will expose an API that serves as the primary application interface.

The web frontend will consume the backend API, and a future mobile application should be able to consume the same backend.

### Rationale

This approach:

* Separates presentation from business logic.
* Supports multiple clients.
* Simplifies future mobile development.
* Centralizes authorization and business rules.
* Creates a clearer system architecture.

### Consequences

Business-critical rules must be enforced by the backend rather than relying only on frontend behavior.

### Related Documents

* `02-system-design/system-architecture.md`
* `05-api-backend/`
* `06-web-frontend/`
* `07-mobile-app/`

---

## DEC-006 — Use a Relational Database Direction

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform contains structured transactional relationships involving users, artists, artworks, services, orders, payments, revisions, reviews, and other entities.

### Decision

The project will use a relational database architecture.

**PostgreSQL** is the current preferred technology.

The final database technology decision will be confirmed during the database and system-design phases.

### Rationale

A relational model is appropriate for:

* Structured transactional data.
* Relationships between entities.
* Referential integrity.
* Transaction processing.
* Complex queries.
* Consistent business data.

### Consequences

The database design will emphasize:

* Proper relationships.
* Constraints.
* Normalization where appropriate.
* Indexing.
* Transaction integrity.
* Security.

### Related Documents

* `04-database/`
* `02-system-design/`

---

## DEC-007 — Do Not Store Large Artwork Files Directly in the Relational Database

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform is expected to handle artwork and other potentially large files.

Storing large binary files directly inside the primary relational database could unnecessarily increase database size and complicate storage and operational management.

### Decision

Large artwork and media files should be stored using dedicated file/object storage.

The relational database will store the metadata and references necessary to manage those files.

### Rationale

This approach supports:

* Better storage management.
* Independent file scaling.
* More efficient database operations.
* Easier backup and operational management.

### Consequences

A file/object storage provider or solution will be selected during the relevant technical phases.

The final provider is currently **TBD**.

### Related Documents

* `04-database/`
* `10-deployment/`

---

## DEC-008 — Use a Third-Party Payment Provider

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform needs to support customer payments.

Developing and operating a proprietary payment-processing system would introduce significant security, regulatory, financial, and technical complexity.

### Decision

Payments will be processed through a third-party Payment Service Provider (PSP).

The platform will integrate with the selected provider rather than implementing payment processing itself.

### Rationale

This reduces:

* Payment infrastructure complexity.
* Security exposure.
* Regulatory complexity.
* Development effort.

### Consequences

The final payment provider is **TBD**.

The architecture must allow payment-provider integration without tightly coupling the entire application to one provider where practical.

### Related Documents

* `01-requirements/business-rules.md`
* `05-api-backend/`
* `09-cybersecurity/`

---

## DEC-009 — Keep Payment Status Separate from Order Status

**Date:** Project Foundation
**Status:** Accepted

### Context

An order has an operational lifecycle, while a payment has a financial lifecycle.

Treating both as one status can produce ambiguous system behavior.

### Decision

Payment status and order status will be modeled as separate concepts.

For example:

```text
Order Status:

Production


Payment Status:

Paid
```

These states may coexist without representing the same information.

### Rationale

The separation improves:

* Domain clarity.
* Database design.
* API design.
* Business-rule enforcement.
* Payment-provider integration.
* Future financial workflows.

### Consequences

Requirements and database design must explicitly model the distinction.

---

## DEC-010 — Fund Holding Is Not Assumed to Be Legal Escrow

**Date:** Project Foundation
**Status:** Accepted

### Context

The intended marketplace concept may involve receiving customer funds through the platform and retaining the corresponding transaction state until contractual conditions are satisfied.

However, technically holding or controlling funds does not automatically make the platform a legally recognized escrow service.

### Decision

The project may design an escrow-like payment workflow conceptually, but it will not assume that the platform is legally providing escrow services.

The actual model must depend on:

* Payment-provider capabilities.
* Applicable regulations.
* Legal requirements.
* Contractual structure.

### Rationale

This prevents the technical design from making unsupported legal assumptions.

### Consequences

The final payment flow cannot be finalized until the payment and legal model has been validated.

### Status of Final Implementation Model

**TBD**

---

## DEC-011 — Enforce Authorization on the Server

**Date:** Project Foundation
**Status:** Accepted

### Context

Frontend interfaces can be modified or bypassed by users.

Therefore, frontend restrictions alone cannot be treated as a security boundary.

### Decision

Authorization must be enforced on the backend/server.

The backend must validate:

* User identity.
* User role.
* Resource ownership.
* Requested operation.
* Relevant business rules.

### Rationale

Server-side authorization provides the authoritative security boundary.

### Consequences

Every protected API operation must be designed with authorization requirements.

---

## DEC-012 — Resource Ownership Must Be Verified

**Date:** Project Foundation
**Status:** Accepted

### Context

Users may have access to resources belonging to their accounts or orders.

Knowing that a user is authenticated does not automatically mean that the user is authorized to access every resource.

### Decision

The backend must perform resource ownership or equivalent access checks wherever required.

Example:

```text
Authenticated Customer
       ↓
Requests Order #123
       ↓
Backend verifies access
       ↓
Customer owns/is authorized for Order #123
```

### Rationale

This reduces unauthorized access to private user and transaction data.

### Consequences

Ownership checks must be included in API authorization design and security testing.

---

## DEC-013 — Production Secrets Must Not Be Stored in Source Control

**Date:** Project Foundation
**Status:** Accepted

### Context

The repository may be publicly accessible as part of the project's portfolio and learning goals.

Including credentials or secrets in source control would create a significant security risk.

### Decision

Secrets must not be committed to the Git repository.

Examples include:

* Database passwords.
* API keys.
* Payment credentials.
* Authentication secrets.
* Production service credentials.

### Rationale

Source control should contain reproducible application code and configuration structure, not sensitive credentials.

### Consequences

Environment variables, secret-management mechanisms, or other secure configuration mechanisms will be used.

---

## DEC-014 — HTTPS Is Required in Production

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform will handle authentication, user information, orders, and payment-related communication.

### Decision

Production traffic must use HTTPS.

### Rationale

HTTPS protects communication between clients and the production platform and is a basic requirement for a system handling authenticated and transactional data.

### Consequences

Production deployment must include TLS/SSL configuration.

### Related Documents

* `09-cybersecurity/`
* `10-deployment/ssl.md`

---

## DEC-015 — Separate Development and Production Environments

**Date:** Project Foundation
**Status:** Accepted

### Context

Development activities may involve debugging, testing, experimental changes, and non-production data.

Mixing development and production environments increases operational and security risks.

### Decision

Development and production environments must be logically separated.

A testing environment may also be introduced as required.

### Rationale

Environment separation helps prevent:

* Accidental production changes.
* Exposure of production data.
* Configuration conflicts.
* Unsafe testing activities.

### Consequences

Environment-specific configuration must be maintained separately.

---

## DEC-016 — Production Data Must Not Be Casually Used in Development

**Date:** Project Foundation
**Status:** Accepted

### Context

Production data may contain personal, transactional, or otherwise sensitive information.

### Decision

Production data must not be copied into development environments casually.

If production-derived data is required for testing, it must be appropriately controlled, sanitized, anonymized, or otherwise approved according to the applicable security requirements.

### Rationale

This reduces privacy and security risks.

---

## DEC-017 — Document Important Architectural Decisions

**Date:** Project Foundation
**Status:** Accepted

### Context

Technical decisions can affect multiple later phases and may otherwise become difficult to understand or reproduce.

### Decision

Important architectural decisions will be documented using Architecture Decision Records (ADRs).

### Rationale

ADRs preserve:

* Context.
* Alternatives.
* Reasoning.
* Consequences.

They also demonstrate professional architecture practices.

### Related Documents

`02-system-design/architecture-decisions/`

---

## DEC-018 — Avoid Premature Overengineering

**Date:** Project Foundation
**Status:** Accepted

### Context

The platform is intended to be scalable and professionally designed, but attempting to solve hypothetical large-scale problems before validating the MVP could unnecessarily increase complexity.

### Decision

The architecture will be designed with reasonable extensibility but will avoid unnecessary complexity that is not justified by current requirements.

### Rationale

The goal is to balance:

```text
Maintainability
+
Security
+
Extensibility
+
Practical MVP Scope
```

without introducing infrastructure or architectural complexity solely for hypothetical future scale.

### Consequences

Future scalability requirements should be addressed when they become justified by actual requirements or measured system needs.

---

# 5. Explicitly Undecided Decisions

The following topics are intentionally not finalized at the Project Foundation phase.

They must not be treated as confirmed implementation decisions.

| Topic                                 | Status |
| ------------------------------------- | ------ |
| Final payment provider                | TBD    |
| Exact payment model                   | TBD    |
| 50% vs. 100% upfront payment          | TBD    |
| Fund-release mechanism                | TBD    |
| Legal escrow model                    | TBD    |
| Platform commission model             | TBD    |
| Payment processing fee responsibility | TBD    |
| Refund policy                         | TBD    |
| Cancellation policy                   | TBD    |
| Dispute-resolution workflow           | TBD    |
| Geographic launch scope               | TBD    |
| Supported currencies                  | TBD    |
| Supported languages                   | TBD    |
| Storage provider                      | TBD    |
| Notification provider                 | TBD    |
| Hosting provider                      | TBD    |
| Final technology stack                | TBD    |
| Mobile technology                     | TBD    |
| Exact artwork categories              | TBD    |
| Exact service model                   | TBD    |
| Intellectual-property/licensing rules | TBD    |

These topics should be resolved through the appropriate requirements, architecture, legal, or technical decision process rather than assumed during implementation.

---

# 6. Decision-Making Principles

Future project decisions should follow these principles:

### 6.1 Requirements First

A technical decision should be based on an identified requirement whenever possible.

### 6.2 Simplicity Before Complexity

Prefer the simplest solution that satisfies the actual requirements.

### 6.3 Security by Design

Security requirements should influence architecture and implementation from the beginning rather than being added only after development.

### 6.4 Replaceability Where Practical

External services should be integrated in a way that avoids unnecessary coupling where reasonable.

### 6.5 Document Significant Trade-offs

When multiple technically valid options exist, the important trade-offs should be documented.

### 6.6 Avoid Premature Commitment

A decision should remain TBD when insufficient information exists to make a responsible final decision.

### 6.7 Maintain Traceability

Important decisions should be traceable to the requirements, constraints, or objectives that motivated them.

---

# 7. Decision Review

A decision may be revisited when:

* New requirements are introduced.
* A major technical limitation is discovered.
* A selected external provider becomes unsuitable.
* Security analysis identifies a significant issue.
* Legal or regulatory requirements change.
* Project scope changes materially.
* Testing demonstrates that the decision does not satisfy the intended requirements.

When a decision is replaced, the original record should remain in this document and its status should be changed to **Superseded** rather than deleted.

This preserves the historical reasoning of the project.

---

# 8. Current Decision Baseline

At the end of the Project Foundation phase, the project has established the following baseline:

```text
Controlled MVP
     ↓
Requirements First
     ↓
Phase Gates
     ↓
Traceable Engineering Process
     ↓
Backend API as Core Application Interface
     ↓
Relational Database Direction
     ↓
External Object/File Storage
     ↓
Third-Party Payment Provider
     ↓
Separate Payment and Order States
     ↓
Server-Side Authorization
     ↓
Resource Ownership Checks
     ↓
Secure Secret Management
     ↓
HTTPS in Production
     ↓
Separated Environments
     ↓
Documented Architectural Decisions
     ↓
Avoid Premature Overengineering
```

This baseline will guide the next project phases unless a documented decision supersedes one of these decisions.
