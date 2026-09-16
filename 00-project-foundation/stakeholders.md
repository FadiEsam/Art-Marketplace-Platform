# Stakeholders

## 1. Purpose

This document identifies the major stakeholders of the Art Marketplace Platform and describes their high-level relationship with the project.

Stakeholder identification provides a foundation for understanding:

* User needs.
* Responsibilities.
* Expectations.
* Business interests.
* Technical dependencies.
* Operational concerns.
* Potential project constraints.
* Future product considerations.

Detailed user roles, permissions, workflows, and stakeholder requirements will be defined during the Requirements Engineering phase.

---

# 2. Stakeholder Categories

The project's stakeholders are divided into the following high-level categories:

* Primary stakeholders.
* Administrative and governance stakeholders.
* Project and technical stakeholders.
* External service stakeholders.
* Future product stakeholders.

The presence of a stakeholder in this document does not automatically mean that the related capability is included in the MVP.

---

# 3. Primary Stakeholders

## 3.1 Customers

Customers are users who browse, discover, interact with, request, and potentially purchase supported artwork through the platform.

Their high-level interests include:

* Easy artwork discovery.
* Clear artwork information.
* Search and filtering.
* Reliable account management.
* Understandable marketplace workflows.
* Clear transaction status.
* Appropriate ownership and usage information.
* Reliable platform performance.
* Protection of personal information.
* Control over notifications and social interactions.
* Ability to request custom digital artwork.
* Ability to interact with approved Artists through supported platform features.

Customers are one of the primary target user groups of the platform.

---

## 3.2 Artists

Artists are users who use the platform to present and potentially sell supported artwork.

An Artist is an approved capability associated with a user account.

A user may continue to act as a Customer after becoming an Artist.

Their high-level interests include:

* Applying to become an Artist.
* Submitting five samples of their own work for review.
* Receiving a clear review decision.
* Maintaining an Artist profile.
* Presenting artwork professionally.
* Publishing eligible artwork.
* Managing artwork information and metadata.
* Managing artwork availability.
* Accepting custom artwork requests when available.
* Managing supported marketplace workflows.
* Receiving relevant transaction information.
* Understanding commission obligations.
* Protecting artwork, rights, and personal information.
* Reaching potential Customers.

Artists are one of the core stakeholder groups because the marketplace depends on the availability and presentation of artwork.

---

# 4. Administrative and Governance Stakeholders

## 4.1 Administrators

Administrators are responsible for managing and supervising the platform.

Their high-level interests include:

* Managing users.
* Managing Artist applications.
* Managing Artist status.
* Managing artwork.
* Managing artwork categories.
* Managing reports.
* Managing user restrictions.
* Managing blocked-user enforcement.
* Monitoring platform activity.
* Enforcing platform policies.
* Managing applicable commission-related restrictions.
* Maintaining platform integrity and security.
* Maintaining appropriate audit information.

The exact administrative responsibilities and permissions will be defined during the Requirements and System Design phases.

---

## 4.2 Specialist Artist Reviewers

Specialist Artist Reviewers are responsible for evaluating users who apply to become Artists.

Their high-level interests include:

* Reviewing submitted artwork samples.
* Evaluating whether submitted work belongs to the selected category.
* Confirming that the applicant meets the platform's Artist approval requirements.
* Providing an approval or rejection decision.
* Maintaining consistency in the review process.
* Preventing inappropriate or unauthorized artwork from entering the approved Artist marketplace.

The Artist application requires the applicant to submit five samples of their own work.

Detailed review criteria, rejection rules, resubmission rules, similarity checks, and reviewer permissions will be defined during Requirements.

---

## 4.3 Legal Consultant or Legal Advisor

A qualified legal consultant may become relevant before a future public or commercial launch.

Potential areas for review include:

* Artist rights.
* Customer rights.
* Artwork ownership.
* Usage and licensing rules.
* Marketplace terms.
* Payment-related responsibilities.
* Privacy requirements.
* Applicable legal obligations.
* Future physical-artwork transactions.
* Future platform-mediated payment.
* Other legally relevant marketplace policies.

Legal review is not treated as a substitute for product requirements.

It may be used to validate or revise the platform's intended rules before broader commercial operation.

---

# 5. Project and Technical Stakeholders

## 5.1 Project Owner / Developer

The Project Owner / Developer is responsible for:

* Defining project direction.
* Making project decisions.
* Defining and controlling scope.
* Designing the system.
* Implementing the system.
* Learning and applying software engineering practices.
* Maintaining project documentation.
* Evaluating technologies.
* Testing and validating the system.
* Managing repositories and development workflows.
* Deploying the application.
* Maintaining and evolving the system.

Because this is an educational project, the developer also acts as the primary learner throughout the software lifecycle.

---

## 5.2 Future Development Contributors

The project may eventually involve additional developers or contributors.

Their interests may include:

* Clear documentation.
* Understandable architecture.
* Maintainable code.
* Consistent development practices.
* Reproducible development environments.
* Clear contribution guidelines.
* Reliable testing.
* Clear API contracts.
* Understandable database design.
* Reliable deployment procedures.

