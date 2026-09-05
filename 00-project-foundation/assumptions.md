# Project Assumptions

## 1. Purpose

This document records the assumptions currently used as a foundation for the Art Marketplace Platform.

An assumption is a statement that is currently treated as true for planning or design purposes but has not yet been fully validated or formally decided.

Assumptions may be changed when new business, technical, legal, or user information becomes available.

When an assumption is validated, rejected, or converted into a formal decision, the relevant project documentation must be updated.

---

# 2. Product Assumptions

## A-001 — Marketplace Model

The platform is assumed to operate as a marketplace connecting customers with artists.

**Status:** Open

**Validation:** Business model validation.

---

## A-002 — Two Primary Marketplace Users

The platform is assumed to have two primary marketplace user types:

- Customer.
- Artist.

An administrator role is also assumed to be required for platform operations.

**Status:** Open

**Validation:** Requirements phase.

---

## A-003 — Customers Can Purchase Existing Artwork

The platform is assumed to support customers purchasing artwork that is already listed by an artist.

**Status:** Open

**Validation:** Requirements phase.

---

## A-004 — Customers Can Commission Custom Artwork

The platform is assumed to support custom artwork requests in which a customer provides requirements and an artist accepts the work.

**Status:** Open

**Validation:** Requirements phase.

---

## A-005 — Orders Are the Core Transaction Unit

The platform is assumed to represent marketplace transactions through an order entity.

An order will provide a structured record of the relationship between:

- Customer.
- Artist.
- Requested or purchased work.
- Requirements.
- Price.
- Delivery.
- Revisions.
- Approval.
- Payment information.

**Status:** Open

**Validation:** Requirements and Database Design.

---

# 3. Order Workflow Assumptions

## A-006 — Orders Have Defined States

Orders are assumed to progress through controlled states rather than being represented only by free-form text.

A preliminary workflow is:

```text
Requested
   ↓
Accepted
   ↓
In Progress
   ↓
Submitted for Review
   ↓
Revision Requested
   ↓
Resubmitted
   ↓
Approved
   ↓
Completed