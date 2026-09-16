# Project Scope

## 1. Scope Overview

This document defines the functional, technical, platform, and product boundaries of the Art Marketplace Platform.

It establishes:

* What is included in the MVP.
* What is excluded from the MVP.
* What belongs to the broader complete project.
* What is intentionally reserved for future product development.
* The main users, capabilities, integrations, and data areas involved in the project.
* The boundaries that should be respected during requirements, design, implementation, testing, and deployment.

This document defines scope at a foundation level. Detailed business rules, workflows, validation rules, permissions, API contracts, database structures, and implementation details are defined in the appropriate later-phase documentation.

The project follows a **Single Source of Truth** approach. This document defines scope boundaries, while detailed behavior is documented in the relevant requirements and technical documents.

---

# 2. Project Scope Model

The project is divided into three scope levels.

## 2.1 MVP Scope

The MVP is the first functional version of the platform.

The MVP is primarily a **Web-based art marketplace** and focuses on establishing the core marketplace, artist onboarding, artwork discovery, digital artwork publishing, customer interaction, moderation, and the initial transaction model.

The MVP does not attempt to implement every capability planned for the complete project.

---

## 2.2 Complete Project Scope

The complete project extends beyond the MVP.

The complete project includes:

* Web application.
* Backend and APIs.
* Relational database.
* Mobile application.
* Quality assurance and testing.
* Security and cybersecurity work.
* Deployment and hosting.
* Monitoring and maintenance.
* Supporting documentation and project lifecycle activities.

The Mobile Application is a **core project phase**, not an optional or merely future platform extension. It is planned after the initial Web MVP and depends on the backend/API foundation established earlier.

---

## 2.3 Future Product Scope

Some product capabilities are intentionally outside the MVP and may be introduced after the MVP or during later product evolution.

Examples include:

* Platform-mediated payment processing.
* Managed physical artwork transactions.
* Printing-service integrations.
* Delivery and logistics integrations.
* AI-powered functionality.
* Other capabilities approved through future scope decisions.

Future scope must not be treated as MVP scope unless a documented scope change explicitly changes the boundary.

---

# 3. Product Scope

The Art Marketplace Platform is intended to connect customers with approved artists and provide a structured environment for discovering, presenting, and transacting around artwork.

The platform supports:

* Customer accounts.
* Artist capabilities.
* Artist approval and category validation.
* Artwork portfolios and listings.
* Digital artwork discovery.
* Ready-made digital artwork.
* Custom digital artwork requests where included by the approved MVP workflow.
* Search and filtering.
* Artwork metadata.
* Social interaction features defined for the MVP.
* Notifications.
* Reporting and user blocking.
* Administrative moderation.
* The MVP payment model based on direct customer-to-artist bank transfer.
* Platform commission tracking and enforcement.
* Basic rights and marketplace rules.

The exact workflow and business rules for each capability are defined in the Requirements phase.

---

# 4. User and Account Scope

## 4.1 Base User Model

All users begin as **Customers**.

A Customer may later apply to become an Artist.

Artist capability is associated with the user's existing account rather than requiring a completely separate user identity.

An approved Artist may continue to use the platform as a Customer.

---

## 4.2 Artist Application and Approval

The MVP includes an artist approval process.

An applicant must:

1. Select an artistic category.
2. Submit five samples of their own work.
3. Submit the application for specialist review.
4. Receive an approval or rejection decision.

An approved Artist may publish artwork within the category for which they were approved.

Detailed rules for:

* Application validation.
* Review.
* Rejection.
* Resubmission.
* Similarity checks.
* Category restrictions.
* Artist status.
* Suspension or removal.

will be defined in the Requirements and Administration documentation.

---

## 4.3 Administrator

Administrators are responsible for platform-level management and moderation.

Administrative capabilities may include:

* User management.
* Artist application review.
* Artist status management.
* Artwork moderation.
* Report handling.
* Account restrictions.
* Platform rule enforcement.
* Commission-related enforcement.
* Audit and administrative records.

Exact administrative permissions are defined later.

---

# 5. Artwork Scope

## 5.1 MVP Marketplace Artwork

The MVP marketplace supports **digital artworks that can be represented and displayed as 2D visual content**.

Examples include:

* Digital drawings.
* Digital paintings.
* Character artwork.
* Engineering drawings.
* Nature artwork.
* Photography.
* Arabic calligraphy.
* Other digital artwork that fits the platform's supported 2D representation.

The artwork category and associated metadata determine how the artwork is described and discovered.

---

## 5.2 Ready-Made Digital Artwork

The MVP supports ready-made digital artwork.

A ready-made artwork is an existing work that the Artist has already created and makes available to Customers.

Its detailed rules include:

* Artwork listing.
* Availability.
* Pricing.
* Purchase workflow.
* Ownership and usage rights.
* Delivery of the digital work.

