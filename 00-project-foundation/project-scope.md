# Project Scope

## 1. Scope Overview

This document defines the functional, product, platform, and technical boundaries of the Art Marketplace Platform.

It establishes:

* What is included in the MVP.
* What is excluded from the MVP.
* What belongs to the complete project.
* What is reserved for future product development.
* The primary users and platform capabilities.
* The supported artwork types.
* The transaction and commission model.
* The major external integrations.
* The main project and product boundaries.

This document defines scope at a foundation level. Detailed requirements, workflows, validation rules, permissions, API contracts, database structures, UI behavior, and implementation details are defined in the appropriate later phases.

The project follows a **Single Source of Truth** approach for scope. Detailed documents may expand on an approved capability, but they must not silently introduce functionality that contradicts this document or a later approved project-wide decision.

---

# 2. Project Scope Model

The project is divided into three related scope levels:

1. MVP Scope
2. Complete Project Scope
3. Future Product Scope

These levels must remain clearly distinguished.

---

## 2.1 MVP Scope

The MVP is the first functional version of the Art Marketplace Platform.

The MVP is primarily a **web-based digital art marketplace** focused on:

* Customer accounts.
* Artist onboarding and approval.
* Artist profiles.
* Digital artwork publishing.
* Ready-made digital artwork.
* Custom digital artwork requests and commissions.
* Artwork discovery.
* Search and filtering.
* Dynamic artwork metadata.
* Limited social interaction.
* Notifications.
* Reporting and user blocking.
* Administrative moderation.
* Direct customer-to-artist bank transfer.
* Platform commission tracking and enforcement.
* Basic artwork, ownership, and marketplace rules.

The MVP intentionally excludes capabilities that are not required for the initial marketplace model.

---

## 2.2 Complete Project Scope

The complete project extends beyond the MVP.

The complete project includes the engineering and product lifecycle required to develop the platform beyond the initial web MVP.

Major areas include:

* Web application.
* Backend and REST APIs.
* Relational database.
* Authentication and authorization.
* File and media handling.
* Mobile application.
* Quality assurance and testing.
* Cybersecurity.
* Deployment and hosting.
* Monitoring and maintenance.
* Supporting documentation.
* CI/CD where appropriate.

The **Mobile Application is a core project phase**.

It is outside the initial MVP, but it is not considered an optional future idea or merely a future product extension.

The intended project progression therefore includes both the Web application and Mobile application.

---

## 2.3 Future Product Scope

Some product capabilities are intentionally outside the MVP and may be introduced during later product development.

Future product capabilities may include:

* Platform-mediated payment processing.
* Automated payment settlement.
* Managed physical artwork transactions.
* Printing and print-on-demand services.
* Delivery and logistics integrations.
* Shipment tracking.
* AI-powered functionality.
* Advanced recommendation and personalization.
* Advanced marketplace capabilities.
* Additional operational and analytical capabilities.

Future product scope must not be treated as MVP scope unless an approved project decision explicitly changes the scope.

---

# 3. Product Scope

The Art Marketplace Platform is intended to connect customers with approved artists and provide a structured environment for discovering, presenting, purchasing, and requesting supported artwork.

The MVP supports:

* Customer accounts.
* Artist capabilities.
* Artist approval and category validation.
* Artist profiles.
* Artwork portfolios and listings.
* Digital artwork discovery.
* Ready-made digital artwork.
* Custom digital artwork requests.
* Search and filtering.
* Artwork metadata.
* Limited social interaction.
* Notifications.
* Reporting.
* User blocking.
* Administrative moderation.
* Direct customer-to-artist bank transfer.
* Platform commission tracking.
* Basic marketplace and rights rules.

Detailed business workflows and validation rules are defined during the Requirements phase.

---

# 4. User and Account Scope

## 4.1 Base User Model

All users begin as **Customers**.

A Customer may apply to become an Artist.

Artist capabilities are associated with the existing user account rather than requiring a separate identity.

An approved Artist may continue to use the platform as a Customer.

---

## 4.2 Artist Application and Approval

The MVP includes an Artist application and approval process.

An applicant must:

1. Select an artistic category.
2. Submit five samples of their own work.
3. Submit the application for specialist review.
4. Receive an approval or rejection decision.

An approved Artist may publish artwork within the category for which they were approved.

Detailed rules for:

* Application validation.
* Specialist review.
* Rejection.
* Resubmission.
* Similarity checking.
* Category restrictions.
* Artist status.
* Suspension.
* Removal.

are defined during the Requirements and Administration phases.

---

