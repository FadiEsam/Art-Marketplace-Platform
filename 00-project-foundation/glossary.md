# Project Glossary

## 1. Purpose

This glossary defines the key terms used throughout the Art Marketplace Platform project.

The purpose of this document is to establish consistent terminology across:

* Business requirements
* Functional and non-functional requirements
* System design
* Database design
* API design
* UI/UX design
* Testing
* Security
* Deployment
* Project documentation

Definitions in this document describe the intended meaning of terms **within this project**. Where a concept has not yet been finalized, the definition intentionally avoids establishing a final business rule.

---

# 2. Business and Product Terms

## 2.1 Art Marketplace Platform

The software platform being developed to connect customers with artists and allow customers to discover, purchase, or commission artwork through structured marketplace workflows.

The platform is initially focused on a web-based MVP, with mobile applications considered as a future extension.

---

## 2.2 Marketplace

A platform that facilitates interactions and transactions between multiple independent parties, primarily customers and artists.

In this project, the platform facilitates the discovery of artwork and services, requests, orders, payments, delivery, approval, and related communication or notifications.

---

## 2.3 MVP — Minimum Viable Product

The smallest complete version of the platform that provides the core marketplace value and allows the primary business workflow to be validated.

The MVP is intentionally controlled and does not include advanced features that are not necessary to validate the core product.

---

## 2.4 Artwork

A creative work created or offered by an artist through the platform.

Artwork may represent a finished work available for purchase or another type of creative product supported by the platform.

The exact supported artwork categories and formats are subject to the requirements phase.

---

## 2.5 Service

An offering published by an artist describing a type of creative work that the artist is willing to provide to customers.

A service may contain information such as:

* Title
* Description
* Price
* Expected delivery time
* Included deliverables
* Revision conditions
* Additional requirements

The final service model will be defined during requirements analysis.

---

## 2.6 Commission

A customer-specific creative work requested from an artist according to requirements agreed between the parties.

A commission differs from a predefined artwork because the final work is created according to customer requirements rather than being an already completed item.

---

## 2.7 Listing

A published marketplace item that can be discovered by users.

Depending on the final product model, a listing may represent an artwork, service, or another marketplace offering.

---

## 2.8 Portfolio

A collection of an artist's selected works used to present their skills, style, and previous work to potential customers.

A portfolio is primarily intended for discovery and evaluation and does not necessarily represent items currently available for purchase.

---

## 2.9 Discovery

The process through which customers find artists, artworks, services, or other marketplace offerings.

Discovery may include:

* Browsing
* Search
* Filtering
* Artist profiles
* Artwork pages
* Service pages
* Categories or other classification mechanisms

---

# 3. User and Stakeholder Terms

## 3.1 Customer

A platform user who discovers artwork or services and may purchase artwork or request creative work from an artist.

A customer may create and manage orders and interact with the platform according to the permissions assigned to the customer role.

---

## 3.2 Artist

A platform user who presents artwork, maintains a portfolio, publishes services, receives customer requests, and manages relevant orders.

An artist is responsible for producing and delivering the agreed creative work.

---

## 3.3 Administrator

A privileged platform user responsible for managing platform-level operations.

Administrative capabilities may include:

* User management
* Content moderation
* Order oversight
* Platform configuration
* Security-related administration
* Review of operational records

The exact administrator permissions will be defined during authorization design.

---

## 3.4 Platform Owner / Business Owner

The person or organization responsible for the business direction, ownership, and commercial decisions of the platform.

The Platform Owner is a business stakeholder rather than necessarily a technical system role.

---

## 3.5 Stakeholder

Any person, organization, or external system that has an interest in, interacts with, influences, or is affected by the project or platform.

Examples include:

* Customers
* Artists
* Administrators
* Platform Owner
* Development Team
* Payment Provider
* Hosting Provider
* Regulatory or legal stakeholders

---

# 4. Marketplace Transaction Terms

## 4.1 Request

A customer's initiation of a request for an artist's service or custom creative work before it becomes a confirmed order.

A request may require additional information, clarification, pricing, or agreement before an order is created.

The exact request-to-order workflow is subject to final requirements.

---

## 4.2 Order

A structured transaction record representing an agreed piece of work or marketplace purchase between a customer and an artist.

An order may contain:

* Customer
* Artist
* Service or artwork
* Requirements
* Deliverables
* Price
* Deadline
* Revision terms
* Payment information
* Delivery information
* Approval status
* Order status

---

## 4.3 Order Lifecycle

The sequence of states through which an order progresses from initiation to completion.

The conceptual lifecycle is:

**Request/Purchase → Order → Payment → Production/Delivery → Review → Revision or Approval → Completion**

The final state names, transitions, and allowed actions will be defined during requirements and system design.

---

## 4.4 Requirement

A specific description of what the artist is expected to produce or provide as part of an order.

Examples may include:

* Required dimensions
* Style
* Content
* Format
* References
* Deliverables
* Deadline
* Special conditions

Order requirements should be sufficiently clear to support production, delivery, review, and acceptance.

---

## 4.5 Deliverable

A specific output that the artist is required to provide as part of an order.

A deliverable may be a file, artwork, design, document, or another agreed output.

---

## 4.6 Deadline

The agreed date or time by which an order or deliverable is expected to be completed.

Deadline rules, extensions, and consequences of delays are subject to the final business requirements.

---

## 4.7 Delivery

The act of making the completed work or deliverables available to the customer through the platform or another approved mechanism.

Delivery does not necessarily mean that the order is completed.

---

## 4.8 Customer Approval

The customer's explicit acceptance of the delivered work according to the agreed requirements and contract/order conditions.

Customer approval is an important condition for completion of applicable orders.

---

## 4.9 Completion

The final state of an order after the applicable delivery, review, revision, and approval conditions have been satisfied.

Completion rules will be formally defined in the requirements and business rules.

---

## 4.10 Revision

A modification to delivered work requested by the customer within the revision conditions agreed for the order.

A revision is not automatically considered a new order.

---

## 4.11 Included Revision

A revision that is covered by the original order according to its agreed revision terms.

---

## 4.12 Additional Revision

A revision requested beyond the number or conditions included in the original order.

Whether an additional revision creates an additional charge or requires another agreement is a business rule to be defined later.

---

## 4.13 Cancellation

The termination of an order before its normal completion.

Cancellation rules, eligibility, responsibility, timing, and financial consequences are **TBD** during the requirements phase.

---

## 4.14 Refund

The return of some or all of a customer's payment according to applicable business rules and payment-provider capabilities.

The MVP refund policy is **TBD**.

---

## 4.15 Dispute

A disagreement between parties regarding an order, payment, delivery, requirements, revisions, approval, or another marketplace matter.

A complete dispute-resolution system is outside the controlled MVP scope unless requirements later establish a minimal necessary workflow.

---

# 5. Payment Terms

## 5.1 Payment

A financial transaction initiated by a customer to pay for an order.

Payments are expected to be processed through a third-party payment service provider.

---

## 5.2 Payment Service Provider (PSP)

An external service that processes payments on behalf of the platform.

The final payment provider is **TBD**.

The platform must not implement its own proprietary payment-processing infrastructure.

---

## 5.3 Payment Status

The state describing the financial status of a payment.

Examples may include:

* Pending
* Authorized
* Paid
* Failed
* Refunded
* Cancelled

The final set of statuses depends on the selected payment provider and business requirements.

---

## 5.4 Order Status

The state describing the operational/business progress of an order.

Order status and payment status are separate concepts.

For example, an order may be in production while its payment record has a separate financial status.

---

## 5.5 Platform Fee / Commission

A fee retained by the platform from a marketplace transaction, if such a business model is adopted.

The platform's commission model is currently **TBD**.

---

## 5.6 Payment Processing Fee

A fee charged by the payment provider for processing a transaction.

This fee is different from any platform commission.

---

## 5.7 Fund Holding / Escrow-like Model

A payment arrangement in which customer funds are retained or controlled until specific conditions are satisfied.

The platform may require an escrow-like business concept, such as linking release of funds to delivery and customer approval.

However, this does **not** imply that the platform will legally operate an escrow service.

The feasibility, legal status, regulatory requirements, and payment-provider capabilities must be validated before implementation.

---

# 6. Authentication and Authorization

## 6.1 Authentication

The process of verifying the identity of a user.

Example:

> Confirming that a person attempting to access an account is the legitimate account holder.

---

## 6.2 Authorization

The process of determining what an authenticated user is allowed to access or perform.

