# Technology Stack

## 1. Purpose

This document defines the project's technology direction and foundational technical choices.

It establishes the technologies, platforms, architectural direction, and technical principles that guide the development of the Art Marketplace Platform.

This document is intentionally maintained at the foundation level.

It does not replace detailed system architecture, database design, API contracts, implementation specifications, deployment configuration, or technology-specific development documentation.

---

# 2. Technology Direction

The project follows a layered web and mobile application architecture supported by a centralized backend API and relational database.

The general direction is:

```text
Web Application
        │
        ├──────────────┐
        │              │
Mobile Application    │
        │              │
        └───────┬──────┘
                │
             Backend
             REST API
                │
        ┌───────┴────────┐
        │                │
    PostgreSQL       File Storage
        │
        └────────────────
```

The exact architecture and infrastructure configuration will be refined in the relevant later phases.

---

# 3. Technology Status

Technology choices in this document use the following categories:

| Status        | Meaning                                                                             |
| ------------- | ----------------------------------------------------------------------------------- |
| **Selected**  | Chosen as the current project technology.                                           |
| **Planned**   | Intended for a later project phase but may require implementation-level refinement. |
| **Preferred** | Preferred direction, subject to technical validation.                               |
| **TBD**       | Not yet sufficiently determined and must be evaluated later.                        |
| **Future**    | Relevant to future product scope rather than the MVP.                               |

A technology being listed in this document does not automatically mean that every related library, service, version, or implementation detail has been finalized.

---

# 4. Application Platforms

## 4.1 Web Application

**Status:** Selected

The project includes a web application as the primary MVP client.

The web application will provide the main user-facing marketplace experience for the MVP.

The web application is expected to support areas such as:

* Authentication.
* Customer functionality.
* Artist functionality.
* Artwork discovery.
* Artwork viewing.
* Artwork publishing.
* Artist profiles and portfolios.
* Marketplace interactions.
* Orders or requests where applicable.
* Notifications.
* Administrative interfaces where required.

Detailed functionality is defined in the Requirements and later system-design phases.

---

## 4.2 Mobile Application

**Status:** Planned

The project includes a mobile application as part of the Complete Project.

The mobile application is outside the MVP implementation scope.

It is therefore represented as:

```text
MVP
    → Web Application

Complete Project
    → Web Application
    → Mobile Application
```

The mobile application is not considered merely an optional future product feature.

The mobile technology and implementation details may be refined during the mobile-development phase.

---

# 5. Frontend Technologies

## 5.1 Web Frontend

**Status:** Preferred / Planned

The preferred web frontend direction is:

* React.
* TypeScript.

The frontend will communicate with the backend primarily through the project's REST API.

The frontend is responsible for:

* User interface rendering.
* Client-side interaction.
* Form handling.
* Client-side validation where appropriate.
* API communication.
* Authentication state handling.
* User feedback and interface states.
* Responsive web experience.

Business rules and security-sensitive authorization must not rely solely on frontend implementation.

---

## 5.2 React

**Status:** Preferred

React is the preferred frontend framework/library direction for the web application.

The final project structure, rendering strategy, routing approach, state management approach, and supporting libraries will be established during the relevant system-design and implementation phases.

---

## 5.3 TypeScript

**Status:** Preferred

TypeScript is the preferred language for the web frontend.

Its use is intended to improve:

* Type safety.
* Maintainability.
* API contract consistency.
* Refactoring safety.
* Developer experience.

The exact TypeScript configuration will be defined during implementation.

---

# 6. Mobile Technologies

## 6.1 Mobile Framework

**Status:** Preferred / Planned

Flutter and Dart are the preferred direction for the mobile application based on the project's planned mobile-development path.

The mobile application will consume the same centralized backend/API layer used by the web application where appropriate.

The final mobile architecture, state management, local storage, authentication handling, and platform-specific integrations will be defined during the mobile-development phase.

---

# 7. Backend

## 7.1 Backend Architecture

**Status:** Selected

The project uses a centralized backend responsible for:

* Business logic.
* Authentication.
* Authorization.
* Data validation.
* Marketplace rules.
* Artist approval workflows.
* Artwork management.
* Orders and requests.
* Payment-related records.
* Commission tracking.
* Notifications.
* Moderation.
* API access control.

The backend is the authoritative enforcement layer for security-sensitive and business-critical rules.

---

## 7.2 Backend Language and Framework

**Status:** Preferred / Planned

PHP is the current backend language direction.

Laravel is the preferred backend framework direction.

The final Laravel architecture, package selection, folder structure, and implementation conventions will be established during the backend-development phase.

---

# 8. API

## 8.1 API Style

**Status:** Selected

The project uses a REST API as the primary communication interface between client applications and the backend.

The API is intended to serve:

