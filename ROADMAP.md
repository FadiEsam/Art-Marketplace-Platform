# Art Marketplace Platform — Roadmap

## 1. Purpose

This roadmap defines the planned development path of the Art Marketplace Platform from its initial foundation through implementation, mobile development, quality assurance, cybersecurity, deployment, and maintenance.

It provides a high-level view of:

* Project phases.
* Major outputs.
* Phase dependencies.
* MVP boundaries.
* Complete project scope.
* Post-project and future product directions.
* Project progression.

The roadmap intentionally remains high-level.

Detailed requirements, business rules, architecture, database structures, API contracts, implementation details, and test cases belong to their respective documentation phases.

---

# 2. Scope Model

The project uses three related but distinct scope levels.

## 2.1 MVP

The MVP establishes the initial marketplace product.

Its primary client is the **Web Application**.

The MVP focuses on:

* Customer functionality.
* Artist functionality.
* Digital artwork.
* Marketplace workflows.
* Approved social functionality.
* Notifications.
* Moderation.
* MVP payment model.
* Backend/API.
* Database.
* Web frontend.

---

## 2.2 Complete Project

The complete project continues beyond the MVP.

It includes all planned engineering phases, including:

* Web Application.
* Mobile Application.
* Quality Assurance.
* Cybersecurity.
* Deployment.
* Maintenance.

The Mobile Application is therefore part of the complete project and learning path even though it is outside the MVP.

---

## 2.3 Future Product Development

Some capabilities are intentionally deferred beyond the current project scope or initial implementation.

Examples include:

* Platform-mediated payment.
* Printing integrations.
* Delivery integrations.
* AI functionality.
* Advanced marketplace capabilities.

These should not be confused with the Mobile Application.

> **Mobile is a core project phase. Future product features are capabilities deferred beyond the current project scope.**

---

# 3. Complete Project Lifecycle