The detailed rules are defined during Requirements.

---

## 5.3 Custom Digital Artwork

The project includes the concept of custom artwork/commission requests.

A Customer may request a new digital artwork from an Artist.

Custom artwork differs from ready-made artwork in areas such as:

* Request workflow.
* Requirements.
* Availability.
* Pricing.
* Payment structure.
* Revisions.
* Ownership and usage rights.
* Completion and approval.

The complete custom-workflow rules must be defined in Requirements before implementation.

If a part of the custom workflow cannot be safely or reliably supported by the MVP's payment and protection model, that part must remain outside the MVP until its requirements are formally approved.

---

# 6. Physical Artwork Scope

## 6.1 MVP Marketplace Transactions

Physical artwork is **not supported as a platform-managed marketplace transaction in the MVP**.

The MVP transaction workflow is focused on digital artwork.

---

## 6.2 Physical Artwork Display

An Artist may be allowed to display or present physical artworks as part of their profile or portfolio.

Displaying a physical artwork does not mean that the platform supports its marketplace transaction.

For example, a physical painting may be shown in an Artist's portfolio while remaining outside the platform's managed purchase and delivery workflow.

---

## 6.3 External Physical Sales

If the platform permits an Artist to present a physical artwork and a Customer independently agrees to purchase it:

* The transaction is arranged outside the platform.
* The Customer and Artist are responsible for agreeing on the transaction terms.
* Delivery is arranged by the relevant parties.
* The platform does not manage physical delivery.
* The platform does not process the physical sale as an MVP marketplace transaction.
* The platform does not apply its normal marketplace commission to that external physical sale.

The exact presentation and policy rules are defined separately.

---

## 6.4 Future Physical Marketplace Support

Future versions may support selected physical artworks through a structured marketplace workflow.

Possible future capabilities include:

* Physical artwork transactions.
* Printing services.
* Delivery providers.
* Shipment tracking.
* Physical-order management.

These capabilities are outside the MVP.

Physical art forms that cannot reasonably be represented as supported 2D-display artwork, such as sculpture, carving, sewing, pottery, and similar three-dimensional or non-2D forms, are outside the current project scope unless a future scope decision explicitly changes this boundary.

---

# 7. Dynamic Artwork Metadata

The MVP may use a dynamic metadata/question flow to improve artwork description and discovery.

After an Artist uploads an artwork, the system may present additional optional questions or metadata fields based on:

* Artwork category.
* Previously selected options.
* Artwork characteristics.
* Other predefined rules.

The purpose is to improve:

* Artwork descriptions.
* Search.
* Filtering.
* Discovery.
* Consistency of artwork information.

This mechanism does **not require AI**.

The Artist remains responsible for reviewing, accepting, or modifying the proposed metadata values.

The exact question structure and implementation will be defined during Requirements and System Design.

---

# 8. Search and Discovery Scope

The MVP includes basic artwork and Artist discovery capabilities.

These may include:

* Browsing.
* Search.
* Category-based discovery.
* Filtering.
* Artist profile discovery.
* Artwork metadata-based discovery.

The dynamic metadata system may contribute to filtering and discovery.

AI-powered recommendations, behavioral personalization, and machine-learning recommendation systems are outside the MVP.

---

# 9. Social Interaction Scope

The MVP includes a limited set of social features intended to support interaction around Artists and artwork.

The approved MVP social capabilities are:

* Like.
* Follow.
* 1–5 star rating.
* Customizable notifications.
* Report.
* Block user.

The following are explicitly excluded from the MVP and are not part of the current planned product scope:

* Dislike.
* Comments.
* Spam functionality.
* User-to-user chat.
* User-to-AI chat.

The platform is not intended to become a general-purpose social network.

---

# 10. Notification Scope

The MVP includes notifications for relevant platform events.

Notifications may cover events such as:

* Artist application status.
* Artwork-related events.
* Follow activity.
* Rating-related events where applicable.
* Orders or requests.
* Payment-related status.
* Commission-related status.
* Administrative actions.
* Reports or account restrictions where appropriate.

Users should have appropriate control over notification preferences.

Exact notification channels, triggers, priority, and preference rules are defined during Requirements.

---

# 11. Payment Scope

## 11.1 MVP Payment Model

The MVP does **not** include platform-mediated payment processing or third-party payment-provider integration.

Instead, the MVP uses a direct bank-transfer model between Customer and Artist.

The high-level process is:

```text
Customer
   ↓
Direct Bank Transfer
   ↓
Artist
   ↓
Platform records relevant transaction information
```

The platform does not act as the payment processor for the MVP transaction.

---

## 11.2 Platform Commission

The MVP includes a **15% platform commission** owed by the Artist according to the approved marketplace rules.