## 4.3 Artist Availability

Artists may indicate whether they are available to accept custom artwork requests.

Artist availability is part of the MVP custom-request model.

The exact availability states and business rules are defined during Requirements.

---

## 4.4 Administrator

Administrators are responsible for platform-level management and moderation.

Administrative capabilities may include:

* User management.
* Artist application review.
* Artist approval and rejection.
* Artist status management.
* Artwork moderation.
* Category management.
* Report handling.
* User restriction.
* Blocking enforcement.
* Commission enforcement.
* Platform configuration.
* Audit records.

Detailed permissions are defined in the Requirements and Security phases.

---

# 5. Artwork Scope

## 5.1 MVP Artwork Scope

The MVP supports **digital artworks that can be represented and displayed as 2D visual content**.

Examples include:

* Digital drawings.
* Digital paintings.
* Character drawings.
* Engineering drawings.
* Nature drawings.
* Photography.
* Arabic calligraphy.
* Other digital artwork that fits the supported 2D-display model.

The artwork category determines the relevant metadata and discovery attributes.

---

## 5.2 Ready-Made Digital Artwork

The MVP supports ready-made digital artwork.

A ready-made artwork is an existing digital work that an Artist has already created and makes available to Customers.

The workflow may include:

* Artwork listing.
* Availability.
* Pricing.
* Purchase.
* Payment-related status.
* Digital delivery.
* Ownership.
* Usage rights.
* Completion.

Detailed rules are defined during Requirements.

---

## 5.3 Custom Digital Artwork

The MVP supports custom digital artwork requests and commissions.

A Customer may request a new digital artwork from an Artist.

Custom artwork may include:

* Request creation.
* Requirements.
* Artist availability.
* Pricing.
* Payment-related status.
* Work progress.
* Submission.
* Revision requests.
* Final approval.
* Completion.
* Ownership and usage rights.

The exact workflow, state transitions, revision limits, cancellation rules, and protection rules are defined during Requirements.

---

# 6. Physical Artwork Scope

## 6.1 MVP Platform Transactions

Physical artwork is **not supported as a platform-managed marketplace transaction in the MVP**.

The MVP marketplace transaction model is focused on supported digital artwork.

---

## 6.2 Physical Artwork Display

The platform may allow an Artist to display physical artwork as part of their profile or portfolio.

Displaying physical artwork does not mean that the platform manages its sale.

For example, an Artist may display a physical painting in their portfolio while arranging any potential sale independently.

---

## 6.3 External Physical Sales

If an Artist and Customer independently agree to purchase a physical artwork:

* The transaction occurs outside the platform.
* The parties are responsible for agreeing on the transaction terms.
* Payment is arranged outside the platform.
* Delivery is arranged by the relevant parties.
* The platform does not manage the physical sale.
* The platform does not manage physical delivery.
* The platform does not apply its normal MVP marketplace commission to that external physical sale.

The detailed presentation and policy rules are defined during Requirements.

---

## 6.4 Future Physical Marketplace

Future versions may support selected physical artworks through a structured marketplace workflow.

Possible future capabilities include:

* Platform-managed physical artwork transactions.
* Printing services.
* Print-on-demand services.
* Delivery providers.
* Shipment tracking.
* Physical-order management.
* Printing-to-customer logistics.

These capabilities are outside the MVP.

Physical art forms that cannot reasonably be represented as supported 2D-display artwork, including sculpture, carving, sewing, pottery, and similar three-dimensional or non-2D forms, are outside the current project scope unless a future scope decision explicitly changes this boundary.

---

# 7. Dynamic Artwork Metadata

The MVP may use a dynamic artwork metadata/question flow to improve artwork description and discovery.

After an Artist uploads an artwork, the system may present additional optional questions or metadata fields based on:

* Artwork category.
* Previously selected options.
* Artwork characteristics.
* Predefined business rules.

Only the artwork category is universally required at the foundation scope level. Additional metadata may become required or optional depending on the selected category and the resulting question flow.

The purpose is to improve:

* Artwork descriptions.
* Search.
* Filtering.
* Discovery.
* Consistency of artwork information.

This mechanism does **not require AI**.

The Artist remains responsible for reviewing, accepting, or modifying suggested metadata values.

The exact question structure and implementation are defined during Requirements and System Design.

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

Dynamic artwork metadata may contribute to search and filtering.

AI-powered recommendations, behavioral personalization, and machine-learning recommendation systems are outside the MVP.

Advanced recommendation capabilities may be considered as future product functionality.

---

# 9. Social Interaction Scope