```text
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

All listed phases are part of the project's planned engineering and learning lifecycle.

---

# 4. Phase Roadmap

## Phase 00 — Project Foundation

**Directory:** `00-project-foundation/`

### Purpose

Establish the stable conceptual foundation of the product.

### Main Areas

* Project Charter.
* Project Scope.
* Project Objectives.
* Stakeholders.
* Assumptions.
* Constraints.
* Glossary.
* Foundation Gate.

Project-wide decisions are maintained in the root `decision-log.md`.

### Outcome

A clear and internally consistent foundation for detailed requirements.

### Status

**In Progress**

---

# 5. Phase 01 — Requirements

**Directory:** `01-requirements/`

### Purpose

Define the detailed, testable behavior of the system.

### Main Areas

* Functional Requirements.
* Non-Functional Requirements.
* User Stories.
* Use Cases.
* Business Rules.
* Customer Workflows.
* Artist Workflows.
* Artwork Rules.
* Marketplace Rules.
* Order Rules.
* Custom Request Rules.
* Payment Rules.
* Commission Rules.
* Notification Rules.
* Social Rules.
* Moderation Rules.
* Rights and Policy Requirements.
* Acceptance Criteria.
* Requirements Traceability.

### Outcome

A sufficiently detailed definition of what the MVP must and must not do.

### Dependency

Phase 00 must provide a sufficiently stable foundation.

### Status

**Not Started**

---

# 6. Phase 02 — System Design

**Directory:** `02-system-design/`

### Purpose

Transform approved requirements into a coherent technical architecture.

### Main Areas

* System Architecture.
* System Context.
* Component Architecture.
* Authentication.
* Authorization.
* Business Logic Boundaries.
* External Service Boundaries.
* UML.
* Architecture Decisions.
* Deployment Architecture.

### Outcome

A technical design capable of guiding implementation.

### Dependency

Requirements must be sufficiently defined.

### Status

**Not Started**

---

# 7. Phase 03 — UI/UX Design

**Directory:** `03-ui-ux-design/`

### Purpose

Design the user experience and interfaces required by the project.

### Main Areas

* User Research.
* Personas.
* User Flows.
* Information Architecture.
* Wireframes.
* Visual Design.
* Prototypes.
* Design System.
* Accessibility.
* Responsive Design.
* Customer Experience.
* Artist Experience.
* Administrative Experience.
* Mobile Experience.

### Outcome

A coherent design system and set of user flows for the project's client applications.

### Dependency

Requirements and relevant system concepts must be sufficiently defined.

### Status

**Not Started**

---

# 8. Phase 04 — Database

**Directory:** `04-database/`

### Purpose

Design and implement the relational data model required by the project.

### Main Areas

* Database Requirements.
* ERD.
* Entity Relationships.
* Normalization.
* Constraints.
* Indexes.
* Security.
* Schema.
* Migrations.
* Seed Data.
* Performance Considerations.

### Current Direction

PostgreSQL.

### Outcome

A maintainable database capable of supporting the approved system requirements.

### Dependency

Requirements and system design.

### Status

**Not Started**

---

# 9. Phase 05 — API / Backend

**Directory:** `05-api-backend/`

**Source Code:** `apps/api/`

### Purpose

Implement the central backend and REST API.

### Main Areas

* API Architecture.
* REST API.
* Authentication.
* Authorization.
* Validation.
* Business Logic.
* Marketplace Logic.
* Artwork Management.
* Order Management.
* Custom Request Management.
* Payment and Commission Logic.
* Notifications.
* Moderation.
* Error Handling.
* Pagination.
* Filtering.
* API Versioning.
* External Services.
* OpenAPI.
* API Testing.

### Outcome

A secure backend capable of serving the Web Application and Mobile Application.

### Dependency

Requirements, system design, and database design.

### Status

**Not Started**

---

# 10. Phase 06 — Web Frontend

**Directory:** `06-web-frontend/`

**Source Code:** `apps/web/`

### Purpose

Implement the primary MVP client.

### Main Areas

* Frontend Architecture.
* Component Architecture.
* Routing.
* State Management.
* API Integration.
* Authentication.
* Customer Workflows.
* Artist Workflows.
* Artwork Discovery.
* Artwork Management.
* Marketplace Workflows.
* Notifications.
* Social Features.
* Administration.
* Accessibility.
* Responsive Design.

### MVP Position

The Web Application is the primary client of the initial MVP.

### Outcome

A functioning web application implementing the approved MVP workflows.

### Dependency

Backend APIs and UI/UX design.

### Status

**Not Started**

---

# 11. Phase 07 — Mobile Application

**Directory:** `07-mobile-app/`

**Source Code:** `apps/mobile/`

### Purpose

Develop the project's Mobile Application as a core part of the complete system and software-engineering learning path.

### MVP Position

The Mobile Application is **outside the MVP**.

This does not make it a future idea or optional project phase.

It is a planned and important stage of the complete project.

### Main Areas

* Mobile Architecture.
* Mobile UX.
* Navigation.
* Screen Structure.
* State Management.
* API Integration.
* Authentication.
* Customer Workflows.
* Artist Workflows.
* Notifications.
* Social Features.
* Mobile-specific capabilities.
* Testing.

### Architecture Principle

The Mobile Application should consume the established backend API and share the project's business rules.

It should not introduce an independent backend implementation of marketplace logic.

### Learning Role

This phase is an important part of the project's learning objectives, providing practical experience in:

* Mobile application architecture.
* API consumption.
* Authentication.
* State management.
* Client-server communication.
* Reusable backend services.
* Mobile UX.
* Cross-platform software engineering.

### Outcome

A functional mobile client integrated with the project's backend.

### Dependency

The backend API must provide sufficiently stable interfaces for mobile development.

### Status

**Not Started**

---

# 12. Phase 08 — Quality Assurance

**Directory:** `08-quality-assurance/`

**Test Source:** `tests/`

### Purpose

Verify that the complete implemented system satisfies its requirements.

### Main Areas

* Test Strategy.
* Test Plan.
* Test Cases.
* Unit Testing.
* Integration Testing.
* End-to-End Testing.
* System Testing.
* Regression Testing.
* Mobile Testing.
* Web Testing.
* API Testing.
* Test Data.
* Defect Management.
* Requirements Traceability.

### Outcome

Evidence that the implemented system satisfies the approved requirements and quality expectations.

### Dependency

Sufficiently functional implementation across the relevant clients and backend.

### Status

**Not Started**

---

# 13. Phase 09 — Cybersecurity

**Directory:** `09-cybersecurity/`

### Purpose

Assess and strengthen the security of the complete system.

### Main Areas

* Security Requirements.
* Threat Modeling.
* OWASP Review.
* Authentication Security.
* Authorization Security.
* API Security.
* Web Security.
* Mobile Security.
* File Security.
* Data Protection.
* Vulnerability Assessment.
* Security Testing.
* Remediation.

### Outcome

A documented security assessment with important findings addressed or appropriately handled.

### Dependency

A sufficiently functional system must exist for meaningful security assessment.

### Status

**Not Started**

---

# 14. Phase 10 — Deployment

**Directory:** `10-deployment/`

**Infrastructure:** `infrastructure/`

### Purpose

Deploy the project to an appropriate production environment.

### Main Areas

* Infrastructure.
* Server Configuration.
* Domain and DNS.
* HTTPS.
* Environment Configuration.
* Secrets Management.
* Database Deployment.
* File Storage.
* Backups.
* Monitoring.
* CI/CD.
* Deployment Runbook.
* Recovery Procedures.

### Outcome

A controlled and reproducible deployment process and operational environment.

### Dependency

Quality Assurance and Cybersecurity must reach the required readiness level.

### Status

**Not Started**

---

# 15. Phase 11 — Maintenance

**Directory:** `11-maintenance/`

### Purpose

Define and demonstrate long-term operation and evolution of the deployed project.

### Main Areas

* Monitoring.
* Backup and Restore.
* Incident Management.
* Dependency Updates.
* Security Maintenance.
* Performance.
* Technical Debt.
* Bug Fixes.
* Maintenance Releases.
* Future Development Planning.

### Outcome

A maintainable project with a documented approach to ongoing operation and evolution.

### Dependency

Deployment and operational infrastructure.

### Status

**Not Started**

---

# 16. MVP Roadmap

The MVP is primarily a web-based marketplace.

Its high-level progression is:

```text
Foundation
    ↓
