# Project Constraints

## 1. Purpose

This document defines the constraints that limit the design, development, deployment, operation, or evolution of the Art Marketplace Platform.

A constraint is a boundary that restricts the available solutions or decisions.

Constraints are different from:

* **Requirements:** What the system must do.
* **Decisions:** What the project intentionally chooses.
* **Assumptions:** What is temporarily treated as true until validated.
* **Scope:** What is included or excluded from a particular project stage.

A project decision may be influenced by a constraint, but the two should not be treated as the same thing.

---

# 2. Constraint Principles

The project should follow these principles:

1. Constraints must be considered when defining requirements and making design decisions.
2. A constraint should be documented explicitly when it materially affects the project.
3. A constraint should not introduce an undocumented feature or requirement.
4. Technical constraints should not unnecessarily restrict future development.
5. MVP constraints should not automatically become permanent constraints on the complete project.
6. When a constraint changes, affected decisions and documentation should be reviewed.
7. Security, privacy, and legal constraints should take priority over convenience.
8. Project constraints should be reviewed when moving between major lifecycle stages.

---

# 3. Product Constraints

## C-P01 — MVP Must Remain Focused

The MVP must remain focused on the approved core marketplace functionality.

Features that are not necessary for the MVP must not be introduced merely because they are technically possible.

This constraint exists to prevent unnecessary scope expansion and premature complexity.

---

## C-P02 — MVP Is Primarily Web-Based

The initial MVP is delivered primarily through the Web application.

The Mobile Application is outside the MVP, but it remains a core part of the complete project.

Therefore, MVP implementation must not require the complete Mobile Application to be implemented before the Web MVP can be completed.

---

## C-P03 — Digital Marketplace Focus

The MVP marketplace is focused on supported digital artwork intended for digital/2D display.

The MVP supports digital works such as, where applicable:

* Character drawings.
* Engineering drawings.
* Nature drawings.
* Photography.
* Arabic calligraphy.
* Other approved digital artwork categories that fit the project's supported representation.

Physical artwork may be displayed or listed for portfolio purposes under approved product behavior, but physical artwork is not a platform-managed marketplace transaction in the MVP.

---

## C-P04 — Supported Artwork Representation

Artwork supported by the MVP marketplace must be representable through the platform's approved digital/2D visual model.

The ability to upload or display an image of an object does not automatically mean that the underlying physical art form is supported as a marketplace product.

Three-dimensional or non-2D-display art forms are outside the approved marketplace model unless the project scope is explicitly changed.

---

# 4. Payment Constraints

## C-PAY01 — No Platform-Mediated Payment in MVP

The MVP must not depend on integrated platform-mediated payment processing.

The initial transaction model uses direct payment from Customer to Artist through bank transfer.

This constraint means that MVP workflows must not assume that the platform can:

* Charge a Customer directly.
* Hold Customer funds.
* Automatically transfer funds to Artists.
* Automatically refund funds through a payment provider.
* Depend on a payment-provider API for marketplace transactions.

Platform-mediated payment is a future product capability and must be introduced only through explicit future requirements and design decisions.

---

## C-PAY02 — Payment-Related Workflows Must Respect External Payment

Because MVP payment occurs outside the platform's payment-processing infrastructure, the system must clearly distinguish between:

* Payment information recorded by the platform.
* Payment actually processed through the external bank.
* Payment confirmation or verification.
* Marketplace transaction state.

The exact verification and recording mechanism must be defined during Requirements, System Design, and Cybersecurity analysis where applicable.

---

## C-PAY03 — Commission Must Be Trackable

The MVP must support the approved commission model without requiring a payment gateway.

The platform must be capable of recording applicable commission obligations and their settlement status.

The approved project commission is **15%** where applicable.

The detailed enforcement mechanism belongs in Requirements and System Design.

---

# 5. Artwork and Media Constraints

## C-M01 — Uploaded Media Must Be Validated

