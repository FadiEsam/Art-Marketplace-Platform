# Project Glossary

## 1. Purpose

This glossary defines the terminology used throughout the Art Marketplace Platform project.

Its purpose is to maintain consistent terminology across:

* Project documentation.
* Requirements.
* System design.
* Database design.
* API design.
* UI/UX design.
* Web application.
* Mobile application.
* Testing.
* Security.
* Deployment.
* Maintenance.

Definitions in this document describe the intended meaning of terms **within this project**.

This glossary does not replace detailed requirements, business rules, legal definitions, or technical specifications.

Where a term represents a concept whose detailed behavior has not yet been finalized, this glossary defines the concept without inventing unresolved rules.

---

# 2. Project and Product Terms

## 2.1 Art Marketplace Platform

The software project and resulting platform intended to provide a structured marketplace for discovering, presenting, and transacting around supported artwork.

The platform includes a Web application and, as part of the complete project, a Mobile Application supported by shared backend/API services.

---

## 2.2 Marketplace

A platform that enables interactions and transactions between independent parties.

In this project, the marketplace primarily connects Customers with approved Artists and supports the discovery and transaction of supported artwork.

---

## 2.3 MVP — Minimum Viable Product

The first complete version of the product that provides the approved core marketplace functionality.

The MVP is primarily Web-based and intentionally excludes capabilities such as platform-mediated payment, managed physical-artwork transactions, delivery integration, printing integration, and AI functionality.

---

## 2.4 Complete Project

The broader project extending beyond the MVP.

The complete project includes:

* Web application.
* Backend and APIs.
* Database.
* Mobile Application.
* Quality Assurance.
* Cybersecurity.
* Deployment.
* Maintenance.

The complete project is therefore broader than the MVP.

---

## 2.5 Future Product Scope

Capabilities intentionally outside the current MVP and potentially introduced later as the product evolves.

Examples include:

* Platform-mediated payment.
* Managed physical-artwork transactions.
* Printing integrations.
* Delivery integrations.
* AI functionality.

Future scope is not automatically part of the complete project until the relevant capability is formally included.

---

## 2.6 Artwork

A creative work presented through the platform.

Within the MVP marketplace, supported artwork focuses on digital artwork that can be represented and displayed as 2D visual content.

An artwork may be:

* Ready-made.
* Custom-created through an approved custom-workflow.

---

## 2.7 Digital Artwork

Artwork created or represented in digital form and suitable for the platform's supported digital/2D presentation model.

Examples may include:

* Digital drawings.
* Digital paintings.
* Character artwork.
* Engineering drawings.
* Photography.
* Nature artwork.
* Arabic calligraphy.

The exact supported file formats and technical limits are defined elsewhere.

---

## 2.8 Physical Artwork

An artwork whose original form is physical rather than purely digital.

Examples include:

* Paper drawings.
* Paintings.
* Physical illustrations.
* Other physical 2D artwork.

Physical artwork may be displayed in an Artist's portfolio where permitted, but physical marketplace transactions are outside the MVP.

---

## 2.9 Supported Artwork

Artwork that satisfies the platform's current technical, category, policy, and marketplace requirements.

Being technically displayable does not automatically mean that an artwork is eligible for marketplace transactions.

---

## 2.10 Ready-Made Artwork

An existing artwork that has already been created by the Artist and is offered to a Customer.

A ready-made artwork is different from a Custom Artwork because the work does not need to be created from a new Customer request.

---

## 2.11 Custom Artwork

Artwork created by an Artist according to requirements provided by a Customer.

Custom Artwork differs from Ready-Made Artwork in areas such as:

* Request workflow.
* Requirements.
* Availability.
* Payment structure.
* Revisions.
* Ownership and usage rights.

The exact workflow is defined in the Requirements documentation.

---

## 2.12 Portfolio

A collection of works presented by an Artist to demonstrate their artistic work, style, or experience.

A portfolio item does not automatically represent an artwork available for marketplace purchase.

A physical artwork may be shown in a portfolio without becoming a supported MVP marketplace transaction.

