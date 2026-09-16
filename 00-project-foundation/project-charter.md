# Project Charter

## 1. Project Information

| Item                     | Details                                                                                        |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| Project Name             | Art Marketplace Platform                                                                       |
| Project Type             | Full-Stack Art Marketplace Platform                                                            |
| Primary MVP Client       | Web Application                                                                                |
| Complete Project Clients | Web Application + Mobile Application                                                           |
| Project Purpose          | Educational software engineering project with potential commercial evolution                   |
| Project Lifecycle        | Foundation → Requirements → Design → Implementation → QA → Security → Deployment → Maintenance |
| Current Document Role    | Project Foundation Charter                                                                     |

---

# 2. Project Overview

The Art Marketplace Platform is a full-stack software project intended to provide a structured environment for customers and artists to discover, present, request, purchase, and manage supported artwork.

The platform is designed around a unified user account model.

Every user begins with customer capabilities and may later apply for artist capabilities through an approval process.

The initial MVP focuses on a web-based marketplace for supported digital artwork.

The complete project continues beyond the MVP and includes development of a Mobile Application as an important project phase and learning objective.

The project therefore distinguishes between:

* **MVP Scope** — the initial product required to validate the core marketplace.
* **Complete Project Scope** — the broader software engineering project, including the Mobile Application and subsequent engineering phases.
* **Future Product Scope** — capabilities intentionally deferred beyond the current project scope.

---

# 3. Problem Statement

Artists and customers may rely on fragmented platforms and informal processes when discovering artwork, presenting artistic work, requesting custom artwork, and managing transactions.

This can result in:

* Difficulty discovering suitable artists.
* Limited structured artist portfolios.
* Inconsistent artwork information.
* Difficulty comparing and filtering artwork.
* Unstructured custom-artwork requests.
* Lack of a consistent marketplace workflow.
* Difficulty managing orders and requests.
* Limited structured interaction and notification mechanisms.
* Unclear responsibilities between customers, artists, and the platform.

The proposed platform aims to provide a structured marketplace that organizes these activities into defined workflows while maintaining controlled MVP scope.

---

# 4. Project Vision

The vision is to build a structured art marketplace that allows customers to discover artists and artwork while giving approved artists tools to present, manage, and offer supported creative work.

The long-term product direction is to evolve the platform into a broader marketplace capable of supporting additional artwork types, transaction mechanisms, services, clients, and integrations.

The initial implementation deliberately focuses on a controlled MVP rather than attempting to implement the complete long-term product immediately.

---

# 5. Project Purpose

The project has two closely related purposes.

## 5.1 Product Purpose

To design and build a functional art marketplace platform with clearly defined customer, artist, marketplace, moderation, and administrative workflows.

## 5.2 Engineering and Learning Purpose

To demonstrate the complete software engineering lifecycle through a realistic multi-phase project.

The project covers:

1. Project Foundation.
2. Requirements Engineering.
3. System Design.
4. UI/UX Design.
5. Database Design.
6. API and Backend Development.
7. Web Frontend Development.
8. Mobile Application Development.
9. Quality Assurance.
10. Cybersecurity.
11. Deployment.
12. Maintenance and Evolution.

The Mobile Application is an important part of the learning and engineering objectives even though it is outside the MVP.

---

# 6. Project Objectives

The project aims to:

* Establish a clear and controlled product scope.
* Define detailed and traceable requirements.
* Design a maintainable system architecture.
* Build a secure REST API.
* Design and implement a relational database.
* Build a functional web marketplace.
* Develop a mobile client using the established backend services.
* Apply professional UI/UX practices.
* Apply systematic testing and quality assurance.
* Apply cybersecurity practices.
* Deploy the system using documented procedures.
* Establish maintainable project documentation.
* Document important technical and product decisions.
* Demonstrate the ability to develop a software product through a complete engineering lifecycle.

---

# 7. Product Scope Model

The project is divided conceptually into three scope levels.

## 7.1 MVP

The MVP is the initial web-based marketplace.