The platform should maintain the necessary records to determine:

* Relevant sales.
* Commission amounts.
* Outstanding commission.
* Commission settlement status.

The platform may enforce restrictions when commission obligations remain unpaid.

Examples of possible restrictions include restrictions on:

* Publishing additional artwork.
* Accepting additional custom requests.
* Other marketplace capabilities.

The exact thresholds and enforcement rules must be defined in Requirements.

---

## 11.3 Future Platform-Mediated Payments

A future version may introduce platform-mediated payment through suitable payment providers.

Future payment capabilities may include:

* Online payment processing.
* Platform-held transaction funds where legally and technically appropriate.
* Automated settlement.
* Refund handling.
* Payment protection.
* Automated commission collection.

These capabilities are outside the MVP.

---

# 12. Order and Custom Workflow Scope

The platform may provide structured workflows for transactions and custom requests that are approved for the MVP.

Detailed workflows may include:

* Request creation.
* Acceptance or rejection.
* Requirements confirmation.
* Payment-related status.
* Work progress.
* Submission.
* Revision requests where applicable.
* Final approval.
* Completion.

The exact state machine, cancellation rules, revision limits, ownership rules, and exception handling must be defined during Requirements.

No final workflow should be implemented based solely on this scope document.

---

# 13. Rights and Marketplace Rules

The MVP includes basic rules governing:

* Artist rights.
* Customer rights.
* Artwork ownership.
* Usage rights.
* Custom-work ownership where applicable.
* Platform responsibilities.
* User responsibilities.

These rules represent the intended product behavior and are not a substitute for final legal advice.

Before a future public/commercial launch, the rights and legal framework may be reviewed and adjusted with a qualified legal consultant where appropriate.

Detailed legal wording and enforceable terms are outside the responsibility of this scope document.

---

# 14. Administration and Moderation Scope

The MVP includes platform administration and moderation capabilities necessary to operate the marketplace.

These may include:

* User management.
* Artist approval.
* Artwork moderation.
* Category management.
* Report handling.
* User blocking enforcement.
* Account restrictions.
* Commission enforcement.
* Basic audit records.
* Platform configuration.

The exact permission model and administrative workflows are defined in the Requirements and Security phases.

---

# 15. Technical Project Scope

The complete technical project includes the following major areas:

* Web application.
* Backend/API layer.
* Relational database.
* Authentication.
* Authorization.
* File and media handling.
* API documentation.
* Testing.
* Security.
* Deployment.
* Monitoring.
* Backup foundations.
* CI/CD where applicable.
* Mobile application.
* Maintenance.

The architecture should support the planned progression from the Web MVP to the broader project without requiring an unnecessary redesign of the entire system.

---

# 16. Platform Scope

## 16.1 Web Application

The Web application is the primary platform for the MVP.

It provides the initial user-facing marketplace experience and supports the approved MVP functionality.

---

## 16.2 Mobile Application

The Mobile Application is a **core project phase** and part of the project's intended final form.

It is outside the initial MVP but is not considered an optional future extension.

The backend and API architecture should therefore support future Mobile consumption.

Detailed mobile requirements and implementation decisions are defined in the Mobile Application phase.

---

# 17. External Integration Scope

The project may eventually integrate with external services where required.

Potential integration areas include:

### MVP or Core Infrastructure

* Email services.
* File/object storage.
* Hosting infrastructure.
* Other infrastructure services required by approved implementation decisions.

### Outside MVP / Future Product

* Payment providers.
* Printing providers.
* Delivery providers.
* Logistics services.
* Other external marketplace services approved through future scope decisions.

An external service must not automatically become part of the project scope merely because it is technically possible.

Its inclusion requires an appropriate documented requirement or decision.

---

# 18. AI Scope

All AI functionality is currently **outside the MVP**.

This includes, but is not limited to:

* AI-generated artwork.
* AI artwork recommendations.
* AI Artist recommendations.
* AI-generated descriptions.
* AI automatic pricing.
* AI moderation.
* AI customer support.
* AI-assisted artwork creation.
* AI chat.
* AI-based marketplace assistance.

AI may be reconsidered in future product development.

No AI functionality should be introduced into the MVP unless the scope is formally changed.

---

# 19. Delivery and Logistics Scope

Delivery and logistics are outside the MVP.

The MVP does not include:

* Delivery-provider integration.
* Shipment tracking.
* Warehousing.
* Packaging management.
* Physical delivery management.
* Delivery route management.
* Printing-to-customer logistics.

Future versions may introduce these capabilities where required by the product model.

---

# 20. Enterprise Scope

The MVP does not target complex enterprise marketplace functionality.

Examples include:

* Multi-tenant organizations.
* Enterprise account hierarchies.
* Complex organizational permissions.
* Enterprise billing.
* Enterprise procurement workflows.