Requirements
    ↓
System Design
    ↓
UI/UX
    ↓
Database
    ↓
Backend / API
    ↓
Web Frontend
    ↓
MVP Integration
    ↓
MVP Verification
```

The MVP does not require the Mobile Application.

However, the project continues after the MVP through Phase 07 and the remaining lifecycle phases.

---

# 17. MVP Functional Scope

The MVP includes:

### Users

* Registration.
* Authentication.
* Customer capabilities.
* Artist application.
* Artist approval.
* Profiles.

### Artwork

* Digital 2D-display artwork.
* Ready-made digital artwork.
* Supported custom digital artwork.
* Artwork categories.
* Dynamic optional metadata.
* Search and filtering.

### Social

* Like.
* Follow.
* 1–5 star Rating.
* Customizable Notifications.
* Report.
* Block.

### Marketplace

* Discovery.
* Purchase.
* Supported custom requests.
* Order/request management.
* Digital delivery/access.

### Payment

* Direct customer-to-artist bank transfer.
* Platform commission tracking.
* 15% applicable commission model.

Platform-mediated payment is outside the MVP.

### Administration

* Artist review.
* Content moderation.
* Reports.
* User management.
* Commission administration.

---

# 18. MVP Explicit Exclusions

The MVP excludes:

### Platform Payment

* Payment gateways.
* PSP integration.
* Platform-held funds.
* Automated payment settlement.

### Communication

* User-to-user chat.
* User-to-artist chat.
* User-to-AI chat.

### AI

All AI functionality.

### Social

* Dislike.
* Comments.
* Spam as a social interaction feature.

### Physical Marketplace

* Platform-managed physical-art transactions.
* Delivery integration.
* Printing integration.

### Mobile

The Mobile Application is outside the MVP.

**It is not outside the project.**

---

# 19. Complete Project After MVP

After the Web MVP has established the core marketplace, the project continues with the remaining planned phases.

A simplified view is:

```text
Web MVP
   ↓
Mobile Application
   ↓
Complete System QA
   ↓
Cybersecurity
   ↓
Deployment
   ↓
Maintenance
```

The exact sequencing may allow controlled overlap where dependencies permit.

---

# 20. Future Product Development

Future product capabilities may include:

* Platform-mediated payment.
* Expanded physical-art marketplace support.
* Printing-provider integration.
* Delivery-provider integration.
* AI-assisted capabilities.
* Advanced discovery.
* Recommendation systems.
* Advanced analytics.
* Additional marketplace functionality.

These are separate from the core Mobile Application phase.

---

# 21. AI Roadmap

AI is outside the MVP.

Potential future AI applications may include:

* Search assistance.
* Recommendation.
* Artist/customer matching.
* Moderation assistance.
* Workflow automation.
* Other AI-assisted marketplace functionality.

AI must not become a dependency for validating the core marketplace.

---

# 22. Physical Artwork Roadmap

## MVP

Physical artwork may be displayed under the applicable product rules, but physical marketplace transactions are not managed by the platform.

## Future

Potential future capabilities include:

* Platform-managed physical-art transactions.
* Printing services.
* Printing-provider integration.
* Delivery-provider integration.

These capabilities require separate requirements and technical design before implementation.

Non-2D physical forms outside the project's supported final scope remain excluded.

---

# 23. Technical Evolution

The project evolves through the following technical stages.

## Stage 1 — Core Backend

```text
Database
    +
REST API
    +
Business Logic
```

## Stage 2 — Web Client

```text
Backend
    +