Artwork uploads must be subject to appropriate validation.

Validation requirements may include:

* File type.
* File size.
* File content.
* Upload permissions.
* Storage rules.
* Security restrictions.
* Appropriate access and visibility rules.

Exact limits and validation rules are defined during Requirements and System Design.

---

## C-M02 — Media Storage Must Be Secure

Artwork and media files must not be stored or served through an architecture that unnecessarily exposes private or protected content.

Access to media must respect applicable:

* Artwork ownership.
* Visibility.
* Publishing.
* Marketplace.
* User authorization rules.

---

## C-M03 — Media Storage Must Consider Scalability

Artwork files may consume substantially more storage than ordinary application data.

The architecture should therefore avoid assuming that all media must be stored directly inside the primary relational database.

The final storage mechanism is a technical design decision.

---

# 6. User and Account Constraints

## C-U01 — Unified User Identity Model

The project uses a unified user-account model.

A user does not need to create a completely separate account merely to become an Artist.

Artist capabilities are associated with the user's existing account.

All users initially enter the platform as Customers and may apply for Artist status through the approved process.

---

## C-U02 — Artist Approval Is Required

A user must not receive unrestricted Artist publishing capabilities before completing the approved Artist application and review process.

The Artist approval process includes:

1. Selecting an applicable art category.
2. Submitting five samples of the applicant's own work.
3. Specialist review of the submitted samples.
4. Approval or rejection according to the defined review rules.

Detailed rejection, resubmission, and similarity rules belong in the appropriate Requirements and System Design documentation.

---

## C-U03 — Artist Publishing Must Respect Approved Category

An approved Artist must not publish artwork outside the category for which the Artist has been approved, unless an approved future requirement changes this rule.

---

## C-U04 — Backend Authorization Is Mandatory

Restricted actions must not rely solely on frontend controls.

The backend must enforce authorization for sensitive operations such as:

* Artist-only actions.
* Administrative actions.
* Artwork management.
* Protected user data.
* Commission information.
* Reports.
* User restrictions.
* Other restricted resources.

---

# 7. Artwork Metadata Constraints

## C-MD01 — Category Is the Core Required Classification

Artwork category is the fundamental classification required for supported artwork.

Other artwork metadata may be collected according to the selected category and applicable answers.

---

## C-MD02 — Dynamic Metadata Must Remain Rule-Based

The MVP may use a dynamic metadata/question mechanism in which additional fields or questions depend on:

* The selected artwork category.
* Previous answers.
* Applicable product rules.

This mechanism must be implementable through predefined application rules.

It must not require AI functionality.

---

## C-MD03 — Optional Metadata Must Not Become an Unnecessary Barrier

Additional artwork metadata should support search, discovery, filtering, and clearer artwork information without unnecessarily preventing Artists from publishing valid artwork.

Only fields explicitly defined as required by the applicable product rules should be mandatory.

---

# 8. Social Feature Constraints

## C-S01 — Limited Social Scope

The MVP social model is intentionally limited.

The approved MVP features are:

* Like.
* Follow.
* 1–5 star rating.
* Customizable notifications.
* Report.
* Block user.

The project must not introduce additional social features without an approved scope change.

---

## C-S02 — No General-Purpose Chat

The platform must not depend on user-to-user chat for its MVP workflows.

User-to-user chat is outside the current scope.

User-to-AI chat is also outside the current scope.

---

## C-S03 — No Comments, Dislike, or Spam

The project must not introduce:

* Comments.
* Dislike.
* Spam functionality.

These are outside the current product scope.

---

# 9. AI Constraints

## C-AI01 — No AI in MVP

The MVP must not depend on AI functionality.

AI-based capabilities are future product possibilities rather than MVP requirements.

Potential future AI capabilities may include:

* Recommendations.
* Personalization.
* Artwork analysis.
* Metadata or description assistance.
* Customer assistance.
* Moderation assistance.
* Matching and discovery.
* AI-assisted creation.
* Other explicitly approved AI capabilities.