---

## 2.13 Listing

A published marketplace representation of an artwork or other approved marketplace offering.

A Listing contains the information necessary for users to discover and evaluate the associated offering.

The exact Listing structure is defined in Requirements.

---

## 2.14 Discovery

The process through which users find Artists or artwork.

Discovery may include:

* Browsing.
* Search.
* Filtering.
* Categories.
* Artist profiles.
* Artwork metadata.

---

## 2.15 Category

A classification used to organize artwork and/or Artist capabilities.

Artist approval is associated with an approved artistic category.

The exact category structure is defined during Requirements.

---

## 2.16 Dynamic Artwork Metadata

A rule-based mechanism that presents optional artwork information fields or questions based on the artwork category and previous selections.

Its purpose is to improve:

* Artwork descriptions.
* Search.
* Filtering.
* Discovery.

Dynamic Artwork Metadata does not require AI.

---

# 3. User and Stakeholder Terms

## 3.1 User

A person with an account on the platform.

Every new account begins as a Customer.

---

## 3.2 Customer

A platform user who can discover Artists and artwork and participate in the marketplace according to the permissions and capabilities available to the account.

A Customer may also become an Artist.

---

## 3.3 Artist

A platform user who has completed the required Artist approval process and is authorized to perform Artist-specific activities.

An Artist may:

* Maintain an Artist profile.
* Present a portfolio.
* Publish eligible artwork.
* Receive applicable custom requests.
* Participate in approved marketplace workflows.

An Artist remains capable of acting as a Customer.

---

## 3.4 Artist Application

The process through which a Customer requests Artist status.

The application includes:

* Selection of an artistic category.
* Submission of five samples of the applicant's own work.
* Specialist review.

---

## 3.5 Artist Reviewer

A specialist responsible for reviewing Artist applications and determining whether an applicant satisfies the platform's Artist approval requirements.

Detailed reviewer rules are defined in Requirements.

---

## 3.6 Administrator

A privileged platform user responsible for administrative and moderation operations.

Administrative capabilities may include:

* User management.
* Artist application review.
* Artwork moderation.
* Report handling.
* Account restrictions.
* Commission-related enforcement.
* Platform configuration.

---

## 3.7 Stakeholder

A person, organization, or external system that has an interest in, interacts with, influences, or is affected by the project or platform.

---

# 4. Marketplace Interaction Terms

## 4.1 Request

An initiated Customer request for a Custom Artwork or another approved marketplace action that has not yet reached the relevant confirmed transaction state.

A Request is not automatically an Order.

---

## 4.2 Order

A structured marketplace transaction record representing an approved purchase or agreed piece of work between a Customer and an Artist.

An Order may contain information such as:

* Customer.
* Artist.
* Artwork.
* Requirements.
* Price.
* Transaction status.
* Payment-related information.
* Completion information.

The exact Order structure depends on the approved workflow.

---

## 4.3 Order Lifecycle

The sequence of states through which an Order progresses.

The exact lifecycle differs according to the transaction type and must be defined in Requirements.

The project should not assume that Ready-Made and Custom Artwork use identical workflows.

---

## 4.4 Order Status

A value describing the current operational state of an Order.

Examples may include:

* Pending.
* Accepted.
* In Progress.
* Completed.
* Cancelled.
* Rejected.

The final states and transitions are defined in Requirements.

---

## 4.5 Requirement — Artwork Requirement

A specific condition or specification describing what an Artist is expected to create or provide for a Custom Artwork request.

Examples may include:

* Dimensions.
* Style.
* Subject.
* Content.
* Format.
* References.
* Required deliverables.

This term should not be confused with a **Software Requirement**.

---

## 4.6 Deliverable

An output that an Artist is required to provide as part of an approved artwork workflow.

For digital artwork, a Deliverable may be a digital file or other agreed digital output.

---

## 4.7 Revision

A permitted modification to Custom Artwork requested by the Customer according to the applicable revision rules.

The exact revision limits and conditions are defined in Requirements.