Such capabilities require separate business requirements before being considered.

---

# 21. Geographic and Localization Scope

The platform should avoid unnecessary architectural assumptions that prevent future expansion to additional regions.

Where appropriate, the system should be designed so that the following can be configured or extended:

* Currency.
* Language.
* Locale.
* Time zone.
* Regional business rules.
* Legal/regulatory requirements.
* Payment methods.

The initial geographic and localization configuration will be defined by the relevant requirements and implementation decisions.

---

# 22. Data Scope

The project may manage data related to:

* User accounts.
* User profiles.
* Artist applications.
* Artist profiles.
* Artist categories.
* Artist approval records.
* Artwork.
* Artwork metadata.
* Artwork categories.
* Artwork availability.
* Ready-made artwork transactions.
* Custom requests.
* Requirements.
* Revisions.
* Orders where applicable.
* Payment and commission records.
* Notifications.
* Ratings.
* Likes.
* Follows.
* Reports.
* Blocks.
* Administrative actions.
* Audit-related information.

The final data model is defined during the Database phase.

This list identifies data domains rather than final database tables or schemas.

---

# 23. Explicit MVP Exclusions

The following capabilities are explicitly outside the MVP:

1. Platform-mediated payment processing.
2. Third-party payment-provider integration for marketplace payments.
3. Managed physical artwork transactions.
4. Delivery and logistics integration.
5. Printing-service integration.
6. AI functionality.
7. User-to-user chat.
8. User-to-AI chat.
9. Comments.
10. Dislike.
11. Spam functionality.
12. Advanced AI or machine-learning recommendations.
13. Enterprise marketplace functionality.
14. Other functionality not required by the approved MVP requirements.

These exclusions should be treated as explicit boundaries rather than temporary omissions.

---

# 24. Complete Project Boundary

The complete project extends beyond the MVP.

The planned lifecycle includes:

```text
Project Foundation
        ↓
Requirements
        ↓
System Design
        ↓
Database
        ↓
Web Application
        ↓
Mobile Application
        ↓
Quality Assurance
        ↓
Cybersecurity
        ↓
Deployment
        ↓
Maintenance
```

The complete project therefore represents more than the MVP Web marketplace.

The MVP is an important product milestone within the broader project rather than the definition of the entire project.

---

# 25. Scope Change Management

A significant change to the approved scope should be documented as a project decision.

A scope change should identify, where applicable:

1. Requested change.
2. Reason for the change.
3. Problem or opportunity being addressed.
4. Effect on MVP or complete-project scope.
5. Business impact.
6. Technical impact.
7. Architecture impact.
8. Requirements impact.
9. Testing impact.
10. Documentation impact.
11. Dependencies.
12. Decision.
13. Decision owner.

When an approved decision changes the scope, all affected documentation should be updated.

Historical decisions should not be silently rewritten. If a previous decision becomes obsolete, it should be marked as superseded and replaced by a new documented decision.

---

# 26. Scope Boundary Test

A proposed capability should be evaluated before being added to the MVP.

Consider:

### 1. Core Marketplace Need

Is the capability required for the approved MVP marketplace workflow?

### 2. User Value

Does the capability solve a meaningful problem for the intended MVP users?

### 3. Dependency

Does it require an external service or capability that is intentionally outside the MVP?

### 4. Complexity

Does it introduce disproportionate architectural, security, operational, or maintenance complexity?

### 5. Timing

Can the capability reasonably be implemented after the MVP without preventing the MVP from achieving its purpose?

### 6. Existing Scope

Is the capability already explicitly excluded by an approved project decision?

A capability that is useful but not necessary for the MVP should normally remain outside the MVP unless there is a documented reason to change the scope.

---

# 27. Scope Completion Criteria

The Project Scope definition is considered sufficiently established when:

* MVP boundaries are clearly defined.
* Complete-project boundaries are identified.
* Future product scope is distinguished from the complete project.
* Primary users and account relationships are defined.
* Artwork boundaries are defined.
* Physical artwork boundaries are defined.
* Payment boundaries are defined.
* Social interaction boundaries are defined.
* AI boundaries are defined.
* Platform boundaries are defined.
* Major integrations are identified.
* Major exclusions are explicit.
* Scope-change rules are established.
* Detailed requirements can be developed without relying on unresolved scope assumptions.

Detailed requirements may still refine behavior and implementation without changing the established scope boundaries.

---

## 28. Scope Authority

This document is the primary foundation-level reference for project scope.

Detailed documents may expand on the behavior of an in-scope capability, but they must not silently introduce functionality that contradicts the approved scope.

If a conflict exists between this document and a later approved project decision, the decision should be recorded in the project-wide `decision-log.md`, and the affected documentation should be updated accordingly.