Listing these possibilities does not constitute approval to implement them.

---

## C-AI02 — AI Must Not Become an Unplanned Dependency

Future AI functionality must not be introduced into the MVP architecture simply to solve a problem that can be handled through ordinary application logic.

The dynamic artwork metadata mechanism must therefore remain rule-based within the MVP.

Future AI capabilities require explicit requirements, scope approval, and appropriate technical decisions.

---

# 10. Physical Artwork Constraints

## C-PH01 — No Managed Physical Transactions in MVP

The MVP must not manage physical artwork transactions as normal platform marketplace orders.

This includes avoiding MVP dependencies on:

* Physical shipment management.
* Delivery providers.
* Logistics tracking.
* Physical order fulfillment.
* Physical warehousing.

---

## C-PH02 — Portfolio Display Does Not Equal Marketplace Support

A physical artwork may be displayed as part of an Artist's portfolio if the approved product behavior permits it.

However, display capability must not be interpreted as support for:

* Platform-managed purchase.
* Platform-managed delivery.
* Platform-managed fulfillment.
* Platform commission on an external physical sale.

Physical artwork may therefore exist as a portfolio/display context without becoming an MVP-managed marketplace transaction.

---

## C-PH03 — Future Physical Support Must Be Deliberate

Future support for physical artwork transactions must be introduced through explicit requirements and architecture decisions.

The project must not prematurely build complete physical-commerce infrastructure into the MVP.

---

# 11. Delivery and Logistics Constraints

## C-D01 — Delivery Is Outside MVP

The MVP must not depend on integrated delivery or logistics services.

This includes:

* Delivery-provider APIs.
* Shipment tracking.
* Delivery status synchronization.
* Logistics management.
* Physical fulfillment workflows.

---

## C-D02 — Future Delivery Integration Must Remain Extensible

The system may be designed so that future delivery integration is possible, but the MVP should not implement unnecessary delivery infrastructure.

Future delivery services may be introduced when physical transactions or other approved product capabilities require them.

---

# 12. Printing Constraints

## C-PR01 — Printing Is Outside MVP

Printing-provider integration is outside the MVP.

The MVP must not depend on:

* Printing APIs.
* Print-order workflows.
* Automated print fulfillment.
* Print-provider shipping.

---

## C-PR02 — Future Printing Must Be Explicitly Introduced

Future printing capabilities may be considered when printed products or physical artwork services become an active project requirement.

Printing must not become an implicit MVP dependency.

---

# 13. Rights and Legal Constraints

## C-L01 — Platform Rules Must Respect Applicable Law

The project must not intentionally design workflows that contradict applicable legal requirements.

Legal requirements affecting the final commercial platform should be reviewed appropriately before public launch.

---

## C-L02 — Product Rules Are Not a Substitute for Legal Advice

Project documentation may define intended product behavior and rights rules, but it must not be treated as final legal advice or a legally sufficient contract by itself.

---

## C-L03 — Rights Must Be Considered Before Final Commercial Launch

Ownership, licensing, usage, intellectual-property, privacy, and marketplace responsibilities should receive appropriate legal review before the platform is operated as a public commercial service where such review is required.

---

# 14. Privacy Constraints

## C-PRV01 — Personal Data Must Be Minimized

The system should collect and retain only personal information that is necessary for approved functionality or legitimate operational requirements.

---

## C-PRV02 — Sensitive Data Requires Appropriate Protection

Information such as:

* Authentication data.
* Personal information.
* Bank-related information.
* Administrative records.
* Reports.
* Private transaction information.

must receive appropriate access controls and security protections.

---

## C-PRV03 — Data Access Must Follow Least Privilege

Users, Artists, administrators, and other system actors should only have access to information required for their authorized activities.

---

# 15. Security Constraints

## C-SE01 — Security Cannot Depend Only on the Client

Security-critical controls must be enforced on trusted backend infrastructure.