---

## 4.8 Completion

The state in which the applicable requirements for a marketplace workflow have been satisfied and the transaction is considered complete according to its defined rules.

Completion is not automatically equivalent to Delivery.

---

## 4.9 Cancellation

The termination of a Request or Order before its normal completion.

Eligibility, responsibility, timing, and financial consequences are defined in Requirements.

---

## 4.10 Dispute

A disagreement between parties concerning a marketplace matter.

Examples may include disagreements involving:

* Artwork.
* Requirements.
* Payment.
* Rights.
* Completion.
* Cancellation.

A complete dispute-resolution system is not automatically part of the MVP.

---

# 5. Payment and Commission Terms

## 5.1 Payment

The transfer of money associated with a marketplace transaction.

In the MVP, payment is made directly from the Customer to the Artist through bank transfer rather than through platform-mediated payment processing.

---

## 5.2 Direct Bank Transfer

A payment method in which the Customer transfers funds directly to the Artist's bank account outside the platform's own payment-processing infrastructure.

The platform may record relevant transaction information without acting as the payment processor.

---

## 5.3 Platform-Mediated Payment

A future payment model in which the platform uses a payment provider or other approved payment infrastructure to process marketplace payments.

Platform-mediated payment is outside the MVP.

---

## 5.4 Payment Provider

An external service capable of processing payments on behalf of the platform.

A Payment Provider is relevant to future platform-mediated payment functionality.

The MVP does not depend on a Payment Provider for marketplace payment processing.

---

## 5.5 Payment Status

A value describing the payment-related state recorded by the platform.

Because MVP payments occur externally, the platform's recorded payment state must not automatically be interpreted as proof that a bank has successfully processed the transfer.

The exact MVP payment-status model is defined in Requirements.

---

## 5.6 Platform Commission

The amount owed to the platform by an Artist according to the marketplace commission rules.

The current MVP commission rate is **15%**.

The commission is separate from any external bank or payment-processing fee.

---

## 5.7 Commission Obligation

The amount of platform commission that an Artist is required to settle.

---

## 5.8 Commission Settlement

The process through which an Artist fulfills an outstanding platform commission obligation.

The exact settlement mechanism is defined in Requirements.

---

## 5.9 Commission Enforcement

Restrictions that may be applied when applicable commission obligations remain unpaid.

The exact thresholds and restrictions are defined in Requirements.

---

## 5.10 Payment Processing Fee

A fee charged by an external payment provider or financial institution for processing a payment.

This is distinct from the platform's commission.

---

## 5.11 Escrow

A legal and financial arrangement in which funds are held by an appropriate party until defined conditions are satisfied.

The MVP does **not** implement a platform escrow model.

The term should not be used to describe the MVP's direct bank-transfer model.

---

# 6. Social Interaction Terms

## 6.1 Like

A user action indicating appreciation or positive interaction with an eligible artwork or supported platform object.

---

## 6.2 Follow

A user action allowing one user to follow another supported account or Artist.

---

## 6.3 Rating

A numerical evaluation assigned according to the platform's approved rating system.

The MVP uses a **1–5 star rating** model.

---

## 6.4 Notification

A system-generated message informing a user about a relevant platform event.

Users may have control over applicable notification preferences.

---

## 6.5 Report

A user-submitted report indicating that another user, artwork, or platform activity may violate platform rules.

---

## 6.6 Block

A user-controlled action that restricts specified interactions between users according to platform rules.

---

## 6.7 Comment

A public textual response associated with an artwork or other platform content.

Comments are outside the current project scope.

---

## 6.8 Dislike

A negative reaction feature separate from the approved Like and Rating mechanisms.

Dislike is outside the current project scope.

---

## 6.9 Spam

Unwanted or abusive content or behavior.

A dedicated Spam feature is outside the current project scope.

---

## 6.10 User-to-User Chat

Direct conversational messaging between platform users.

User-to-user Chat is outside the current MVP scope.

---

## 6.11 User-to-AI Chat