The repository should therefore be structured so that another developer can understand and contribute to the project without relying entirely on undocumented project history.

---

## 5.3 QA and Testing Stakeholders

Quality assurance activities may involve developers, testers, or future contributors responsible for verifying the system.

Their interests include:

* Testable requirements.
* Clear acceptance criteria.
* Stable environments.
* Reproducible defects.
* Reliable test data.
* Functional correctness.
* Regression prevention.
* API and integration verification.
* Web application verification.
* Mobile application verification.

The exact QA roles and responsibilities will be defined during the Quality Assurance phase.

---

## 5.4 Security Stakeholders

Security activities may involve the project developer, security specialists, or other qualified contributors depending on the project's development needs.

Their interests include:

* Account security.
* Authentication.
* Authorization.
* Protection of sensitive information.
* Secure API behavior.
* Secure file and media handling.
* Protection against common application vulnerabilities.
* Secure deployment.
* Monitoring and incident handling.
* Protection of future payment-related functionality if introduced.
* Protection of future AI-related functionality if introduced.

Detailed security responsibilities will be defined during the Cybersecurity phase.

---

## 5.5 Mobile Application Stakeholders

The Mobile Application is part of the complete core project, although it is outside the initial MVP.

Relevant stakeholders include:

* Customers using the Mobile Application.
* Artists using the Mobile Application.
* Mobile developers.
* Backend/API developers.
* QA and testing stakeholders.
* Security stakeholders.
* Project Owner / Developer.

Their high-level interests include:

* Consistent functionality with the approved product rules.
* Reliable API integration.
* Appropriate mobile UX.
* Secure authentication.
* Secure data handling.
* Reliable notifications.
* Consistent account and marketplace behavior.
* Appropriate mobile performance.

Detailed Mobile Application requirements will be defined during the Mobile Application phase.

---

# 6. External Service Stakeholders

The platform may interact with external service providers when their services are required by approved project requirements.

Potential examples include:

* Email service providers.
* Cloud or object storage providers.
* Hosting and infrastructure providers.
* Monitoring services.
* Authentication or identity services.
* Payment providers.
* Printing providers.
* Delivery or logistics providers.
* Future AI service providers.

The presence of an external provider in this document does **not** automatically make that provider an MVP dependency.

---

## 6.1 MVP / Core Infrastructure Providers

External services may be required for infrastructure or supporting functionality, such as:

* Hosting.
* Storage.
* Email.
* Monitoring.
* Other approved infrastructure services.

Their inclusion depends on the technical requirements established during the relevant project phases.

---

## 6.2 Future Payment Providers

Payment service providers are relevant to a possible future platform-mediated payment model.

They are **not required as marketplace payment providers for the MVP**, because the MVP uses direct Customer-to-Artist bank transfer.

If platform-mediated payment is introduced in the future, payment providers become active project stakeholders and dependencies according to the approved requirements.

---

## 6.3 Future Printing Providers

Printing providers may become stakeholders if the platform later introduces:

* Printing.
* Print-on-demand.
* Printed versions of digital artwork.
* Print-order management.

Printing providers are outside the MVP marketplace transaction model.

---

## 6.4 Future Delivery and Logistics Providers

Delivery and logistics providers may become stakeholders if the platform later introduces:

* Physical-artwork delivery.
* Printing-to-customer delivery.
* Shipment creation.
* Shipment tracking.
* Other logistics services.

Delivery and logistics integration is outside the MVP.

---

# 7. Future Product Stakeholders

Some stakeholder groups may become relevant when future product capabilities are introduced.

Examples include:

* Customers participating in future physical-artwork transactions.
* Artists participating in future physical-artwork marketplace capabilities.
* Printing service providers.
* Delivery and logistics providers.
* Payment service providers.
* Additional mobile application users.
* AI service providers.
* AI-related specialists.
* Other future marketplace service providers.

These stakeholders should be evaluated when the corresponding capability becomes an approved project requirement.

---

# 8. AI-Related Stakeholders

AI functionality is currently outside the MVP.

If AI capabilities are introduced in future product development, potential stakeholders may include:

* Customers using AI-assisted features.
* Artists whose artwork is processed by AI-related functionality.
* Administrators responsible for monitoring AI features.
* Developers implementing AI functionality.
* Data or machine-learning specialists.
* AI service or infrastructure providers.
* Security stakeholders.
* Legal stakeholders where AI-related legal issues are relevant.

Potential future AI capabilities may include:

* Recommendations.
* Personalization.
* Artist/customer matching.
* Artwork analysis.
* AI-assisted metadata.
* AI-generated descriptions.
* AI-assisted moderation.
* AI customer assistance.
* AI chat.
* AI-assisted artwork creation.

These capabilities are future possibilities and are not MVP requirements.

AI-related stakeholder requirements should be formally evaluated only when the corresponding AI functionality becomes an approved project scope.

---

# 9. Stakeholder Interests