Web Application
```

This establishes the MVP.

## Stage 3 — Mobile Client

```text
Backend
    +
Web Application
    +
Mobile Application
```

This is a core part of the complete project.

## Stage 4 — Quality and Security

```text
Web
 +
Mobile
 +
API
 +
Database
 ↓
QA
 +
Cybersecurity
```

## Stage 5 — Production

```text
Complete Application
       ↓
Infrastructure
       ↓
Deployment
       ↓
Monitoring
       ↓
Maintenance
```

## Stage 6 — Future Product Expansion

```text
Platform Payment
 +
Physical Marketplace
 +
Printing
 +
Delivery
 +
AI
 +
Advanced Features
```

---

# 24. Gate-Based Progression

Each major phase contains a Gate or equivalent completion criteria.

The general model is:

```text
Phase Work
    ↓
Documentation
    ↓
Implementation / Validation
    ↓
Gate
    ↓
PASS ─────────→ Next Phase
   │
   ├── Conditional Pass → Resolve Conditions
   │
   └── Fail → Corrective Work → Re-evaluation
```

A Gate is a quality checkpoint rather than a formality.

---

# 25. Dependency Principles

| Dependency                 | Principle                                                       |
| -------------------------- | --------------------------------------------------------------- |
| Foundation → Requirements  | Product boundaries must be sufficiently clear.                  |
| Requirements → Design      | Architecture responds to approved requirements.                 |
| Requirements → Database    | Data structures represent approved domain requirements.         |
| Design → Backend           | Backend follows the approved system architecture.               |
| Database → Backend         | Backend uses the approved data model.                           |
| UI/UX → Web                | Web implements approved user experience.                        |
| UI/UX → Mobile             | Mobile implements approved mobile experience.                   |
| Backend → Web              | Web consumes defined backend APIs.                              |
| Backend → Mobile           | Mobile consumes defined backend APIs.                           |
| Implementation → QA        | Testing requires functional implementation.                     |
| Implementation → Security  | Security assessment requires a sufficiently implemented system. |
| QA + Security → Deployment | Production deployment requires acceptable quality and security. |
| Deployment → Maintenance   | Maintenance depends on an operational deployment.               |

Controlled parallel work is allowed when it does not introduce unsupported assumptions or conflicting designs.

---

# 26. Scope Change Management

A proposed new feature should be evaluated before implementation.

Consider:

* Business value.
* MVP necessity.
* Project importance.
* Development effort.
* Technical complexity.
* Security impact.
* Testing impact.
* Maintenance cost.
* Legal impact.
* Architecture impact.
* Schedule impact.

Possible outcomes include:

```text
MVP
  OR
Core Project
  OR
Future Product
  OR
Rejected
```

A feature should not become part of the MVP merely because it is technically interesting or potentially useful.

Major scope changes should be reflected in the relevant project documentation and, where appropriate, the root decision log.

---

# 27. Documentation Principles

1. Root documentation describes project-wide information.
2. Phase documentation describes phase-specific information.
3. Project-wide decisions belong in the root `decision-log.md`.
4. The same business rule should not be independently redefined in multiple documents.
5. References may be used instead of duplicating canonical information.
6. Phase documents must not track temporary project status.
7. Root documentation tracks project progression.
8. Historical decisions remain traceable.
9. Superseded decisions should be marked rather than silently deleted.
10. Future capabilities must not silently become MVP requirements.
11. Documentation should support developers, contributors, clients, maintainers, and AI systems.

---

# 28. Roadmap Status

The current project status is maintained here and in other appropriate Root documentation.

| Phase                   | Status      |
| ----------------------- | ----------- |
| 00 — Project Foundation | In Progress |
| 01 — Requirements       | Not Started |
| 02 — System Design      | Not Started |
| 03 — UI/UX Design       | Not Started |
| 04 — Database           | Not Started |
| 05 — API / Backend      | Not Started |
| 06 — Web Frontend       | Not Started |
| 07 — Mobile Application | Not Started |
| 08 — Quality Assurance  | Not Started |
| 09 — Cybersecurity      | Not Started |
| 10 — Deployment         | Not Started |
| 11 — Maintenance        | Not Started |

The current active work is the Project Foundation re-baseline.

After the Foundation Gate is satisfied, the roadmap proceeds to Requirements.

---

# 29. Roadmap Maintenance

This file should be updated when there is a meaningful change to:

* Phase status.
* Project sequencing.
* MVP scope.
* Complete project scope.
* Major dependencies.
* Major future directions.

Detailed implementation tasks should remain in their appropriate phase documentation, issue tracking, or source-code documentation.

The roadmap should remain understandable at a high level and should not become a replacement for detailed engineering documentation.
