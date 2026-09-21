# Changelog



All notable changes to the Art Marketplace Platform project documentation, scope, architecture, and implementation are documented in this file.



The changelog records meaningful project-level changes. Detailed historical decisions are maintained in the root `decision-log.md`.



---



## \[Unreleased]



### Documentation



* Re-baselining the Project Foundation documentation.

* Aligning the project documentation with the current MVP scope.

* Clarifying the distinction between MVP scope and the complete project scope.

* Clarifying the role of the Mobile Application as a core project phase while remaining outside the MVP.

* Moving the project-wide Decision Log from `00-project-foundation/` to the repository root.

* Removing temporary project-status information from phase-specific documentation.

* Establishing clearer separation between project-wide concepts, requirements, technical design, and implementation details.

* Reviewing outdated payment, social, communication, artwork, and future-scope descriptions.



### Scope Clarifications



* MVP marketplace transactions focus on supported digital artwork.

* Platform-mediated payment integration is outside the MVP.

* Direct customer-to-artist bank transfer is the intended MVP payment model for applicable marketplace transactions.

* The platform commission model is based on a 15% commission on applicable marketplace transactions.

* Artist capabilities are granted through an approval process rather than being a separate account type.

* Like, Follow, 1–5 star Rating, customizable Notifications, Report, and Block are part of the MVP.

* User-to-user Chat is outside the MVP.

* User-to-AI Chat is outside the MVP.

* AI functionality is outside the MVP.

* Comments, Dislike, and Spam are not part of the approved social scope.

* Physical artwork is not supported as a platform-managed marketplace transaction in the MVP.

* Physical artwork may be displayed under the applicable MVP rules without becoming a platform-managed physical sale.

* Delivery and printing integrations are outside the MVP.

* Dynamic artwork metadata/question flows may be included in the MVP without requiring AI.

* Mobile Application development is outside the MVP but remains a core project phase and an important part of the project's final form and learning path.


---



## Changelog Conventions



### Categories



Changes may be grouped under:



* **Added** — New functionality, documentation, or project capability.

* **Changed** — Modification to existing behavior, scope, or documentation.

* **Deprecated** — Functionality or direction that is being phased out.

* **Removed** — Functionality or content explicitly removed from the project.

* **Fixed** — Correction of an identified problem.

* **Security** — Security-related changes.

* **Documentation** — Documentation-only changes.



### Scope of Entries



Changelog entries should describe meaningful changes rather than every individual edit.



Minor wording corrections do not normally require a changelog entry unless they materially affect project understanding.



### Relationship to Decision Log



The changelog records **what changed**.



The root `decision-log.md` records **important project decisions, their rationale, and their historical status**.



A major scope decision may therefore appear in both files:



* `CHANGELOG.md` records the resulting project change.

* `decision-log.md` records the decision and its reasoning.



---



## Versioning



The project is currently in active development and documentation refinement.



Version numbers should be introduced when a meaningful project milestone or release strategy has been established.



Until then, changes may be grouped under:



```text

[Unreleased]

```



A released version should contain the changes that were actually included in that release and should not be used as a substitute for the project's decision history.