| Stakeholder                     | Primary Interest                                                                           | Influence |
| ------------------------------- | ------------------------------------------------------------------------------------------ | --------- |
| Customers                       | Discover, request, and interact with supported artwork through clear marketplace workflows | High      |
| Artists                         | Establish a professional presence and participate in supported marketplace workflows       | High      |
| Administrators                  | Manage and supervise the platform                                                          | High      |
| Specialist Artist Reviewers     | Evaluate Artist applications consistently                                                  | High      |
| Project Owner / Developer       | Build, learn, maintain, and evolve the system                                              | Very High |
| Future Contributors             | Understand and extend the system                                                           | Medium    |
| QA / Testing Stakeholders       | Verify system correctness and quality                                                      | Medium    |
| Security Stakeholders           | Protect the system, users, and data                                                        | High      |
| Mobile Application Stakeholders | Deliver and maintain the Mobile Application experience                                     | High      |
| Legal Consultant / Advisor      | Review applicable rights and legal requirements                                            | Medium    |
| Infrastructure Providers        | Provide required infrastructure services                                                   | Medium    |
| Future Payment Providers        | Support future platform-mediated payment                                                   | Future    |
| Future Printing Providers       | Support future printing capabilities                                                       | Future    |
| Future Delivery Providers       | Support future physical-artwork logistics                                                  | Future    |
| Future AI Stakeholders          | Use, manage, develop, or provide future AI capabilities                                    | Future    |

Influence describes the stakeholder's potential influence on project decisions or operation. It is not a ranking of importance or value.

---

# 10. Stakeholder Management Principles

The project will follow these principles when dealing with stakeholder needs:

1. Stakeholder needs should be understood before defining detailed requirements.
2. Stakeholder expectations should not automatically become system requirements.
3. Conflicting stakeholder needs should be identified and evaluated.
4. Requirements should provide meaningful value to relevant stakeholders.
5. Technical decisions should support validated project needs.
6. Security and privacy concerns should be considered when stakeholder needs involve sensitive data.
7. Scope should remain controlled when stakeholder requests introduce unnecessary complexity.
8. Future stakeholder needs should not unnecessarily increase the initial MVP scope.
9. External service dependencies should only be introduced when the corresponding capability is approved.
10. Stakeholder needs should be translated into explicit requirements before implementation.
11. Future product stakeholders should not be treated as active MVP dependencies unless their capability is formally approved.
12. Stakeholder changes should be reflected in project documentation when they materially affect project scope or responsibilities.

---

# 11. Stakeholder Validation

Stakeholders and their needs will be reviewed during the Requirements Engineering phase.

During that phase, the project will determine:

* Detailed stakeholder goals.
* Stakeholder responsibilities.
* User roles.
* User permissions.
* User journeys.
* Stakeholder requirements.
* Conflicting needs.
* Business rules related to stakeholders.
* Privacy and security considerations.
* External dependency requirements.
* Mobile-specific stakeholder requirements.
* Future stakeholder considerations where relevant.

The stakeholder model may evolve as the project requirements become better understood.

Changes to the stakeholder model should not automatically change project scope.

Any significant scope change should follow the project's documented scope and decision-management process.

---

# 12. Relationship Between Stakeholders and Requirements

Stakeholders provide needs, expectations, constraints, or responsibilities that may contribute to requirements.

However:

> A stakeholder request is not automatically a project requirement.

Before implementation, a proposed stakeholder need should be evaluated against:

* Project objectives.
* Approved scope.
* User value.
* Technical feasibility.
* Security.
* Privacy.
* Maintainability.
* Project complexity.
* MVP boundaries.
* Future product boundaries.

Approved requirements should then be documented in the appropriate Requirements documentation.

---

# 13. Stakeholder Coverage

The project should ensure that the major perspectives required to operate and evolve the platform are represented.

At a minimum, the project foundation should account for:

* Customer needs.
* Artist needs.
* Artist review needs.
* Administrative needs.
* Development needs.
* Web application needs.
* Mobile application needs.
* Quality assurance needs.
* Security needs.
* Legal considerations.
* Infrastructure dependencies.
* Future payment dependencies.
* Future printing dependencies.
* Future delivery dependencies.
* Future AI considerations.
* Future product expansion needs.

This does not require every stakeholder group to participate directly in every development phase.

The level of stakeholder involvement should correspond to the capabilities being designed or implemented.

---

# 14. Stakeholder Scope Boundary

The stakeholder model must remain aligned with the project scope.

In particular:

* Customers and Artists are primary MVP stakeholders.
* Administrators and Specialist Artist Reviewers are required for MVP governance and Artist approval.
* Project and technical stakeholders support the complete project lifecycle.
* Mobile stakeholders become directly relevant to Phase 07 and later Mobile development.
* Payment providers are future stakeholders for platform-mediated payment.
* Printing providers are future stakeholders for printing capabilities.
* Delivery providers are future stakeholders for physical-artwork logistics.
* AI-related stakeholders are future stakeholders unless AI functionality is formally introduced into the project.

The existence of a stakeholder does not by itself authorize the implementation of the associated capability.
