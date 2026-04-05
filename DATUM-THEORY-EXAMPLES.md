# Datum Theory in Practice: Five Worked Examples

*A companion to Datum Theory: A Chemist's Model for Software Ontology*

**Author:** Bilal Mahmud  
**Year:** 2026  
**License:** CC BY 4.0 — Creative Commons Attribution 4.0 International  
https://creativecommons.org/licenses/by/4.0/

---

## Introduction

Datum Theory proposes that every meaningful unit of software reality carries three concurrent dimensions of existence: semantic, presentational, and operational. But theory without grounding risks becoming abstraction without application.

This companion piece works through five concrete examples drawn from real business contexts. Each example is chosen to reveal a different aspect of Datum Theory — including its most important practical clarification:

**The same data value can be a Datum in one business context and a Datum attribute in another.**

The Datum is not defined by the data type it carries. It is defined by the business context it exists in. Understanding this distinction is the key to applying Datum Theory correctly.

---

## Example 1 — The Phone Number

### Two Contexts. Two Different Answers.

The phone number is the most instructive example in Datum Theory precisely because the answer changes completely depending on context.

**Context A: The DMC agency record.**

A Destination Management Company maintains records of the overseas agencies it works with. Each agency record contains a name, a country, a credit limit, payment terms, a contact person — and a phone number.

In this context, the phone number is not a Datum. It is an attribute of the Agency Datum. On its own, the phone number means nothing. It has no independent business identity. It cannot be confirmed, assigned, contacted, or closed. It does not participate in any process independently of the agency it belongs to. It is simply one of several properties that together constitute the Agency Datum.

Below the Agency Datum, you find attributes — name, phone number, credit limit. These are not Datums. They are the components of one.

**Context B: The contact form callback.**

A business operates a website. Visitors submit a phone number requesting a callback. The submitted phone number stands alone. It is the entire meaningful unit — not an attribute of something larger.

In this context, the phone number is a full Datum.

**Semantic dimension:** This phone number is a callback request. It has identity — a specific person at a specific number waiting to be contacted. It has an invariant — it must be a valid, dialable phone number. It has states — new, assigned, contacted, closed. It has a transition — from new to contacted, it must be assigned to a sales person first.

**Presentational dimension:** In the admin panel where callback requests are managed, who sees this phone number? The sales team sees it. The accountant does not. The operations manager sees it but cannot edit it. These are not developer decisions. They are business rules governing who may access this meaningful unit — and they belong to the Datum, not to the screen that renders it.

**Operational dimension:** When the phone number arrives — log it, create an assignment queue entry. When assigned — notify the assigned sales person. When contacted — record the outcome. When closed — archive it, update reporting. The phone number's lifecycle produces consequences at every stage.

**The lesson:**

The data is identical — a string of digits. The business context is different — and that difference determines everything.

This is the most important practical rule of Datum Theory: **before classifying something as a Datum, ask what business context it exists in.** The same value, in a different context, may be a Datum attribute rather than a Datum itself.

---

## Example 2 — The Commission Rate

### The Configuration Question

The commission rate is a Datum — but what kind of Datum depends on a question that must be answered before any code is written:

**Can it have a variety of values, or just one?**

This is not a technical question. It is a business question. And the answer determines the entire structure of the Datum.

**Case A: One commission rate for the whole system.**

If the business charges a single commission rate applied uniformly — say, 15% on all transactions — then the commission rate is a **configuration Datum**.

It exists at the system level. It has one value. It belongs to the system's operational configuration, not to any individual entity.

**Semantic dimension:** This commission rate is the system's standard margin. Its invariant: must be between 0 and 100. Its state: current value. Its identity: the system's pricing rule.

**Presentational dimension:** Only the super administrator sees and edits it. No other role has access. The visibility is strict and unambiguous.

**Operational dimension:** When changed, it affects all future calculations that reference it. Existing transactions are not retroactively affected — they captured the rate at the time of booking as a price snapshot. Changing it is a significant operational event that should be logged.

This is a Datum — small, singular, governed — but a Datum nonetheless.

**Case B: Commission rate varies by agency relationship.**

If the business charges Agency A 15%, Agency B 12%, and Agency C 18% depending on the relationship and volume — then the commission rate is an **attribute of the relationship Datum** between the DMC and each agency.

It lives on the agency record or on a contract record. It is one of the properties that define the commercial relationship. It is not a standalone Datum — it is part of the Agency or Contract Datum's semantic core.

**The lesson:**

Never assume the structure of a Datum before answering the business questions that define it. The commission rate example reveals that the same concept can be a configuration Datum in one business model and a relationship attribute in another.

**This is why Datum Theory begins with business conversations, not with code.** The structure of a Datum is determined by the business, not by the developer.

---

