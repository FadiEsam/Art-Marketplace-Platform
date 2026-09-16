# Project Decision Log

## 1. Purpose

This document records important project-wide decisions that affect the scope, architecture, product behavior, technical direction, or long-term evolution of the Art Marketplace Platform.

The purpose of this log is to:

* Preserve the reasoning behind major decisions.
* Provide a historical record of project evolution.
* Prevent previously rejected or superseded ideas from being reintroduced accidentally.
* Provide a reliable reference for developers, contributors, and AI systems working with the repository.
* Make changes to project direction traceable.

This is a **project-wide decision log**.

Detailed implementation decisions that only affect a specific phase may be documented in that phase unless they have a broader impact on the project.

---

# 2. Decision Status

Each decision may have one of the following statuses:

| Status       | Meaning                                                                         |
| ------------ | ------------------------------------------------------------------------------- |
| `Accepted`   | The decision is currently approved and applicable.                              |
| `Superseded` | The decision was previously accepted but has been replaced by a newer decision. |
| `Rejected`   | The proposed option was explicitly rejected.                                    |
| `Deferred`   | The decision has not yet been finalized.                                        |
| `Deprecated` | The decision or capability is no longer intended to be used.                    |

A superseded decision should remain in the log for historical traceability.

---

# 3. Decision Format

Each decision should contain, where applicable:

* Decision ID.
* Title.
* Status.
* Date.
* Context.
* Decision.
* Rationale.
* Impact.
* Supersedes / Superseded by.

Dates should use the project's established date format.

---

# 4. Project-Wide Decisions

## DEC-001 — Project Direction

**Status:** `Accepted`

### Decision

The project is an Art Marketplace Platform intended to provide a structured marketplace experience connecting Customers and approved Artists.

The project is both:

* An educational and engineering project.
* A platform designed with potential future commercial use in mind.

The architecture and documentation should therefore support realistic software engineering practices while keeping the MVP sufficiently bounded.

---

## DEC-002 — MVP as a Web-Based Digital Art Marketplace

**Status:** `Accepted`

### Decision

The MVP will primarily be a Web-based marketplace focused on supported digital artwork.

The MVP should provide the minimum capabilities required for Customers and Artists to discover, publish, request, and transact around supported digital artwork.

### Rationale

This provides a manageable first product while establishing a foundation that can later support the broader platform.

---

## DEC-003 — Base User Role

**Status:** `Accepted`

### Decision

Every user begins as a Customer.

A Customer may apply to become an Artist.

An approved Artist may also continue using Customer functionality.

---

## DEC-004 — Artist Approval Process

**Status:** `Accepted`

### Decision

Users who want to become Artists must:

1. Select an artwork category.
2. Submit five samples of their own work.
3. Submit the application for specialist review.
4. Receive an approval or rejection decision.

An approved Artist may publish artwork within the approved category.

Detailed rejection, resubmission, similarity, suspension, and moderation rules are defined in the relevant requirements.

---

## DEC-005 — Artwork Scope

**Status:** `Accepted`

### Decision

The MVP supports digital artwork that can be represented and displayed as 2D visual content.

Examples include:

* Character drawings.
* Engineering drawings.
* Nature drawings.
* Photography.
* Arabic calligraphy.
* Digital drawings and paintings.
* Other supported digital 2D visual artwork.

---

## DEC-006 — Physical Artwork Boundary

**Status:** `Accepted`

### Decision

Physical artwork is not supported as a platform-managed marketplace transaction in the MVP.

Artists may display physical artwork as part of their portfolio where appropriate.

If an Artist and Customer arrange a physical artwork sale independently, that transaction occurs outside the platform.

The platform does not manage:

* The physical payment.
* Physical delivery.
* Physical order fulfillment.
* The external transaction.

### Future Scope

Future versions may support platform-managed physical artwork transactions.

---

## DEC-007 — Unsupported Non-2D Artwork Forms

**Status:** `Accepted`

### Decision

Three-dimensional or non-2D-display artwork forms such as:

* Sculpture.
* Carving.
* Sewing.
* Pottery.
* Similar physical/non-2D forms.

are outside the current project scope unless a future project decision explicitly changes this boundary.

---

## DEC-008 — Ready-Made Digital Artwork

**Status:** `Accepted`

### Decision

The MVP supports ready-made digital artwork.

Artists may publish existing digital works for Customers according to the approved marketplace rules.

Detailed purchase, payment-related, ownership, usage-rights, and digital-delivery workflows are defined during Requirements.

---

## DEC-009 — Custom Digital Artwork

**Status:** `Accepted`

### Decision

The MVP supports custom digital artwork requests and commissions.

Artists may indicate whether they are available to accept custom requests.

The detailed workflow may include:

* Request.
* Requirements.
* Artist acceptance.
* Pricing.
* Work progress.
* Submission.
* Revisions.
* Final approval.
* Completion.