Conversational interaction between a platform user and an AI system.

User-to-AI Chat is outside the current MVP scope.

---

# 7. Rights and Intellectual Property Terms

## 7.1 Intellectual Property — IP

Legal rights associated with creative works, designs, software, trademarks, and other intellectual creations.

---

## 7.2 Ownership

The legal relationship determining who owns a creative work or associated intellectual property.

Technical ownership of a database record does not automatically determine legal ownership of the underlying artwork.

---

## 7.3 License

A permission granted to another party describing how a work may be used.

Licensing rules depend on the applicable business and legal requirements.

---

## 7.4 Usage Rights

The permissions governing how a Customer may use an artwork after obtaining it.

Usage Rights may include restrictions such as:

* Personal use.
* Commercial use.
* Reproduction.
* Modification.
* Redistribution.

Exact rules depend on the applicable artwork and legal requirements.

---

## 7.5 Artist Rights

Rights and protections applicable to Artists and their creative works.

---

## 7.6 Customer Rights

Rights and permissions applicable to Customers in relation to artwork and marketplace transactions.

---

# 8. Authentication and Authorization Terms

## 8.1 Authentication

The process of verifying the identity of a user.

---

## 8.2 Authorization

The process of determining what an authenticated user is allowed to access or perform.

Authentication answers:

> Who are you?

Authorization answers:

> What are you allowed to do?

---

## 8.3 Role

A defined category of permissions or responsibilities associated with a user or system actor.

Project roles may include:

* Customer.
* Artist.
* Administrator.

Artist is a capability associated with a user's account rather than necessarily a separate account identity.

---

## 8.4 Permission

An authorization rule allowing an actor to perform a specific action or access a specific resource.

---

## 8.5 RBAC — Role-Based Access Control

An authorization approach in which permissions are associated with roles.

The project may use RBAC or a more detailed authorization model where required by the system design.

---

## 8.6 Resource

A system entity or object that can be accessed, viewed, created, modified, or deleted.

Examples include:

* User.
* Artist profile.
* Artwork.
* Order.
* Request.
* Payment record.
* Commission record.
* Report.
* File.

---

## 8.7 Resource Ownership

The relationship between a resource and the user or entity that owns or controls it.

---

## 8.8 Audit Log

A record of important system or administrative actions.

An Audit Log may contain:

* Actor.
* Action.
* Target.
* Timestamp.
* Relevant metadata.

The exact events that require auditing are defined in Requirements and Security.

---

# 9. Artwork Metadata Terms

## 9.1 Metadata

Structured information describing an artwork or other system entity.

---

## 9.2 Required Metadata

Metadata that must be provided before an artwork can satisfy the relevant publication requirements.

---

## 9.3 Optional Metadata

Metadata that may be provided but is not universally required.

---

## 9.4 Category-Specific Metadata

Metadata that becomes relevant only to certain artwork categories.

---

## 9.5 Dynamic Metadata Question

An optional question presented based on predefined rules such as artwork category or previous answers.

---

# 10. Technical Terms

## 10.1 Frontend

The client-side software through which users interact with the platform.

The initial frontend is the Web application.

---

## 10.2 Web Application

The browser-based application that provides the primary MVP user experience.

---

## 10.3 Mobile Application

The mobile client developed as a core post-MVP project phase.

The Mobile Application consumes the backend/API services and is part of the complete project.

---

## 10.4 Backend

The server-side part of the platform responsible for:

* Business logic.
* API processing.
* Authentication.
* Authorization.
* Data access.
* Integration with external services.

---

## 10.5 API — Application Programming Interface

A defined interface through which software components communicate.

The platform backend exposes APIs for the Web application and future Mobile Application.

---

## 10.6 REST API

An API designed around resources and HTTP operations following REST architectural principles.

REST is the current API direction of the project unless changed through a documented technical decision.

---

## 10.7 Endpoint

A specific API route and HTTP operation used to access or manipulate a resource or perform an operation.

Example:

```text
GET /api/v1/artworks
```

---

## 10.8 Business Logic