## Example 3 — The Reservation

### The Core Transaction Datum

The reservation is the clearest example of a full, rich Datum in the Destination Management Company context. It is the heart of the business — the unit around which everything else orbits.

**Semantic dimension:**

A reservation has identity — a unique reference number (e.g., RES-2026-1042) that identifies it unambiguously throughout its entire lifecycle and beyond. It cannot be broken into smaller units without losing what it is. A reservation broken into its components — hotel nights, tours, transfers — loses the identity of the grouped commitment. The whole is the meaningful unit.

Its invariants: it cannot be confirmed without at least one line item and at least one passenger. A reservation without guests is not a reservation. A reservation without a service is not a reservation. These are not database constraints — they are business rules that belong to the Datum.

Its states: draft → confirmed → cancelled. Each state has meaning. A draft reservation carries no financial commitment. A confirmed reservation has triggered a price snapshot and an allotment deduction. A cancelled reservation carries its own consequences depending on when the cancellation occurred relative to the service dates.

Its relationships: it belongs to an agency, it references a branch, it contains line items that reference hotels and services, it contains passengers.

**Presentational dimension:**

The same reservation appears differently to different actors.

An agent sees the sell price — what the agency will be charged. An agent does not see the cost price — what Siwan Travel paid the supplier.

An accountant sees both sell price and cost price, and therefore sees the margin. An accountant cannot edit the reservation itself.

A branch manager sees all reservations within their branch. A client administrator sees all reservations across all branches.

A viewer sees the reservation as read-only, with limited financial visibility.

These are not screen design decisions. These are business rules. They belong to the Reservation Datum. The frontend renders what the Datum governs.

**Operational dimension:**

When a reservation is confirmed:
- The price is snapshotted on each line item — the sell price and cost price at the moment of confirmation, never to be affected by future rate changes
- The allotment is decremented — available inventory for the contracted hotel rooms is reduced
- An accounting entry is created — the receivable from the agency is recorded
- An email notification is sent to the agency confirming the booking
- The reservation event is recorded — `ReservationConfirmed` becomes part of the system's history

When a reservation is cancelled:
- Allotment may be released depending on release rules
- Cancellation penalties may apply depending on timing
- The accounting entry is reversed or adjusted
- Notification is sent

Every one of these consequences is intrinsic to the Reservation Datum. They are not external processes that happen to touch the reservation. They are the reservation asserting its own operational reality.

**The lesson:**

The reservation demonstrates that a rich Datum is not complicated because of its technical implementation. It is rich because the business is rich. Every rule in the reservation's three dimensions corresponds to something real that happens in a travel agency every day.

---

## Example 4 — The Hotel Type

### The Reference Datum

Hotel type — City Hotel, Resort, Boutique, Apart-Hotel, Heritage — is a Datum of a fundamentally different kind from the reservation. It is a **reference Datum**: a unit that classifies and gives vocabulary to other Datums without being a primary business transaction itself.

Reference Datums are often underestimated. They are treated as simple lookup tables — just a list of strings. But under Datum Theory, they carry all three dimensions.

**Semantic dimension:**

A hotel type has identity — City Hotel is not the same as Resort, and the distinction matters to the business. A client choosing hotels for a beach holiday filters by Resort. A client arranging a business trip filters by City Hotel. The classification affects search, recommendation, and reporting.

Its invariant: once a hotel is classified as a City Hotel, that classification should not be changed casually — it may affect historical reports and client expectations.

In the DMC context, hotel type is a **global reference Datum** — it has no `client_id`. It is shared across all tenants. The super administrator manages the vocabulary. Client users read it. This is a deliberate business decision: the meaning of "City Hotel" should be consistent across all agencies using the system.

**Presentational dimension:**

In the admin interface, the super administrator sees hotel types with full edit capability — create, rename, activate, deactivate.

A client administrator sees hotel types as a read-only reference when categorizing their hotels.

An agent sees hotel types as a filter option when searching for hotels for a reservation.

A viewer sees hotel type as a label on the hotel record.

Four roles. Four different presentations. All governed by the Datum.

**Operational dimension:**

When a hotel type is deactivated — it should no longer appear in new hotel creation forms, but existing hotels classified under it retain their classification for historical integrity.

When used as a search filter — hotel type participates in the search query that retrieves hotels matching a client's requirements.

When used in reporting — hotel type is a dimension across which reservation volume, revenue, and occupancy can be analyzed.

**The lesson:**

Reference Datums are not trivial. They are the vocabulary layer of the business — the controlled language through which other Datums are classified and compared. When reference Datums are treated as mere lookup tables with no governed dimensions, the result is inconsistent classification, broken filters, and meaningless reports.