The frontend may improve user experience but must not be treated as the authoritative security boundary.

---

## C-SE02 — Authentication and Authorization Are Required

Protected platform functionality must use appropriate authentication and authorization mechanisms.

The exact implementation is defined during System Design and Cybersecurity.

---

## C-SE03 — Uploaded Content Is an Attack Surface

Artwork and other uploaded files must be treated as potentially unsafe input.

The system must account for appropriate:

* Validation.
* Sanitization where applicable.
* Storage isolation.
* Access control.
* Abuse prevention.

---

## C-SE04 — Security Must Continue Beyond Development

Security considerations must extend into:

* Testing.
* Deployment.
* Monitoring.
* Maintenance.
* Dependency updates.

---

# 16. Technical Architecture Constraints

## C-T01 — Backend Must Support Web and Mobile

The backend/API architecture should support both the Web application and the Mobile Application.

The Mobile Application must not require a completely separate business-logic backend merely because it uses a different client platform.

---

## C-T02 — Business Rules Should Be Centralized

Critical marketplace rules should be enforced consistently at the backend/domain level rather than duplicated independently across clients.

This is particularly important for:

* Artist permissions.
* Artwork publishing.
* Transaction states.
* Commission rules.
* User restrictions.
* Administrative actions.

---

## C-T03 — Database Integrity Must Be Preserved

The database must enforce appropriate integrity constraints where possible.

Application logic should not be the only protection against invalid relational data when the database can reliably enforce the rule.

---

## C-T04 — Architecture Should Avoid Premature Complexity

The project should not introduce infrastructure solely because it may become useful at a much larger scale in the future.

Future scalability should be considered, but MVP architecture should remain proportional to actual requirements.

---

# 17. Development Constraints

## C-DEV01 — Requirements Before Implementation

Major functionality should be based on approved requirements before implementation begins.

Implementation should not become the mechanism through which unresolved product decisions are accidentally made.

---

## C-DEV02 — Documentation Must Reflect Decisions

When a project-wide decision changes an important boundary, affected documentation must be updated.

Historical decisions should be preserved rather than silently rewritten.

---

## C-DEV03 — Phase Documents Must Avoid Temporal Status

Phase documentation must not contain temporary project-status information such as:

* Current phase.
* Progress percentage.
* Previous phase.
* Next phase.
* Completion status.

Project status belongs in appropriate root-level documents such as:

* `README.md`
* `ROADMAP.md`
* `CHANGELOG.md`

---

## C-DEV04 — Avoid Contradictory Duplicate Definitions

The same project-wide rule should not be independently defined in multiple documents in ways that can diverge.

A document may summarize or reference a rule defined elsewhere, but conflicting duplicate definitions should be avoided.

---

# 18. Project Lifecycle Constraints

## C-LC01 — Project Is Developed Incrementally

The complete project must be developed through defined phases rather than requiring all components to be completed simultaneously.

---

## C-LC02 — MVP Is a Milestone, Not the Complete Project

Completion of the MVP does not mean that the entire project is complete.

The complete project continues beyond the MVP through its defined core lifecycle, including:

* Mobile Application.
* Quality Assurance.
* Cybersecurity.
* Deployment.
* Maintenance.

---

## C-LC03 — Mobile Is a Core Project Phase

The Mobile Application is a core part of the complete project.

It is outside the MVP, but it must not be treated as an optional future feature that can simply be removed from the intended project lifecycle without an explicit scope decision.

---

## C-LC04 — Future Product Capabilities Are Separate From Core Project Phases

Future product capabilities must not be confused with the project's defined core development lifecycle.

Examples include:

* Platform-mediated payment.
* Expanded physical-artwork marketplace support.
* Printing services.
* Delivery and logistics integrations.
* AI-powered capabilities.
* Other advanced marketplace capabilities approved later.

These may extend the product after or alongside the core project, but they do not automatically become requirements of the current MVP or core phase sequence.