Authentication answers:

> Who are you?

Authorization answers:

> What are you allowed to do?

---

## 6.3 Role

A defined category of permissions assigned to a user.

Primary roles in the platform are:

* Customer
* Artist
* Administrator

---

## 6.4 RBAC — Role-Based Access Control

An authorization model in which permissions are associated with roles rather than being independently assigned to every user.

For example:

```text
Customer → Customer permissions

Artist → Artist permissions

Administrator → Administrative permissions
```

---

## 6.5 Resource

A system entity or object that can be accessed or manipulated.

Examples include:

* User
* Artist profile
* Artwork
* Service
* Order
* Payment
* Review
* File

---

## 6.6 Resource Ownership

The relationship determining which user or entity owns or controls a particular resource.

Ownership checks are required when access to private resources is restricted.

---

## 6.7 Audit Log

A record of important system or administrative actions.

An audit log may contain:

* Actor
* Action
* Target resource
* Timestamp
* Relevant metadata

Auditability requirements will determine which actions must be recorded.

---

# 7. Technical Terms

## 7.1 API — Application Programming Interface

A defined interface through which software components communicate with each other.

The platform backend will expose APIs that can be consumed by the web application and, in the future, a mobile application.

---

## 7.2 REST API

An API designed around resources and HTTP operations following REST architectural principles.

REST is the current API direction for the project.

---

## 7.3 Endpoint

A specific API URL and HTTP operation used to access or manipulate a resource or perform an operation.

Example:

```text
GET /api/v1/artworks
```

---

## 7.4 Backend

The server-side part of the platform responsible for business logic, data access, authentication, authorization, API processing, and integration with external services.

---

## 7.5 Frontend

The client-side application through which users interact with the platform.

The initial frontend is a web application.

---

## 7.6 Client

An application that consumes the backend API.

Examples include:

* Web application
* Future mobile application
* Potential future integrations

---

## 7.7 Business Logic

Rules and processes that define how the platform operates.

Examples include:

* Who can create an order
* Which order transitions are allowed
* Which users can access an order
* When a revision is allowed
* When an order can be completed

Business logic must not depend exclusively on frontend enforcement.

---

## 7.8 Relational Database

A database that stores structured information using tables and relationships between them.

A relational database is the current database direction for the project.

---

## 7.9 PostgreSQL

The current preferred relational database technology for the project.

The final technology decision will be documented through the appropriate architecture decision process.

---

## 7.10 Schema

The logical structure defining database objects such as:

* Tables
* Columns
* Relationships
* Constraints
* Indexes

---

## 7.11 Migration

A version-controlled change to the database structure.

Migrations allow database schema changes to be applied consistently across environments.

---

## 7.12 Seed Data

Initial or controlled sample data inserted into a database for development, testing, or demonstration purposes.

Seed data must not contain real sensitive production information.

---

## 7.13 Object Storage

External storage designed for files and large binary objects.

Artwork files and other large media are expected to use object/file storage rather than being tightly coupled to relational database storage.

The final provider is **TBD**.

---

## 7.14 Environment

A distinct technical setup in which the application operates.

The project considers at least:

* Development
* Testing
* Production

---

## 7.15 Development Environment

The environment used by developers to implement and locally test the system.

---

## 7.16 Testing Environment

An environment used to verify application behavior before production deployment.

---

## 7.17 Production Environment

The live environment used by real users.

Production requires stronger security, monitoring, backup, access control, and operational procedures than development environments.

---

# 8. Software Engineering Terms

## 8.1 SDLC — Software Development Life Cycle

The structured process used to develop and maintain the system.

For this project, the major phases include:

1. Project Foundation
2. Requirements
3. System Design
4. UI/UX Design
5. Database
6. API/Backend
7. Web Frontend
8. Quality Assurance
9. Cybersecurity
10. Deployment
11. Maintenance

---

## 8.2 Functional Requirement

A requirement describing what the system must do.

Example:

> The system shall allow an artist to publish a service.

---

## 8.3 Non-Functional Requirement

A requirement describing a quality, constraint, or characteristic of the system rather than a specific business function.

Examples include:

* Security
* Performance
* Availability
* Accessibility
* Maintainability

---

## 8.4 Business Rule

A rule defining how the business or marketplace operates.

Example:

