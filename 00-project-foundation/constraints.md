# Project Constraints

## 1. Purpose

This document identifies the constraints that may restrict the design, development, deployment, operation, or future evolution of the Art Marketplace Platform.

Constraints may originate from:

- Business requirements.
- Technical limitations.
- Security requirements.
- Legal and regulatory considerations.
- Project scope.
- Resources.
- External dependencies.
- Operational requirements.

Constraints are different from assumptions.

An assumption represents something currently believed to be true, while a constraint represents a condition that limits the available options.

---

# 2. Scope Constraints

## C-001 — MVP Scope Must Remain Controlled

The initial release must remain limited to the approved MVP scope.

Additional functionality must not be added simply because it may be useful.

Any significant expansion must follow the defined scope-change process.

**Impact:** High

---

## C-002 — Core Marketplace Workflow Has Priority

Development must prioritize the core marketplace workflow over secondary features.

The primary workflow is:

```text
Discovery
   ↓
Request / Purchase
   ↓
Order
   ↓
Payment
   ↓
Production / Delivery
   ↓
Review
   ↓
Revision or Approval
   ↓
Completion