Rules and processes that define how the platform operates.

Business logic should be enforced by trusted backend components where appropriate.

---

## 10.9 Relational Database

A database that stores structured data using tables and relationships.

The project uses a relational-database direction.

---

## 10.10 PostgreSQL

The current preferred relational database technology for the project.

Any final technology decision should be documented through the appropriate technical decision process.

---

## 10.11 Database Schema

The logical structure of database objects such as:

* Tables.
* Columns.
* Relationships.
* Constraints.
* Indexes.

---

## 10.12 Migration

A version-controlled change to the database structure.

---

## 10.13 Seed Data

Controlled initial or sample data used for development, testing, or demonstration.

Seed data must not contain real sensitive production information.

---

## 10.14 Object Storage

Storage designed for files and large binary objects.

Artwork and other large media may use object/file storage rather than being stored directly inside the relational database.

---

## 10.15 Environment

A distinct technical setup in which the system operates.

Common environments include:

* Development.
* Testing.
* Production.

---

## 10.16 Development Environment

An environment used to develop and locally test the system.

---

## 10.17 Testing Environment

An environment used to verify the system before production deployment.

---

## 10.18 Production Environment

The live environment used by real users.

Production requires stronger security, access control, monitoring, backup, and operational controls than development environments.

---

# 11. Software Engineering Terms

## 11.1 SDLC — Software Development Life Cycle

The structured process used to develop, test, deploy, and maintain the system.

The project lifecycle includes the major phases represented in the project roadmap.

---

## 11.2 Functional Requirement

A requirement describing a behavior or capability that the system must provide.

---

## 11.3 Non-Functional Requirement

A requirement describing a quality, characteristic, or constraint of the system.

Examples include:

* Security.
* Performance.
* Availability.
* Accessibility.
* Maintainability.

---

## 11.4 Business Rule

A rule defining how the marketplace or business process operates.

Business rules should be enforceable by the backend where appropriate.

---

## 11.5 User Story

A short description of a desired capability from a user's perspective.

Typical structure:

> As a [user], I want [capability], so that [benefit].

---

## 11.6 Use Case

A structured description of an interaction between an actor and the system to achieve a goal.

---

## 11.7 Acceptance Criterion

A condition that must be satisfied for a requirement or user story to be considered successfully implemented.

---

## 11.8 Traceability

The ability to connect requirements with their design, implementation, and testing artifacts.

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

## 11.9 Gate

A formal checkpoint used to determine whether a project phase satisfies its defined completion criteria.

---

## 11.10 Scope Change

A modification that adds, removes, or significantly changes an approved project scope element.

Significant scope changes should be documented through the project's decision-management process.

---

# 12. Architecture and Design Terms

## 12.1 System Architecture

The high-level structure of the system, including major components, responsibilities, communication mechanisms, data flows, and external dependencies.

---

## 12.2 Component

A distinct software or infrastructure unit with a defined responsibility.

Examples include:

* Web application.
* Backend API.
* Database.
* Object storage.
* Notification service.

---

## 12.3 Architecture Decision

A documented technical choice that has a meaningful impact on system structure or future development.

---

## 12.4 ADR — Architecture Decision Record

A document used to record an important architecture decision, including:

* Context.
* Problem.
* Decision.
* Alternatives.
* Consequences.

---

## 12.5 UML — Unified Modeling Language

A standardized modeling language used to communicate aspects of a software system.

Possible diagrams include:

* Use Case.
* Class.
* Sequence.
* Activity.
* State.
* Component.
* Deployment.

---

# 13. Security Terms

## 13.1 HTTPS

HTTP communication protected using TLS encryption.

HTTPS is required for production environments.

---

## 13.2 Secret

Sensitive information used to authenticate or authorize access to systems or services.

Examples include:

* API keys.
* Passwords.
* Tokens.
* Database credentials.
* Encryption keys.

Secrets must not be committed to source control.

---

## 13.3 Personal Data

Information that identifies or relates to an individual.

The exact legal classification depends on the deployment context and applicable law.