The MVP includes a limited set of social features.

The approved MVP social functionality includes:

Like.
Follow.
1–5 star Rating.
Customizable Notifications.
Report.
Block User.

The following features are outside the MVP and outside the scope of the project entirely:

Dislike.
Comments.
Live.
Posts.
Videos.
Community.
Spamming.

The following communication features are outside the MVP but remain within the scope of the project's planned final version:

User-to-user Chat.
User-to-AI Chat.

These exclusions and inclusions are intentional product-scope decisions. Features listed as outside the project entirely must not be designed, implemented, or treated as planned functionality unless the project scope is explicitly revised. Features listed as outside the MVP but within the final project scope are deferred to later development stages and must not be included in the MVP.

---

# 10. Notification Scope

The MVP includes notifications for relevant platform events.

Notifications may cover:

* Artist application status.
* Artwork-related events.
* Follow activity.
* Rating-related events where applicable.
* Orders and requests.
* Payment-related status.
* Commission-related status.
* Administrative actions.
* Reports or account restrictions where appropriate.

Users should have appropriate control over their notification preferences.

Exact notification triggers, channels, priorities, and preference rules are defined during Requirements.

---

# 11. Payment Scope

## 11.1 MVP Payment Model

The MVP does **not** include platform-mediated payment processing.

The MVP also does not require third-party payment-provider integration for marketplace payments.

Instead, the MVP uses a **direct bank-transfer model between the Customer and Artist**.

High-level model:

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

The exact confirmation and transaction-recording workflow is defined during Requirements.

---

## 11.2 Platform Commission

The MVP includes a **15% platform commission** owed by the Artist according to the approved marketplace rules.

The platform should maintain records for:

* Relevant sales.
* Commission amount.
* Outstanding commission.
* Commission settlement status.

The platform may enforce restrictions when commission obligations remain unpaid.

Possible restrictions may include:

* Restricting publication of additional artwork.
* Restricting acceptance of additional custom requests.
* Restricting other marketplace capabilities.

Exact thresholds and enforcement rules are defined during Requirements.

---

## 11.3 Future Platform-Mediated Payments

A future version may introduce platform-mediated payments.

Possible capabilities include:

* Online payment processing.
* Payment-provider integration.
* Automated settlement.
* Refund handling.
* Payment protection.
* Automated commission collection.

These capabilities are outside the MVP.

---

# 12. Order and Custom Workflow Scope

The platform may provide structured workflows for approved ready-made transactions and custom requests.

Possible workflow stages include:

* Request or purchase creation.
* Acceptance or rejection.
* Requirements confirmation.
* Payment-related status.
* Work progress.
* Submission.
* Revision requests where applicable.
* Final approval.
* Completion.

The exact state machine, cancellation rules, revision limits, ownership rules, and exception handling are defined during Requirements.

No detailed workflow should be implemented based solely on this foundation-level document.

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

These rules represent intended product behavior and are not a substitute for final legal advice.

Before a future public/commercial launch, the legal and rights framework may be reviewed with a qualified legal consultant where appropriate.

Detailed legal wording belongs in the relevant legal and requirements documentation.

---

# 14. Administration and Moderation Scope

The MVP includes administration and moderation capabilities required to operate the marketplace.

These may include:

* User management.
* Artist approval.
* Artwork moderation.
* Category management.
* Report handling.
* User-block enforcement.
* Account restrictions.
* Commission enforcement.
* Basic audit records.
* Platform configuration.

Detailed administrative permissions and workflows are defined during Requirements and Security.

---

# 15. Technical Project Scope

The complete technical project includes:

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
* Hosting.
* Monitoring.
* Backup foundations.
* CI/CD where appropriate.
* Mobile application.
* Maintenance.

The architecture should support progression from the Web MVP to the broader project without requiring unnecessary redesign of the entire system.

---

# 16. Platform Scope

## 16.1 Web Application

The Web application is the primary platform for the MVP.

It provides the initial user-facing marketplace experience and supports the approved MVP functionality.

---

## 16.2 Mobile Application

The Mobile Application is a **core project phase** and part of the intended final project.

It is outside the initial MVP, but it is not considered an optional future product extension.

The backend and API architecture should therefore support future mobile consumption.

Detailed mobile requirements and implementation decisions are defined in the Mobile Application phase.

---

# 17. External Integration Scope

The project may integrate with external services where required.

## 17.1 MVP / Core Infrastructure

Potential infrastructure integrations include:

* Email services.
* File/object storage.
* Hosting infrastructure.
* Other infrastructure services required by approved implementation decisions.