Exact workflow rules are defined during Requirements.

---

## DEC-010 — Dynamic Artwork Metadata

**Status:** `Accepted`

### Decision

The MVP may use a dynamic, rule-based artwork metadata/question flow.

The system may present additional questions or metadata fields based on:

* Artwork category.
* Previous answers.
* Artwork characteristics.
* Predefined rules.

The artwork category is the fundamental required classification.

Additional metadata may be optional or conditionally required depending on the selected category and answers.

### Important Constraint

This functionality does not require AI.

The Artist remains responsible for reviewing and modifying the resulting metadata.

---

## DEC-011 — Payment Model for MVP

**Status:** `Accepted`

### Decision

The MVP will not use platform-mediated payment processing.

Customers pay Artists directly through bank transfer.

The platform records the relevant transaction and commission information without acting as the payment processor.

### Future Scope

Future versions may introduce platform-mediated payment processing and payment-provider integrations.

---

## DEC-012 — Platform Commission

**Status:** `Accepted`

### Decision

The platform commission is **15%** according to the approved MVP marketplace model.

The platform records the commission obligation associated with relevant Artist transactions.

Outstanding commission obligations may result in restrictions on selected marketplace capabilities.

Exact enforcement thresholds and rules are defined during Requirements.

---

## DEC-013 — Printing Integration

**Status:** `Accepted`

### Decision

Printing integration is outside the MVP.

### Future Scope

Future versions may integrate with external printing or print-on-demand providers.

Possible future capabilities include:

* Printing digital artwork.
* Print products.
* Print-order management.
* Printing-provider integration.

---

## DEC-014 — Delivery and Logistics Integration

**Status:** `Accepted`

### Decision

Delivery and logistics integration is outside the MVP.

The MVP does not include:

* Delivery-provider integration.
* Shipment tracking.
* Physical logistics management.
* Printing-to-customer logistics.

### Future Scope

Future versions may integrate with external delivery and logistics providers.

---

## DEC-015 — Social Features

**Status:** `Accepted`

### Decision

The MVP includes the following social capabilities:

* Like.
* Follow.
* 1–5 star Rating.
* Customizable Notifications.
* Report.
* Block User.

The MVP does not include:

* Dislike.
* Comments.
* Spam functionality.
* User-to-user chat.
* User-to-AI chat.

The platform is not intended to operate as a general-purpose social network.

---

## DEC-016 — AI Exclusion from MVP

**Status:** `Accepted`

### Decision

AI functionality is outside the MVP.

No AI capability should be introduced into the MVP unless the project scope is formally changed.

### Future Scope

Potential future AI capabilities may include:

* Personalized recommendations.
* Artist recommendations.
* Artist/customer matching.
* Artwork analysis.
* AI-assisted metadata.
* AI-generated descriptions.
* AI-assisted moderation.
* AI customer assistance.
* AI chat.
* AI-assisted artwork creation.
* Other AI-assisted marketplace capabilities.

These are future possibilities and are not approved MVP requirements.

---

## DEC-017 — Mobile Application as a Core Project Phase

**Status:** `Accepted`

### Decision

The Mobile Application is a **core project phase**.

It is outside the initial MVP, but it is part of the intended complete project.

It must not be classified as:

* Optional.
* Merely a future idea.
* A future product extension.

The Mobile Application is planned as **Phase 07** after the Web Frontend phase.

### Rationale

The project is intended to demonstrate a broader software engineering lifecycle rather than only a Web MVP.

The backend/API should therefore be designed with future Mobile consumption in mind.

---

## DEC-018 — Complete Project vs MVP

**Status:** `Accepted`

### Decision

The MVP and the complete project are not the same thing.

The MVP represents the first functional product milestone.

The complete project includes the broader engineering lifecycle:

```text id="1h9l7j"
00 Project Foundation
        ↓
01 Requirements
        ↓
02 System Design
        ↓
03 UI/UX Design
        ↓
04 Database
        ↓
05 API / Backend
        ↓
06 Web Frontend
        ↓
07 Mobile Application
        ↓
08 Quality Assurance
        ↓
09 Cybersecurity
        ↓
10 Deployment
        ↓
11 Maintenance
```

---

## DEC-019 — Future Product Capabilities Remain Outside Core MVP

**Status:** `Accepted`

### Decision

The following capabilities remain outside the MVP and should be treated as future product development unless explicitly promoted through a later scope decision:

* Platform-mediated payments.
* Payment-provider integration.
* Platform-managed physical artwork transactions.
* Printing integration.
* Print-on-demand.
* Delivery integration.
* Shipment tracking.
* AI functionality.
* Advanced recommendation systems.
* Advanced personalization.
* Other advanced marketplace capabilities.

### Rationale

These capabilities may provide future value but are not required to establish the approved MVP marketplace.

---

## DEC-020 — Auction Exclusion