---

## 13.4 Threat

A potential cause of harm to the confidentiality, integrity, or availability of a system or its data.

---

## 13.5 Vulnerability

A weakness that could potentially be exploited to compromise a system.

---

## 13.6 Risk

The potential impact resulting from a threat exploiting a vulnerability.

Risk analysis may consider:

* Likelihood.
* Impact.
* Exposure.
* Existing controls.

---

## 13.7 Threat Model

A structured analysis of potential threats, attack surfaces, assets, and security controls.

---

# 14. Testing and Quality Terms

## 14.1 Test Case

A defined set of conditions, inputs, actions, and expected results used to verify system behavior.

---

## 14.2 Unit Test

A test that verifies a small isolated unit of application logic.

---

## 14.3 Integration Test

A test verifying that multiple components work correctly together.

---

## 14.4 End-to-End Test

A test that validates a complete user or system workflow.

---

## 14.5 System Test

A test performed against the integrated system to verify that it satisfies its requirements.

---

## 14.6 Regression Testing

Testing performed after changes to verify that existing functionality has not been unintentionally broken.

---

## 14.7 Bug

A defect or unexpected behavior in the software.

---

## 14.8 Quality Assurance

Systematic activities used to verify and improve software quality.

---

# 15. Deployment and Operations Terms

## 15.1 Deployment

The process of making a software version available in a target environment.

---

## 15.2 Docker

A containerization technology used to package applications and dependencies into reproducible environments.

Docker may be used where appropriate but does not imply that every project component must be containerized.

---

## 15.3 CI/CD

Continuous Integration and Continuous Delivery/Deployment practices used to automate activities such as:

* Building.
* Testing.
* Validation.
* Packaging.
* Deployment.

---

## 15.4 Monitoring

Continuous observation of system health, availability, performance, errors, and relevant operational metrics.

---

## 15.5 Backup

A copy of data or configuration maintained for recovery after loss, corruption, or failure.

---

## 15.6 Restore

The process of recovering data, configuration, or system functionality from a backup or other recovery source.

---

## 15.7 Deployment Runbook

A documented sequence of steps required to deploy, verify, troubleshoot, or roll back the system.

---

# 16. Documentation Terms

## 16.1 Project Charter

A document establishing the project's purpose, vision, high-level scope, objectives, stakeholders, and overall direction.

---

## 16.2 Project Scope

A document defining the boundaries of what the project includes and excludes.

---

## 16.3 Objective

A defined outcome that the project intends to achieve.

---

## 16.4 Assumption

A condition temporarily treated as true for planning or design purposes but not yet fully validated.

---

## 16.5 Constraint

A limitation that restricts project decisions, implementation, resources, technology, or scope.

---

## 16.6 Decision

A formally established project choice.

Important project-wide decisions are recorded in the project-wide Decision Log.

---

## 16.7 Decision Log

A record of important project-wide decisions and their context.

The Decision Log belongs at the project root because project-wide decisions may affect multiple phases.

---

## 16.8 Change Log

A chronological record of significant changes to the project, documentation, or software.

---

## 16.9 Roadmap

A high-level representation of planned project phases, capabilities, or future work.

A roadmap should not be interpreted as a guarantee that every future item will be implemented exactly as originally described.

---

# 17. External Service Terms

## 17.1 Third-Party Service

An external system operated by another organization that provides a capability used by the platform.

Examples may include:

* Email.
* Storage.
* Hosting.
* Payment.
* Printing.
* Delivery.

---

## 17.2 Integration

A technical connection between the platform and an external system or internal component.

---

## 17.3 Provider

An external organization or service responsible for supplying a technical capability.

---

## 17.4 Payment Provider

An external organization providing payment-processing capabilities.

Payment Provider integration is outside the MVP.

---

## 17.5 Printing Provider

An external service capable of producing physical printed versions of eligible artwork.

Printing integration is outside the MVP.

---

## 17.6 Delivery Provider

An external service capable of transporting physical products.

Delivery integration is outside the MVP.