It focuses on:

* User registration and authentication.
* Customer capabilities.
* Artist application and approval.
* Artist profiles.
* Digital artwork.
* Artwork discovery.
* Search and filtering.
* Ready-made digital artwork.
* Supported custom digital artwork.
* Artwork metadata.
* Marketplace workflows.
* Orders and requests.
* Approved social features.
* Notifications.
* Reporting and blocking.
* Administration and moderation.
* Direct customer-to-artist payment.
* Platform commission tracking.

---

## 7.2 Complete Project

The complete project includes the MVP and the remaining planned engineering phases.

The complete project includes:

* Web Application.
* Mobile Application.
* Backend/API.
* Database.
* Quality Assurance.
* Cybersecurity.
* Deployment.
* Maintenance.

The Mobile Application is therefore part of the project scope even though it is outside the MVP.

---

## 7.3 Future Product Scope

Potential future product capabilities include:

* Platform-mediated payment.
* Expanded physical-art marketplace support.
* Printing integrations.
* Delivery integrations.
* AI-assisted capabilities.
* Advanced marketplace features.
* Additional external-service integrations.

These capabilities are not current MVP commitments.

---

# 8. User Model

The platform uses a unified account model.

## 8.1 Base User

Every registered user begins with customer capabilities.

A user may apply for artist capabilities without creating a separate account.

Conceptually:

```text id="5j5kqk"
User
├── Customer capabilities
└── Artist capabilities
       └── Granted after approval
```

An approved artist can continue to use the platform as a customer.

---

## 8.2 Artist Approval

Artist capabilities are granted through an approval process.

The intended high-level process is:

```text id="r0t9y7"
User
 ↓
Artist Application
 ↓
Select Artistic Category
 ↓
Submit 5 Self-Owned Samples
 ↓
Specialist Review
 ↓
Approval / Rejection
 ↓
Artist Capabilities
```

An approved artist may publish artwork within the approved artistic category subject to the platform's rules.

Detailed approval, rejection, resubmission, similarity, and moderation rules belong to Requirements.

---

# 9. Artwork Scope

## 9.1 MVP Marketplace Artwork

The MVP marketplace focuses on digital artwork that can be represented and displayed as 2D visual content.

Examples include:

* Character drawings.
* Digital drawings and paintings.
* Engineering drawings.
* Nature artwork.
* Photography.
* Arabic calligraphy.
* Other supported digital 2D artwork.

The exact artwork categories and metadata requirements are defined in Requirements.

---

## 9.2 Ready-Made Artwork

Ready-made artwork is an existing completed artwork offered by an artist.

Its detailed purchase and delivery workflow will be defined in Requirements and System Design.

---

## 9.3 Custom Artwork

Custom artwork represents work created according to a customer's request.

Custom artwork may differ from ready-made artwork in:

* Request workflow.
* Payment conditions.
* Production stages.
* Revision rules.
* Ownership.
* Usage rights.
* Completion conditions.

The exact custom-artwork MVP scope will be determined during Requirements based on the capabilities and limitations of the MVP payment model.

---

# 10. Physical Artwork

Physical artwork is not supported as a platform-managed marketplace transaction in the MVP.

Physical artworks may be displayed where permitted by the product rules.

Display and marketplace transaction are separate concepts.

If a customer and artist independently agree to sell a physical artwork:

* The transaction occurs outside the platform.
* Payment occurs outside the platform.
* Delivery is arranged outside the platform.
* The platform does not manage the physical delivery.
* The platform does not process the physical transaction.
* The platform does not apply the marketplace commission to that external physical sale.

A future version may introduce platform-managed support for selected physical artwork.

Physical forms that cannot be reasonably represented within the project's supported 2D-display model, such as sculpture, pottery, sewing, and carving, remain outside the project's final scope.

---

# 11. Social and Communication Scope

The approved MVP social functionality includes:

* Like.
* Follow.
* 1–5 star Rating.
* Customizable Notifications.
* Report.
* Block User.

The following are not part of the MVP:

