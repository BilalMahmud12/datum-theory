# Datum Theory & Domain-Sovereign Architecture

**Author:** Bilal Mahmud  
**Year:** 2026  
**License:** CC BY 4.0

---

## What This Is

This repository contains two original works in software theory and architecture methodology.

**Datum Theory** is a software ontology proposing that every meaningful unit of software reality — a Datum — carries three concurrent dimensions of existence: semantic, presentational, and operational. These dimensions are not architectural choices. They are intrinsic to the nature of meaningful software units. Conventional layer-based architecture fragments them. The consequences are measurable: security vulnerabilities, inconsistent interfaces, purposeless processes, and drifting truth.

The theory is derived from observing the atom. An atom is not split across layers. Its identity, its presentational behavior, and its operational reality are three dimensions of one thing — whole, self-governing, expressing outward. Software should work the same way.

**Domain-Sovereign Architecture (DSA)** is the architectural governance doctrine derived from Datum Theory. It holds that the domain must be the highest authority over all three dimensions of every Datum in the system. The domain governs not only meaning and rules, but also the contracts of presentation, persistence, process, integration, and system evolution. Everything else — the API, the UI, the database, external integrations — serves that authority.

DSA is DDD extended from semantic modeling doctrine into full-dimensional governance doctrine.

---

## Documents

| Document | Description |
|----------|-------------|
| [`DATUM-THEORY.md`](./DATUM-THEORY.md) | The foundational ontology. What a Datum is. The three dimensions. The fragmentation claim. The four formal claims. |
| [`DATUM-THEORY-EXAMPLES.md`](./DATUM-THEORY-EXAMPLES.md) | Five worked examples from real business contexts showing how to identify Datums and their dimensions in practice. |
| [`DSA/DSA-v5.md`](./DSA/DSA-v5.md) | The complete DSA methodology. The argument, the foundation, the domain taxonomy, the delivery layers, scalability, economics, and implementation checklist. |

---

## The Reference Implementation

**datum-commerce** is the open source reference implementation of Domain-Sovereign Architecture — an enterprise-grade, multi-tenant e-commerce platform built in Java and Spring Boot according to DSA principles.

The domain layer is pure Java with zero Spring dependency. The Spring Boot infrastructure layer serves it. The domain governs. Infrastructure executes.

datum-commerce exists for the community. Read it. Fork it. Port it to your language. Challenge its domain decisions. Every port that preserves the same business rules in a different language is a proof of Datum Theory's portability claim.

*datum-commerce repository coming soon.*

---

## The Intellectual Stack

```
Datum Theory        ← ontology
      ↓
DSA                 ← governance doctrine
      ↓
datum-commerce      ← open source reference implementation
```

---

## License & Attribution

© 2026 Bilal Mahmud

Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).  
https://creativecommons.org/licenses/by/4.0/

You are free to share, implement, adapt, and build upon this work for any purpose, provided you give appropriate credit to the original author: **Bilal Mahmud**.