**Status:** `Accepted`

### Decision

Auction functionality is not part of the current MVP or core project design.

The project documentation, architecture, database, UI/UX, API, and implementation must not introduce auction functionality unless the user explicitly requests reconsideration and a new project decision approves it.

The idea may be mentioned only as a possible future product idea alongside other future capabilities if appropriate.

---

## DEC-021 — Dynamic Metadata Does Not Imply AI

**Status:** `Accepted`

### Decision

The dynamic artwork metadata feature should initially be designed as a deterministic/rule-based system.

It should not be described as an AI feature.

AI-assisted metadata may be considered independently as future functionality.

### Rationale

This allows the MVP to provide structured artwork information without introducing unnecessary AI dependencies.

---

## DEC-022 — Future Physical Marketplace Services

**Status:** `Accepted`

### Decision

Physical marketplace expansion may eventually involve multiple external services rather than a single integrated platform workflow.

Potential future services include:

```text id="i1o4o4"
Artist / Customer
       ↓
Platform
       ↓
Printing Provider
       ↓
Delivery Provider
       ↓
Customer
```

Depending on the future business model, delivery may also originate directly from the Artist.

Printing and delivery are therefore treated as separate future service domains.

---

## DEC-023 — Project-Wide Documentation Principle

**Status:** `Accepted`

### Decision

General project-wide decisions, boundaries, and principles should be documented at the repository root where appropriate.

Phase-specific documents should focus on the concerns of their respective phases.

Project-wide information should not be unnecessarily duplicated across multiple phases.

---

## DEC-024 — Phase Documents Should Avoid Temporal Project Status

**Status:** `Accepted`

### Decision

Phase documentation should not contain changing project-status statements such as:

* Current phase.
* Previous phase.
* Percentage of completion.
* Current progress.
* Temporary implementation status.

These belong in root-level project tracking documentation such as `README.md` and `ROADMAP.md`.

Phase documents should primarily describe stable scope, requirements, decisions, and technical information relevant to their phase.

---

## DEC-025 — Detailed Future Features Require Future Decisions

**Status:** `Accepted`

### Decision

Mentioning a capability in Future Product Scope does not constitute approval to implement it.

Future capabilities require their own:

* Requirements.
* Technical evaluation.
* Security evaluation.
* Legal evaluation where applicable.
* Architecture decisions.
* Implementation planning.

This applies particularly to:

* AI.
* Platform-mediated payments.
* Physical marketplace transactions.
* Printing.
* Delivery.
* Advanced recommendation systems.

---

# 5. Superseded Decisions

Historical decisions that no longer represent the current project direction should remain documented and explicitly marked as superseded.

A superseded decision must not be treated as current scope.

When a decision is superseded:

1. Keep the original decision.
2. Change its status to `Superseded`.
3. Identify the decision that replaced it.
4. Ensure affected project documents are updated.
5. Preserve the historical rationale where useful.

---

# 6. Decision Precedence

When project documentation contains conflicting information, the following principle should be applied:

1. The latest accepted project-wide decision takes precedence over an older conflicting decision.
2. Superseded decisions are historical and must not be treated as current requirements.
3. Root-level project-wide decisions take precedence over outdated phase-level assumptions.
4. Detailed requirements may refine an approved decision but must not contradict it.
5. A change to an approved project-wide boundary should be recorded as a new decision.

---

# 7. Decision Maintenance

The decision log should be updated when a project-wide decision:

* Changes MVP scope.
* Changes complete-project scope.
* Changes a major architectural direction.
* Introduces or removes a major platform capability.
* Changes an explicit project boundary.
* Supersedes an earlier project-wide decision.

Normal editing, wording improvements, documentation cleanup, and implementation progress do not require a new decision entry unless they change an approved project-wide decision.

---

# 8. Current High-Level Decision Summary

The current project direction can be summarized as:

```text id="5z5a7v"
MVP
│
├── Web-based marketplace
├── Digital 2D artwork
├── Ready-made digital artwork
├── Custom digital artwork
├── Artist approval
├── Dynamic rule-based metadata
├── Search and discovery
├── Like
├── Follow
├── 1–5 star Rating
├── Customizable Notifications
├── Report
├── Block User
├── Direct bank transfer
├── 15% Artist commission
└── Basic marketplace administration


Complete Core Project
│
├── MVP
├── Backend / API
├── Database
├── Web Frontend
├── Mobile Application
├── Quality Assurance
├── Cybersecurity
├── Deployment
└── Maintenance


Future Product Scope
│
├── Platform-mediated payments
├── Physical marketplace transactions
├── Printing
├── Delivery / Logistics
├── AI capabilities
├── Advanced recommendations
├── Advanced personalization
└── Other future marketplace capabilities
```

The above summary is derived from the accepted decisions in this document and should remain consistent with the root README, roadmap, and project-scope documentation.