* Dislike.
* Comments.
* User-to-user Chat.
* User-to-AI Chat.

These exclusions are intentional product-scope decisions rather than temporary implementation omissions.

---

# 12. Payment Model

## 12.1 MVP Payment Model

The MVP does not include platform-mediated payment processing.

The intended payment mechanism for applicable marketplace transactions is direct bank transfer from the customer to the artist.

Conceptually:

```text id="42wz98"
Customer
    │
    │ Direct Bank Transfer
    ▼
Artist
    │
    │ 15% Platform Commission
    ▼
Platform
```

The intended platform commission is **15% of applicable marketplace sales**.

The platform may apply restrictions when an artist has outstanding commission obligations.

Exact calculation, settlement, thresholds, and enforcement rules belong to Requirements.

---

## 12.2 Future Payment Model

A future product version may introduce platform-mediated payment.

Such functionality may require:

* Payment provider integration.
* Payment security.
* Financial reconciliation.
* Refund handling.
* Settlement rules.
* Additional legal and regulatory review.

These requirements are outside the MVP.

---

# 13. Dynamic Artwork Metadata

The MVP may use a dynamic question and metadata mechanism to improve artwork information and discovery.

The system may present optional questions based on:

* Artwork category.
* Previously selected options.
* Relevant artwork characteristics.

The artist reviews and controls the resulting information.

This mechanism is intended to operate through predefined system rules and does not require AI.

Detailed behavior and implementation belong to Requirements and later technical phases.

---

# 14. Administration and Moderation

The platform requires administrative and moderation capabilities.

High-level responsibilities include:

* User management.
* Artist application review.
* Artist approval.
* Artwork moderation.
* Report handling.
* Blocking-related administration.
* Marketplace administration.
* Commission administration.
* Security-related administration.
* Operational management.

Exact roles, permissions, and authorization rules belong to Requirements and System Design.

---

# 15. Project Lifecycle

The project follows the complete planned lifecycle:

```text id="k0g8d6"
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

Each phase has defined outputs and completion criteria.

The project may return to an earlier phase when newly discovered information requires changes to an approved artifact or decision.

---

# 16. Major Deliverables

The project is expected to produce documentation and implementation artifacts across the lifecycle.

## Foundation

* Project Charter.
* Project Scope.
* Project Objectives.
* Stakeholder Analysis.
* Assumptions.
* Constraints.
* Glossary.
* Foundation Gate.

## Requirements

* Requirements Specification.
* User Stories.
* Use Cases.
* Business Rules.
* Acceptance Criteria.
* Requirements Traceability.

## System Design

* System Architecture.
* System Context.
* Component Design.
* Authentication Design.
* Authorization Design.
* UML.
* Architecture Decisions.

## UI/UX

* User Flows.
* Information Architecture.
* Wireframes.
* High-Fidelity Designs.
* Prototypes.
* Design System.
* Accessibility specifications.
* Web and Mobile UX specifications.

## Database

* Database Requirements.
* ERD.
* Relational Schema.
* Normalization.
* Constraints.
* Index Strategy.
* Migrations.
* Seed Data.

## Backend

* REST API.
* API Documentation.
* OpenAPI Specification.
* Authentication.
* Authorization.
* Validation.
* Business Logic.
* Error Handling.
* API Testing.

## Web

* Responsive Web Application.
* Component Architecture.
* Routing.
* State Management.
* API Integration.
* Accessibility.

## Mobile

* Mobile Application.
* Mobile Architecture.
* Navigation.
* State Management.
* API Integration.
* Authentication.
* Mobile UX implementation.

## Quality and Security

* Test Strategy.
* Test Plan.
* Test Cases.
* Integration Tests.
* End-to-End Tests.
* Security Requirements.
* Threat Model.
* Security Review.
* Security Test Results.

## Deployment and Maintenance

* Infrastructure Configuration.
* Environment Configuration.
* Deployment Runbook.
* CI/CD.
* Backup Strategy.
* Monitoring.
* Recovery Procedures.
* Maintenance Documentation.

---

# 17. Project Success Criteria

The project should be considered successful when the following have been achieved:

1. The project foundation is coherent and documented.
2. MVP requirements are clearly defined and traceable.
3. The system architecture supports the approved requirements.
4. The database correctly represents the required domain.
5. The backend implements the required business operations.
6. The Web Application implements the approved MVP workflows.
7. The Mobile Application is implemented as a client of the established backend services.
8. Authentication and authorization are appropriately implemented.
9. Required quality assurance activities are completed.
10. Required cybersecurity activities are completed.
11. The system can be deployed using documented procedures.
12. Operational and maintenance documentation exists.
13. Important technical and product decisions are traceable.
14. Known limitations and future capabilities are documented.
15. The resulting project demonstrates a complete software engineering lifecycle.

---

# 18. Scope Control

The project will maintain controlled scope.

A proposed feature should be evaluated before being added.

Evaluation should consider:

* Product value.
* MVP necessity.
* Complete-project importance.
* Development effort.
* Technical complexity.
* Security implications.
* Testing implications.
* Maintenance cost.
* Legal considerations.
* Architectural impact.
* Schedule impact.

A feature may therefore be classified as:

```text id="m3l8p1"
MVP
  OR