> A customer may request a revision only when the order is within its allowed revision conditions.

Business rules should be enforceable by the backend where applicable.

---

## 8.5 User Story

A short description of a desired capability from a user's perspective.

Typical structure:

> As a [user], I want [capability], so that [benefit].

---

## 8.6 Use Case

A structured description of an interaction between an actor and the system to achieve a specific goal.

---

## 8.7 Acceptance Criterion

A condition that must be satisfied for a requirement or user story to be considered successfully implemented.

---

## 8.8 Traceability

The ability to trace a requirement through the development lifecycle.

A typical relationship is:

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

---

## 8.9 Gate

A formal checkpoint at the end of a project phase.

A phase should not be considered complete merely because its files exist. The phase must satisfy its defined Gate criteria before the project progresses.

---

## 8.10 Scope Change

A modification that adds, removes, or significantly changes an agreed project requirement, feature, constraint, or deliverable.

Scope changes should be evaluated before implementation to prevent uncontrolled MVP growth.

---

# 9. Architecture and Design Terms

## 9.1 System Architecture

The high-level structure of the system, including major components, their responsibilities, communication mechanisms, and external dependencies.

---

## 9.2 Component

A distinct software or infrastructure unit with a defined responsibility.

Examples may include:

* Web frontend
* Backend API
* Database
* Object storage
* Payment integration

---

## 9.3 Architecture Decision

A documented technical decision that has a meaningful impact on system structure or future development.

---

## 9.4 ADR — Architecture Decision Record

A document used to record an important architectural decision, including:

* Context
* Decision
* Alternatives
* Consequences

---

## 9.5 UML — Unified Modeling Language

A standardized modeling language used to represent and communicate aspects of software systems.

This project may use UML diagrams including:

* Use Case
* Class
* Sequence
* Activity
* State
* Component
* Deployment

---

# 10. Security Terms

## 10.1 HTTPS

HTTP communication protected using TLS encryption.

HTTPS is mandatory for production environments.

---

## 10.2 Secret

Sensitive information used to authenticate or authorize access to systems or services.

Examples include:

* API keys
* Passwords
* Tokens
* Database credentials
* Encryption keys

Secrets must not be committed to source control.

---

## 10.3 Personal Data

Information that can identify or relate to an individual.

Examples may include:

* Name
* Email address
* Phone number
* Account information

The exact personal-data classification and applicable legal requirements depend on the deployment context.

---

## 10.4 Threat

A potential cause of harm to the confidentiality, integrity, or availability of the system or its data.

---

## 10.5 Vulnerability

A weakness that could potentially be exploited to compromise the system.

---

## 10.6 Risk

The potential impact resulting from a threat exploiting a vulnerability.

Risk assessment may consider factors such as:

* Likelihood
* Impact
* Exposure
* Existing controls

---

## 10.7 Threat Model

A structured analysis of potential threats, attack surfaces, assets, and security controls.

---

# 11. Testing and Quality Terms

## 11.1 Test Case

A defined set of conditions, inputs, actions, and expected results used to verify a specific system behavior.

---

## 11.2 Integration Test

A test verifying that multiple components work correctly together.

---

## 11.3 End-to-End Test

A test that validates a complete user or system workflow from beginning to end.

---

## 11.4 System Test

A test performed against the complete system to verify that the integrated product satisfies its requirements.

---

## 11.5 Regression Testing

Testing performed after changes to verify that previously working functionality has not been unintentionally broken.

---

## 11.6 Bug

A defect or unexpected behavior in the software.

---

## 11.7 Quality Assurance

The systematic activities used to ensure that the system meets defined requirements and quality expectations.

---

# 12. Deployment and Operations Terms

## 12.1 Deployment

The process of making a software version available in a target environment.

---

## 12.2 Docker

A containerization technology that can be used to package applications and their dependencies into reproducible environments.

Docker is part of the project's technical learning and deployment direction but does not imply that every component must necessarily be containerized.

---

## 12.3 CI/CD

Continuous Integration and Continuous Delivery/Deployment practices used to automate activities such as:

* Building
* Testing
* Validation
* Packaging
* Deployment

---

## 12.4 Monitoring

The continuous observation of system health, availability, performance, errors, and relevant operational metrics.

---

## 12.5 Backup

A copy of data or system configuration maintained so that information can be restored after loss, corruption, or failure.