The hotel type example also introduces the concept of **scope**: some Datums are global (shared across all tenants, governed by the platform). Others are per-client (owned by each tenant, governed by the client). The scope is determined by who has authority over the Datum's meaning — and that is always a business decision.

---

## Example 5 — The User Role Assignment

### An Operational Interface, Not a Standalone Datum

The user role assignment is the most structurally interesting example because the answer to "is this a Datum?" is: **no — but understanding why not deepens the theory.**

In the DMC system, a user can be assigned a role — Agent, Accountant, Senior Agent, Branch Manager — within a specific branch or across all branches. The assignment record stores: which user, which role, which branch (or no branch for global assignments).

The temptation is to treat `UserRoleAssignment` as a standalone Datum. It has a table. It has fields. It participates in queries. But under Datum Theory, it fails the defining criterion: it does not have irreducible business identity of its own.

A user role assignment, on its own, means nothing independently. It only has meaning as part of the User Datum's operational reality — as an expression of what the User can do in the system.

**The UserRoleAssignment is the operational dimension of the User Datum expressing itself.**

Specifically: it is the part of the User's operational life that governs how the User participates in processes, accesses other Datums, and exercises behavioral boundaries in the system.

When a user is assigned the Agent role for the Cairo branch:
- The User Datum's operational dimension is updated
- The user's access to reservations within that branch is now governed
- The user's visibility of financial data is now governed
- The user's ability to confirm reservations (or not) is now determined

These consequences belong to the User Datum. They are expressions of the User's operational reality. The assignment record is the mechanism — not the meaning.

**What this teaches about Datum composition:**

This example demonstrates a critical structural principle: **a Datum's operational dimension can be complex enough to require its own data structures — without those structures becoming standalone Datums.**

The `UserRoleAssignment` table in the database is real. The record is real. But the business identity belongs to the User, not to the assignment. The assignment is infrastructure serving the User Datum's operational expression.

This is precisely analogous to the atom: an electron orbital is real, it has mathematical structure, it participates in physical processes — but it is not a standalone atom. It is the atom's operational reality expressing itself in a particular way.

**The lesson:**

Not every table, not every record, not every data structure is a Datum. Some are expressions of a Datum's operational dimension. Recognizing this prevents over-classification — the mistake of treating every database table as if it carries independent business identity.

The test remains: does this carry irreducible business meaning of its own? The user role assignment does not. The User does.

---

## Summary: A Natural Taxonomy

These five examples reveal that Datums are not all of the same kind. A natural taxonomy emerges from examining them in their business context:

| Type | Example | Characteristic |
|------|---------|----------------|
| **Contextual attribute** | Phone number in an agency record | Attribute of another Datum — not a Datum itself |
| **Standalone Datum** | Phone number in a contact form | Independent business identity with all three dimensions |
| **Configuration Datum** | Commission rate (if system-wide) | System-level meaningful unit, single value, governed scope |
| **Relationship attribute** | Commission rate (if per-agency) | Attribute of the contract or agency Datum |
| **Core transaction Datum** | Reservation | Full three-dimensional Datum, heart of the business |
| **Reference Datum** | Hotel type | Classifies other Datums, controlled vocabulary, scoped globally or per-client |
| **Operational expression** | User role assignment | Serves the operational dimension of another Datum |

This taxonomy is not exhaustive. Different domains will reveal additional types. But the principle underlying all of them is consistent:

**The Datum is defined by irreducible business meaning in context — not by the data type it carries, not by whether it has a database table, and not by how many fields it contains.**

---

## The Most Important Practical Rule

Before writing any code, before designing any database table, before building any API endpoint — ask:

**What is the Datum here? What business context gives it meaning? And what are its three dimensions?**

If the unit has irreducible business meaning in this context — it is a Datum. Govern all three of its dimensions: define its semantic truth, define who sees it and how, define its operational consequences.

If the unit only has meaning as part of something else — it is an attribute of a Datum. Let the containing Datum govern it.

If it is technical infrastructure — a cache layer, an index, a deployment script — it serves the expression of Datums but is not itself one.

The phone number in a contact form. The reservation in a DMC. The hotel type in a travel system. The user's access rights in a multi-tenant platform.

These are Datums. They were always Datums. They carried all three dimensions before anyone thought to ask the question.

Datum Theory simply names what was always there — and asks that software be built to honor it.

---

*© 2026 Bilal Mahmud*

*Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0)*  
*https://creativecommons.org/licenses/by/4.0/*

*You are free to share, implement, adapt, and build upon this work for any purpose, provided you give appropriate credit to the original author: Bilal Mahmud.*

---

*This document is a companion to:*  
*Datum Theory: A Chemist's Model for Software Ontology*  
*Domain-Sovereign Architecture (DSA) — the architectural implementation of Datum Theory*  
*TurXpert — the reference implementation of DSA*