These integrations do not automatically represent marketplace features.

---

## 17.2 Future Product Integrations

The following are outside the MVP:

* Payment providers for marketplace payments.
* Printing providers.
* Print-on-demand providers.
* Delivery providers.
* Logistics services.
* Shipment tracking services.
* Other external marketplace services approved through future scope decisions.

An external service must not automatically become part of project scope merely because it is technically possible.

Its inclusion requires an appropriate documented requirement or decision.

---

# 18. AI Scope

All AI functionality is currently **outside the MVP**.

Potential future AI capabilities may include:

* AI-assisted artwork recommendations.
* AI-assisted Artist recommendations.
* Personalized discovery.
* Artist/customer matching.
* AI-generated artwork descriptions.
* AI-assisted metadata.
* Artwork analysis.
* AI-assisted moderation.
* AI customer support.
* AI-assisted artwork creation.
* AI chat.
* Other AI-based marketplace assistance.

These examples describe possible future directions and do not constitute approved MVP requirements.

No AI functionality should be introduced into the MVP unless the project scope is formally changed.

The dynamic artwork metadata system described in this document does **not** depend on AI.

---

# 19. Printing Scope

Printing is outside the MVP.

Future versions may integrate with printing or print-on-demand providers to support capabilities such as:

* Printing digital artwork.
* Print product creation.
* Print-order management.
* Printing physical versions of supported digital artwork.
* Coordination between Artist, platform, and printing provider.

The exact business model, providers, supported products, pricing, and workflow are future requirements.

Printing must not be treated as an MVP marketplace capability.

---

# 20. Delivery and Logistics Scope

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

A future delivery workflow may involve delivery directly from the Artist or from an external printing provider.

---

# 21. Enterprise Scope

The MVP does not target complex enterprise marketplace functionality.

Examples include:

* Multi-tenant organizations.
* Enterprise account hierarchies.
* Complex organizational permissions.
* Enterprise billing.
* Enterprise procurement workflows.

Such capabilities require separate business requirements before being considered.

---

# 22. Geographic and Localization Scope

The platform should avoid unnecessary architectural assumptions that prevent future expansion to additional regions.

Where appropriate, the system should be designed so the following can be configured or extended:

* Currency.
* Language.
* Locale.
* Time zone.
* Regional business rules.
* Legal and regulatory requirements.
* Payment methods.

The initial geographic and localization configuration is defined during Requirements and System Design.

---

# 23. Data Scope

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
* Ready-made artwork.
* Custom requests.
* Custom requirements.
* Revisions.
* Orders where applicable.
* Transaction records.
* Payment-related status.
* Commission records.
* Notifications.
* Ratings.
* Likes.
* Follows.
* Reports.
* Blocks.
* Administrative actions.
* Audit-related information.

This list identifies data domains rather than final database tables or schemas.

The final data model is defined during the Database phase.

---

# 24. Explicit MVP Exclusions

The following are explicitly outside the MVP:

1. Platform-mediated payment processing.
2. Third-party payment-provider integration for marketplace payments.
3. Platform-managed physical artwork transactions.
4. Printing-service integration.
5. Print-on-demand integration.
6. Delivery-provider integration.
7. Shipment tracking.
8. Physical logistics management.
9. AI functionality.
10. AI-powered recommendations.
11. AI chat.
12. User-to-user chat.
13. User-to-AI chat.
14. Comments.
15. Dislike.
16. Spam functionality.
17. Advanced machine-learning personalization.
18. Enterprise marketplace functionality.
19. Auction functionality.
20. Other functionality not required by the approved MVP requirements.

These exclusions are explicit project boundaries rather than merely postponed implementation tasks.

---

# 25. Complete Project Boundary

The complete project extends beyond the Web MVP.

The intended project lifecycle includes:

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

The Mobile Application is therefore part of the complete project.

The following are **not required to define the complete core project phases** and remain Future Product Scope:

* Platform-mediated payments.
* Managed physical marketplace transactions.
* Printing integrations.
* Delivery integrations.
* AI capabilities.
* Advanced marketplace extensions.

The MVP is an important product milestone within the complete project, but it does not define the entire project.

---

# 26. Future Product Development

Future product development may extend the platform beyond the approved MVP and its initial project scope. These capabilities represent planned or potential future directions and are not part of the MVP unless explicitly moved into MVP scope through a formal project decision.

## Payments

Future payment capabilities may include:

- Platform-mediated payments.
- Payment-provider integrations.
- Automated settlements.
- Refunds.
- Payment protection.
- Automated commission collection.