* Web clients.
* Mobile clients.
* Authorized administrative interfaces.
* Other approved internal or external integrations where required.

Detailed endpoint definitions, request/response schemas, authentication mechanisms, validation rules, error formats, and versioning strategy belong in the API and backend documentation.

---

## 8.2 API Responsibilities

The API layer is responsible for providing controlled access to backend capabilities.

Typical responsibilities include:

* Authentication.
* Authorization.
* Resource access.
* Data validation.
* Business operation requests.
* Artwork management.
* Marketplace interactions.
* Order/request operations.
* Notifications.
* Administrative operations.

The API must not expose internal implementation details unnecessarily.

---

# 9. Database

## 9.1 Database Management System

**Status:** Selected

PostgreSQL is the project's relational database management system.

PostgreSQL will be used for structured application data such as:

* Users.
* Roles and permissions.
* Artist applications.
* Artwork records.
* Artwork metadata.
* Categories.
* Listings.
* Orders and requests.
* Payment records.
* Commission obligations.
* Social interactions.
* Notifications.
* Reports and moderation records.
* Audit-related records where required.

The final schema will be defined in the Database phase.

---

## 9.2 Database Design Direction

The database should prioritize:

* Data integrity.
* Referential integrity.
* Appropriate normalization.
* Clear relationships.
* Appropriate indexing.
* Secure access patterns.
* Maintainability.
* Traceability of important state changes.

The technology-stack document does not define the final database schema.

---

# 10. File and Artwork Storage

## 10.1 Artwork Files

**Status:** Planned

Artwork files are expected to require storage separate from ordinary relational database records.

The database should store appropriate metadata and references to stored files rather than unnecessarily storing large artwork binaries directly in ordinary relational tables.

The exact storage technology and provider remain subject to infrastructure and deployment decisions.

---

## 10.2 Storage Requirements

The storage solution must support the project's requirements for:

* Artwork uploads.
* Artwork retrieval.
* Access control.
* File organization.
* File validation.
* Appropriate size limitations.
* Secure file handling.
* Backup and recovery considerations.
* Future scalability.

Specific storage-provider selection will be documented separately when finalized.

---

# 11. Authentication and Authorization

## 11.1 Authentication

**Status:** Planned

The backend will provide centralized authentication for supported clients.

Authentication design must support the project's user-account model and future web/mobile clients.

The exact authentication mechanism and token/session strategy will be finalized during system design and backend development.

---

## 11.2 Authorization

**Status:** Selected

Authorization must be enforced by the backend.

The system will distinguish permissions and capabilities based on the user's role and relevant resource ownership.

The project includes role concepts such as:

* Customer.
* Artist.
* Artist Reviewer.
* Administrator.

A user may have Artist capabilities while continuing to act as a Customer.

Detailed role and permission matrices belong in the Requirements and backend phases.

---

# 12. Payment-Related Technology

## 12.1 MVP Payment Model

**Status:** Selected

The MVP does not use platform-mediated payment processing.

The MVP payment model supports direct bank transfer between the Customer and Artist where applicable.

Therefore, the MVP does not require a payment gateway or payment service provider to collect and process customer payments through the platform.

---

## 12.2 Commission Tracking

**Status:** Selected

The platform tracks the Artist's 15% commission obligation.

The backend and database must be capable of recording the information necessary to:

* Identify applicable transactions.
* Calculate or record the applicable commission.
* Track outstanding obligations.
* Track settlement status.
* Support commission-related business rules.

Detailed commission calculations, enforcement thresholds, and related workflows belong in the Requirements and backend phases.

---

## 12.3 Platform-Mediated Payments

**Status:** Future

Platform-mediated payment processing may be introduced in a future version.

This may require:

* Payment provider integration.
* Payment processing.
* Payment status synchronization.
* Refund handling.
* Transaction security.
* Additional compliance requirements.

No specific future payment provider is selected by this document.

---

# 13. External Services and Integrations

External services may be introduced when they provide functionality that should not be implemented directly by the platform.

Potential integration categories include:

* Payment providers.
* Email services.
* Notification services.
* File/object storage.
* Printing providers.
* Delivery providers.
* Other infrastructure services.

The existence of an integration category does not mean that the integration is part of the MVP.

Each external dependency should be evaluated according to:

* Business necessity.
* Security.
* Cost.
* Reliability.
* Privacy.
* Availability.
* Technical compatibility.
* Project scope.

---

# 14. Printing and Delivery Technology

## 14.1 Printing

**Status:** Future

Printing-provider integration is outside the MVP.

A future implementation may integrate external printing services where appropriate.

The current technology foundation does not select a printing provider.

---

## 14.2 Delivery

**Status:** Future

Delivery-provider integration is outside the MVP.

A future implementation may integrate external delivery services if physical artwork transactions become supported.

The current technology foundation does not select a delivery provider.

---