---

# 19. Operational Constraints

## C-O01 — External Services Must Be Justified

External services should only be introduced when they provide a clear benefit or are required by an approved capability.

---

## C-O02 — External Dependencies Must Be Replaceable Where Practical

The architecture should avoid unnecessary coupling to a single external provider where practical.

This is particularly relevant to future:

* Payment providers.
* Storage providers.
* Printing providers.
* Delivery providers.
* AI providers.
* Other infrastructure services.

---

## C-O03 — Deployment Must Consider Operational Security

A deployable system must account for:

* Environment configuration.
* Secret management.
* Access control.
* Database security.
* File storage security.
* Logging.
* Monitoring.
* Backup considerations.

Exact deployment requirements are defined during the Deployment and Cybersecurity phases.

---

# 20. Educational Project Constraints

## C-E01 — The Project Must Provide Practical Learning Value

The project is intended to provide practical software engineering experience across a realistic development lifecycle.

Technology choices should therefore provide meaningful learning value while remaining appropriate for the project.

---

## C-E02 — Learning Should Not Override Product Correctness

A technology should not be introduced solely for learning purposes if doing so creates unreasonable risk to:

* Security.
* Maintainability.
* Correctness.
* Project scope.
* Reliability.

Learning opportunities should be balanced against the needs of the actual project.

---

## C-E03 — Technology Choices Remain Explicit Decisions

The constraints document does not prescribe a final technology stack.

Technology choices should be documented through the appropriate architecture or technology decision process.

---

# 21. Constraint Priority

When constraints conflict, the project should generally consider them in the following order:

1. Legal and regulatory obligations.
2. Security and privacy.
3. Explicit project scope boundaries.
4. Core functional requirements.
5. Data integrity and reliability.
6. Maintainability.
7. Operational feasibility.
8. Performance and scalability requirements.
9. Learning and experimentation.

This priority is a planning principle rather than a replacement for case-specific engineering judgment.

---

# 22. Constraint Review

Constraints should be reviewed when:

* A major scope change is proposed.
* A new external integration is introduced.
* The architecture changes significantly.
* The project moves into a new major lifecycle stage.
* The MVP boundary changes.
* The project approaches public or commercial deployment.
* Legal or security requirements change.
* A previously future-only capability is formally approved for implementation.

A constraint should not remain in this document indefinitely if it is no longer valid.

When a constraint is removed or changed, affected requirements, decisions, architecture documents, and scope documentation should be reviewed.

---

# 23. Relationship to Other Foundation Documents

### Project Charter

Defines the overall project purpose, vision, lifecycle, and high-level boundaries.

### Project Scope

Defines what belongs to the MVP, complete project, and future product scope.

### Project Objectives

Defines what the project is intended to achieve.

### Assumptions

Records unresolved conditions temporarily treated as true.

### Decision Log

Records formal project-wide decisions.

### Requirements

Defines detailed system behavior and business rules.

### System Design

Defines the technical architecture and implementation direction.

Constraints should inform these documents without becoming a replacement for them.

---

# 24. Constraint Completion Criteria

The constraint definition is considered sufficiently established when:

* Major product boundaries are understood.
* MVP limitations are explicit.
* Payment limitations are explicit.
* Artist approval and publishing boundaries are explicit.
* Artwork and media limitations are explicit.
* Physical-artwork limitations are explicit.
* Delivery and printing limitations are explicit.
* AI limitations are explicit.
* Dynamic metadata is explicitly separated from AI functionality.
* Social feature boundaries are explicit.
* Security and privacy boundaries are identified.
* Technical architecture constraints are understood.
* Documentation constraints are established.
* Lifecycle constraints are clear.
* Mobile Application is correctly identified as a core project phase outside the MVP.
* Future product capabilities are distinguishable from the core project lifecycle.
* Future expansion is possible without requiring premature implementation.
* No major known constraint is hidden inside an assumption or undocumented decision.