---

# 18. Status and State Terms

## 18.1 State

A defined condition of a system entity at a particular point in time.

Examples:

```text
Artist Application → Under Review

Artwork → Published

Order → Completed
```

---

## 18.2 State Transition

A valid change from one state to another.

Example:

```text
Artist Application → Under Review → Approved
```

State transitions should be explicitly defined so invalid transitions can be prevented.

---

## 18.3 Status History

A record of changes to the status of an entity over time.

Status history may be required for important entities such as:

* Artist applications.
* Artwork.
* Orders.
* Commission obligations.
* Administrative actions.

---

# 19. Project-Specific Terminology Principles

The following terminology principles apply throughout the project:

1. **Customer and Artist are capabilities associated with the same user-account model.**
2. **Every new user begins as a Customer.**
3. **Artist status requires the approved Artist application and review process.**
4. **An Artist may continue to act as a Customer.**
5. **Ready-Made Artwork and Custom Artwork are distinct concepts.**
6. **Digital artwork being displayable does not automatically mean that every transaction type is supported.**
7. **Physical Artwork display is not the same as a managed physical marketplace transaction.**
8. **MVP marketplace transactions focus on supported digital artwork.**
9. **MVP payment uses direct Customer-to-Artist bank transfer.**
10. **Platform-mediated payment is a future capability, not an MVP dependency.**
11. **Platform Commission and external Payment Processing Fees are separate concepts.**
12. **The current MVP commission rate is 15%.**
13. **Payment Status must not be interpreted as proof of bank-side payment unless the applicable verification process establishes that fact.**
14. **User-to-user Chat and User-to-AI Chat are outside the current scope.**
15. **Comments, Dislike, and Spam are outside the current scope.**
16. **AI functionality is outside the MVP.**
17. **Dynamic Artwork Metadata is rule-based and does not require AI.**
18. **Delivery and Printing integrations are outside the MVP.**
19. **Mobile Application is outside the MVP but is a core phase of the complete project.**
20. **Authentication and Authorization are separate concepts.**
21. **Frontend restrictions must not be treated as sufficient backend authorization.**
22. **A Request is not automatically an Order.**
23. **Order Status and Payment Status are separate concepts.**
24. **Completion and Delivery are not automatically equivalent.**
25. **Ownership and technical database ownership are not automatically equivalent.**
26. **Technical implementation must not be used to infer legal rights.**
27. **Project-wide decisions belong in the project-wide Decision Log.**
28. **TBD information must not be treated as a finalized technical or business decision.**
29. **Terms should be used consistently across requirements, design, implementation, testing, and deployment documentation.**

---

# 20. Terms That Must Not Be Used as Current MVP Concepts

The following terms may appear in future-oriented documentation but should not be described as active MVP capabilities unless the scope is formally changed:

* Platform-Mediated Payment.
* Payment Provider Integration.
* Escrow.
* Managed Physical Artwork Transaction.
* Delivery Integration.
* Printing Integration.
* AI Recommendation.
* AI Artwork Generation.
* AI Chat.
* User-to-User Chat.
* Comments.
* Dislike.
* Spam.

Their presence in this glossary does not mean that the corresponding functionality is currently implemented or included in the MVP.

---

# 21. Terminology Maintenance

The glossary should be updated when:

* A new project-wide term is introduced.
* A term changes meaning.
* A formal decision changes an established concept.
* A requirement introduces terminology that will be reused across phases.
* A technical term becomes important to multiple project areas.
* A previously used term becomes obsolete.

Terminology changes should be reviewed for consistency across existing documentation.

A term should not be redefined differently in another project-wide document without a documented reason.

---

# 22. Source of Authority

The glossary defines terminology, but it does not independently establish:

* Detailed business rules.
* Detailed functional requirements.
* Database structures.
* API contracts.
* Legal contracts.
* Security controls.
* Implementation details.

When a glossary definition conflicts with an approved project decision or detailed requirement, the relevant authoritative document must be reviewed and the glossary updated to restore consistency.