# 15. Notifications

**Status:** Planned

The platform will support customizable notifications as part of the MVP product scope.

Notification delivery may use application-level notification mechanisms and appropriate external services where required.

The exact notification channels and provider integrations will be defined during Requirements and system design.

Potential channels may include:

* In-app notifications.
* Email.
* Push notifications for the mobile application.

A specific external notification provider is not selected by this document.

---

# 16. Search and Discovery

**Status:** Planned

The platform requires artwork discovery capabilities.

The initial implementation may use database-supported search, filtering, categorization, and metadata-based discovery.

Dynamic artwork metadata may improve discovery without requiring AI.

AI-based search or recommendation systems are outside the MVP.

The exact search implementation will be defined during system design and backend development.

---

# 17. Security Technology Direction

Security is treated as a cross-cutting concern across all application layers.

The technology direction must support:

* Secure authentication.
* Backend authorization.
* Input validation.
* Secure file handling.
* Protection against common web vulnerabilities.
* Secure API communication.
* Secret management.
* Appropriate password handling.
* Auditability where required.
* Protection of sensitive user and transaction data.

Security implementation details belong to the Security phase and relevant technical phases.

---

# 18. Development Tools

The project may use the following development tools and technologies.

### Version Control

**Status:** Selected

Git is used for source-code version control.

GitHub is used as the project's repository and collaboration platform.

### API Development and Testing

**Status:** Planned

API development and testing may use tools such as:

* Postman.
* API documentation tools.
* Automated API testing frameworks.

The final toolset may evolve during implementation.

### Containerization

**Status:** Planned

Docker is planned as part of the project's development and deployment tooling.

Its exact role, service definitions, and production usage will be defined during the DevOps and deployment phases.

---

# 19. Testing Technologies

Testing is a core project area.

The project is expected to use multiple testing levels, including where appropriate:

* Unit testing.
* Integration testing.
* API testing.
* Feature testing.
* End-to-end testing.
* Security testing.
* Usability testing.
* Mobile testing.

The exact testing frameworks and tools will be selected during the Testing and QA phase.

Testing technologies are not required to be completely finalized at the Foundation level.

---

# 20. Deployment and Infrastructure

## 20.1 Deployment Direction

**Status:** Planned

The complete project will include deployment of the web application, backend, database, and required supporting services.

The deployment architecture will be defined later based on:

* Application requirements.
* Security requirements.
* Expected workload.
* Cost.
* Availability.
* Scalability.
* Operational complexity.

---

## 20.2 Environments

The project should distinguish between environments such as:

```text id="o8p3gd"
Development
    ↓
Testing / Staging
    ↓
Production
```

The exact environment structure will be defined during the deployment phase.

Production credentials and secrets must not be committed to the source repository.

---

# 21. Architecture Principles

The technology direction follows these principles:

### Separation of Concerns

Web, mobile, backend, database, storage, and external services should have clearly defined responsibilities.

### Backend Authority

Business-critical rules and authorization must be enforced by the backend.

### API-Centered Integration

Web and mobile clients should communicate with backend capabilities through controlled APIs.

### Maintainability

Technology choices should support readable, testable, and maintainable code.

### Security by Design

Security requirements should influence architecture and implementation from the beginning rather than being treated solely as a final testing activity.

### Extensibility

The architecture should allow future capabilities without unnecessarily implementing them in the MVP.

### Appropriate Simplicity

The project should avoid unnecessary infrastructure complexity when a simpler solution satisfies the requirements.

---

# 22. Technology Boundaries

Technology choices must not independently expand the product scope.

For example:

* Adding a mobile framework does not make mobile an MVP requirement.
* Adding a payment library does not make platform-mediated payment part of MVP.
* Adding an AI library does not make AI functionality part of MVP.
* Adding a storage provider does not make physical delivery part of MVP.
* Adding an external service does not automatically make its associated future capability an MVP feature.

Product scope is defined by the project foundation and requirements, not by the availability of a technology.

---

# 23. Technology Decisions That Remain Open

The following areas may require later technical decisions:

* Exact React project architecture.
* Exact Laravel architecture and package selection.
* API authentication mechanism.
* State-management approach.
* Exact mobile architecture.
* Exact file/object storage provider.
* Exact notification providers.
* Search implementation details.
* Deployment provider.
* Infrastructure architecture.
* CI/CD tooling.
* Monitoring and observability tooling.
* Production payment provider for future platform-mediated payments.

Open technical decisions must be documented when they become sufficiently important to affect architecture, scope, or implementation.

---

# 24. Relationship to Other Documentation

This document defines technology direction at the Foundation level.

Detailed information belongs to the appropriate later documentation.

| Topic                             | Primary Documentation Area     |
| --------------------------------- | ------------------------------ |
| Project-wide technology direction | `00-project-foundation/technol |