Core Project
  OR
Future Product
  OR
Rejected
```

The classification should be documented where appropriate.

---

# 19. Key Risks

The project has several high-level risks.

| Risk                               | Initial Consideration |
| ---------------------------------- | --------------------- |
| Scope expansion                    | High                  |
| Complex marketplace workflows      | High                  |
| Payment and commission rules       | High                  |
| Custom artwork workflow complexity | High                  |
| Rights and policy ambiguity        | High                  |
| Marketplace moderation             | Medium/High           |
| Security and privacy               | High                  |
| Mobile scope and integration       | Medium                |
| Third-party service dependency     | Medium                |
| Production operational complexity  | Medium                |
| Future scalability                 | Medium                |

Detailed risk analysis belongs to the relevant project phases.

---

# 20. Key Dependencies

The project may depend on:

* Cloud hosting.
* Domain and DNS services.
* File/object storage.
* Email or notification services.
* External services required by approved requirements.
* Development and deployment infrastructure.

Platform payment providers are **future dependencies**, not MVP dependencies.

Specific providers should be selected only after requirements and technical constraints have been evaluated.

---

# 21. Technology Direction

The project currently has the following general technology direction:

* PostgreSQL for relational data.
* REST API architecture.
* Web client.
* Mobile client.
* Containerized development/deployment where appropriate.
* Git and GitHub for version control.
* Automated testing.
* CI/CD.

The final technology choices are documented through the appropriate technical phases and architecture decisions.

---

# 22. Documentation and Governance

Project-wide decisions are recorded in:

`decision-log.md`

The Decision Log is located at the repository root because project-wide decisions may affect multiple phases.

Architecture-specific decisions may additionally be documented in:

`02-system-design/architecture-decisions/`

Documentation should follow the project's Single Source of Truth principle.

Temporary phase status information should not be embedded in Phase 00 documents.

---

# 23. Definition of Complete Project

The complete project is not considered finished merely because the MVP Web Application runs.

The broader project completion target includes:

* Functional MVP.
* Mobile Application.
* Quality Assurance.
* Cybersecurity validation.
* Production deployment.
* Operational documentation.
* Backup and recovery procedures.
* Monitoring.
* Maintenance documentation.
* Known limitations.
* Technical debt documentation.
* Future development documentation.

The exact completion criteria for each phase are defined by its Gate and supporting documentation.

---

# 24. Approval

This Project Charter establishes the project-level foundation.

It defines the project's purpose, vision, scope model, major objectives, lifecycle, and high-level boundaries.

Detailed business requirements, technical architecture, database design, API contracts, UI/UX specifications, testing procedures, security controls, and implementation details are intentionally defined in their respective project phases.

Changes to project-wide scope or major decisions should be recorded in the root `decision-log.md`.