These capabilities would replace the MVP's direct buyer-to-artist payment approach and may be introduced after the required business, technical, and operational foundations are established.

## Physical Artwork

Physical-artwork capabilities are outside the MVP and may be introduced in later development stages for eligible and supported artwork types.

Future capabilities may include:

- Managed physical-art transactions.
- Printing of eligible digital artworks.
- Print-on-demand services.
- Physical order management.
- Delivery and logistics.
- Shipment tracking.
- Integration with printing providers.
- Integration with delivery and logistics providers.

The platform may therefore support a future workflow in which an eligible digital artwork can be printed and delivered as a physical product. Such capabilities would require separate requirements, operational processes, provider integrations, and scope decisions before implementation.

Artwork forms that are explicitly excluded from the project scope remain excluded unless the project scope is formally revised.

## AI

AI functionality is outside the MVP and may be introduced in later development stages.

Future AI capabilities may include:

- Personalized recommendations.
- Artist/customer matching.
- Artwork analysis.
- AI-assisted metadata.
- AI-generated descriptions.
- AI-assisted moderation.
- AI customer assistance.
- AI-assisted creation.

AI functionality remains subject to separate requirements, technical evaluation, responsible-use considerations, and future scope decisions.

## Advanced Marketplace Capabilities

Future marketplace development may include:

- Advanced discovery.
- Advanced personalization.
- Advanced analytics.
- Expanded operational tooling.
- Additional marketplace capabilities approved through future scope decisions.

These capabilities are not commitments to specific future implementations. Their inclusion depends on future requirements, technical feasibility, business needs, and explicit project decisions.

Future features remain subject to separate requirements, technical evaluation, business and operational considerations, and project decisions. Features described in this section must not be treated as part of the MVP unless they are explicitly moved into MVP scope through a formal project decision.
---

# 27. Scope Change Management

A significant change to the approved scope should be documented as a project decision.

A scope change should identify, where applicable:

1. Requested change.
2. Reason for the change.
3. Problem or opportunity being addressed.
4. Effect on MVP scope.
5. Effect on complete-project scope.
6. Effect on future product scope.
7. Business impact.
8. Technical impact.
9. Architecture impact.
10. Requirements impact.
11. Testing impact.
12. Documentation impact.
13. Dependencies.
14. Decision.
15. Decision owner.

When an approved decision changes the scope, affected documentation should be updated.

Historical decisions should not be silently rewritten. If an earlier decision becomes obsolete, it should be marked as **Superseded** and replaced or clarified by the newer approved decision.

---

# 28. Scope Boundary Test

A proposed capability should be evaluated before being added to the MVP.

Consider:

### 1. Core Marketplace Need

Is the capability required for the approved MVP marketplace workflow?

### 2. User Value

Does it solve a meaningful problem for the intended MVP users?

### 3. Dependency

Does it require an external service or capability intentionally outside the MVP?

### 4. Complexity

Does it introduce disproportionate architectural, security, operational, or maintenance complexity?

### 5. Timing

Can the capability reasonably be implemented later without preventing the MVP from achieving its purpose?

### 6. Existing Scope

Is the capability already explicitly excluded by an approved project decision?

A capability that is useful but not necessary for the MVP should normally remain outside the MVP unless a documented scope change approves its inclusion.

---

# 29. Scope Completion Criteria

The Project Scope definition is considered sufficiently established when:

* MVP boundaries are clearly defined.
* Complete-project boundaries are identified.
* Future product scope is distinguished from the complete project.
* Primary users and account relationships are defined.
* Artist approval is defined at a foundation level.
* Artwork boundaries are defined.
* Physical artwork boundaries are defined.
* Dynamic artwork metadata is defined.
* Payment boundaries are defined.
* Commission boundaries are defined.
* Social interaction boundaries are defined.
* AI boundaries are defined.
* Mobile application scope is defined.
* Platform boundaries are defined.
* Major integrations are identified.
* Major exclusions are explicit.
* Scope-change rules are established.
* Detailed requirements can be developed without relying on unresolved scope assumptions.

Detailed requirements may refine behavior and implementation without changing the established scope boundaries.

---

# 30. Scope Authority

This document is the primary foundation-level reference for project scope.

Detailed documents may expand on the behavior of an in-scope capability, but they must not silently introduce functionality that contradicts the approved scope.

If a conflict exists between this document and a later approved project-wide decision, the decision must be recorded in the project-wide `decision-log.md`, and all affected documentation should be updated accordingly.