---

## 12.6 Restore

The process of recovering data, configuration, or system functionality from a backup or other recovery source.

---

## 12.7 Deployment Runbook

A documented sequence of steps required to deploy, verify, troubleshoot, or roll back the system.

---

# 13. Documentation Terms

## 13.1 Project Charter

A document establishing the project's purpose, high-level scope, objectives, stakeholders, and overall direction.

---

## 13.2 Project Scope

The defined boundaries of what the project includes and excludes.

---

## 13.3 Assumption

A condition believed to be true for planning purposes but not yet fully validated.

---

## 13.4 Constraint

A limitation that restricts project decisions, implementation, resources, technology, schedule, or scope.

---

## 13.5 Decision Log

A record of important project decisions and the reasoning behind them.

---

## 13.6 Change Log

A chronological record of significant changes made to the project, documentation, or software.

---

## 13.7 Roadmap

A high-level representation of planned future work, features, improvements, or project phases.

A roadmap is not necessarily a commitment to implement every listed item.

---

# 14. External Service Terms

## 14.1 Third-Party Service

An external system operated by another organization that the platform depends on for a particular capability.

Examples include:

* Payment processing
* Email delivery
* Notifications
* File/object storage
* Hosting

---

## 14.2 Integration

The technical connection between the platform and an external system or internal component.

---

## 14.3 Provider

An external organization or service responsible for supplying a technical capability.

Examples:

* Payment provider
* Hosting provider
* Storage provider
* Notification provider

The specific providers used by the final system may be selected later.

---

# 15. Intellectual Property Terms

## 15.1 Intellectual Property (IP)

Legal rights associated with creative works, designs, trademarks, software, and other intellectual creations.

The platform may involve intellectual-property considerations because artists upload and sell or license creative works.

---

## 15.2 Ownership Rights

The rights determining who legally owns a creative work or other intellectual property.

Ownership rules for artwork created or sold through the platform are business/legal matters and must not be assumed solely from the technical implementation.

---

## 15.3 License

A permission defining how a customer may use an artwork or other creative work.

Licensing terms are subject to business and legal requirements.

---

# 16. Status and State Terms

## 16.1 State

A defined condition of a system entity at a particular point in time.

Examples:

```text
Order → In Production

Payment → Paid

Artwork → Published
```

---

## 16.2 State Transition

A valid change from one state to another.

Example:

```text
In Production → Delivered
```

State transitions should be explicitly defined so that invalid transitions can be prevented.

---

## 16.3 Status History

A record of changes to the status of an entity over time.

Status history may be required for important entities such as orders and payments.

---

# 17. Project-Specific Terminology Principles

The following principles apply throughout the project:

1. **Order Status and Payment Status must remain separate concepts.**
2. **Authentication and Authorization must not be treated as the same mechanism.**
3. **A Request is not automatically an Order.**
4. **Delivery is not automatically Completion.**
5. **Customer Approval is distinct from Delivery.**
6. **A Revision is governed by the order's revision conditions.**
7. **Additional Revision does not automatically imply a specific price or workflow until defined by business rules.**
8. **Platform Commission and Payment Processing Fees are separate concepts.**
9. **Fund holding must not be described as legal escrow unless the legal and payment model explicitly supports that terminology.**
10. **Technology choices marked as TBD are not considered final architectural decisions.**
11. **Future features such as advanced AI, recommendation systems, and social-network capabilities must not be treated as MVP requirements unless formally added through scope change.**
12. **The frontend must not be considered the authoritative enforcement point for security or business rules.**
13. **Business-critical rules must be enforceable by the backend.**
14. **Terms in this glossary should be used consistently across requirements, design, implementation, and testing documentation.**

---

# 18. Terms Marked as TBD

The following concepts remain intentionally undecided at this stage:

* Final payment provider
* Payment split model
* Fund-holding mechanism
* Platform commission model
* Refund policy
* Cancellation policy
* Dispute-resolution workflow
* Geographic launch scope
* Supported currencies
* Supported languages
* Final storage provider
* Final notification provider
* Final hosting provider
* Final technology stack
* Mobile application technology
* Exact artwork categories
* Exact service model
* Licensing and intellectual-property rules

These decisions must be formally defined during the relevant project phase before they become implementation assumptions.
