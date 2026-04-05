# Datum Theory: A Chemist's Model for Software Ontology
## Editorial Refinement Draft with Flags

*On the Atomic Nature of Meaningful Software Units and How Observing the Atom Revealed Their Three Dimensions of Existence*

**Author:** Bilal Mahmud  
**Year:** 2026  
**Version:** 3.0 — Editorial Refinement Draft  
**License:** CC BY 4.0 — Creative Commons Attribution 4.0 International  
**Attribution:** You are free to share, implement, adapt, and build upon this work for any purpose, provided you give appropriate credit to the original author: Bilal Mahmud.  
https://creativecommons.org/licenses/by/4.0/

---

## Preface

In 2019 I had a vision.

Not a vision driven by frustration with existing software architectures. Not a reaction to a problem I was trying to solve. A genuine vision — unprovoked, unsolicited, arriving whole.

I saw what I called the Atomic Ocean: an abstract space in which software exists not as files, frameworks, or layers, but as atomic meaningful units floating in an enormous combinational space. Like atoms in an ocean. Tiny. Self-contained. Infinite in their combinations.

At the time, I could not fully articulate what I had seen. But the image remained. So did the question it planted. Over years of building real systems, observing real problems, and watching software fragment in ways that felt not merely inconvenient but structurally wrong, that question kept growing.

When the answer finally crystallized, it did not come from a software book or an architectural pattern. It came from chemistry.

It came from the atom.

---

## 1. The Problem with Software's Distributed Truth

All software carries a burden of coordinated truth.

A system must determine what a thing is, how it may be acted upon, how it appears to different participants, how it changes state, how it is remembered, how it is retrieved, and how it interacts with the rest of the world. This is not optional. Every system must answer these questions.

The question is not whether these dimensions of truth exist. They always do. The question is where they live — and who is responsible for keeping them consistent.

In conventional software architecture, that truth is fragmented. A field exists in one dimension at a time. In the database, it exists as a column. In the API layer, it exists as a JSON key. In the frontend, it exists as an input element or a display string. In the permission system, it exists as a conditional check — often written by a developer making a judgment call, alone, at the moment of implementation, with no governing authority behind that decision.

Never whole. Always projected. Always split.

The consequences are not merely technical inconvenience. They are structural failures with real business cost.

- **Security vulnerabilities** — data exposed to the wrong actors because who may see what was decided ad hoc by a developer rather than governed by the meaningful unit itself
- **Inconsistent interfaces** — the same field visible on one screen and hidden on another for reasons nobody can trace back to a written rule
- **Processes with no consequence** — operations that execute without triggering the business behaviors they were supposed to trigger because the operational life of a unit was scattered across disconnected handlers
- **Drifting truth** — rules changed in one layer and forgotten in another, producing a system whose actual behavior no longer matches any single authoritative description

These are not bugs in the conventional sense. They are the structural result of treating meaningful software units as if their dimensions could be safely managed in separate places by separate people operating under separate assumptions.

Datum Theory proposes a different starting point.

---

## 2. The Atom as the Original Observation

A carbon atom does not exist in layers.

It does not have a database layer where its atomic number is stored, a separate API layer where its bonding behavior is exposed, and a frontend layer where its visual representation is rendered. It exists as one thing — whole, self-contained, simultaneously expressing all of its properties in all of their dimensions.

The atom has identity. Carbon is always carbon. Its atomic number — 6 — is invariant. You cannot change what it is without it becoming something else entirely. This is not a rule imposed on the atom from outside. It is intrinsic. It belongs to the atom.

The atom has a presentational reality. Under spectroscopy, it emits specific light frequencies. In a molecular bond, it presents certain electrons to neighboring atoms. In different chemical contexts, it appears differently — but always as carbon, always governed by the same underlying truth. The presentation varies. The identity does not.

The atom has an operational reality. It bonds. It ionizes. It reacts. It participates in processes. It carries energy states. It responds to electromagnetic fields. Its operational behavior is not separate from what it is; it is an expression of what it is. The same carbon atom defined by atomic number 6 is also the carbon atom that forms four covalent bonds, becomes the backbone of organic chemistry, and burns in oxygen to produce carbon dioxide.

What struck me — and what planted the seed of Datum Theory — was this:

**The atom is never split across layers. It is always whole. Its identity, its presentation, and its operational behavior are not three separate things. They are three dimensions of one thing.**

And I asked: why is software not built this way?

The atom analogy is the inspiration for the ontological insight, not a literal claim that software units are physical atoms in every respect. The atom motivates the core observation — that a meaningful unit has concurrent dimensions of existence — and nothing more is claimed of it than that.

---

## 3. The Datum

A Datum is the least atomic unit of meaningful software existence.

It is not a field. It is not a database row. It is not a component. It is not a class in the conventional sense.

A Datum is the smallest unit of software reality that still retains its own identity within the business domain. Below the Datum, you find raw data — bits, bytes, strings, integers — real, but no longer carrying business meaning. A phone number decomposed into its digits is no longer a phone number. It is a sequence of numbers. A hotel type decomposed into its label string is no longer a hotel type. It is text.

The Datum is where meaning lives. And because meaning lives there, the Datum simultaneously carries:

- what it is
- how it appears
- how it lives and reacts within the system

These are not three separate concerns to be assigned to three separate layers. They are three dimensions of a single meaningful unit — exactly as the atom's identity, presentation, and operational behavior are three dimensions of one physical reality.

The phone number is the clearest illustration.

A phone number is not simply a string of digits stored in a column. A phone number has a life that spans dimensions. It lives somewhere — it must be stored, and the question of how it is stored, how it is identified, and what format it persists in is part of what the phone number is. It appears differently to different actors — a customer service agent sees it and can edit it, a viewer sees it as plain text, a marketing system includes it in a contact block, a security system may hide it entirely. It reacts — it can be dialed, it can trigger a notification, it can participate in a verification workflow. And when it fails to validate — when a submitted phone number does not conform to the rules of what a phone number is — that failure is not external to the Datum. It is the Datum asserting its own invariants. The validation error is the Datum speaking.

These dimensions were not designed into the phone number by any architect. They were already there. I observed them. Once observed, the question became unavoidable: why does software pretend they can be managed separately?

A Datum is the unit that keeps them together.

---

## 4. The Three Dimensions of a Datum

Every Datum exists in three dimensions simultaneously. These dimensions are not layers. They are not phases of a pipeline. They are concurrent aspects of a single meaningful unit — just as mass, charge, and spin are concurrent properties of a subatomic particle.

### 4.1 The Semantic Dimension — What It Is

The semantic dimension is the identity and meaning of the Datum. It answers the question: what is this thing?

It includes:

- **Identity** — what makes this Datum uniquely itself; the smallest expression that still carries the meaning of the whole
- **Invariants** — what is always true about it; what cannot change without the Datum becoming something else entirely
- **Allowable states** — the valid configurations the Datum can occupy
- **Transitions** — how it moves from one valid state to another, and what governs those movements
- **Relationships** — how it relates to other Datums; how Datums combine into larger meaningful structures
- **Domain truth** — the business meaning it carries; the reason it exists in the system at all
- **Validation** — the rules the Datum asserts about its own correctness; validation failures are expressions of the semantic dimension, not external judgments imposed upon it

This comes closest to what domain-driven design tried to protect with entities and value objects. But Datum Theory extends beyond that protection. The semantic dimension does not merely say: model the domain correctly. It says: the semantic core must be authoritative. It must govern the other dimensions, not merely coexist with them.

### 4.2 The Presentational Dimension — How It Appears

The presentational dimension is the governed visible and interactive form of the Datum. It answers the question: how does this thing appear to those who encounter it?

This dimension is not decoration. It is not a UI concern delegated to frontend developers. It is part of the legitimate reality of the Datum, and it must be governed by the Datum itself rather than decided ad hoc at the point of rendering.

A phone number may appear:

- as plain text to a viewer
- as an editable input to an administrator
- as hidden entirely from an auditor
- as a formatted contact string in a marketing context
- as a masked value in a security context

The meaning remains linked to the same underlying Datum. The presentation varies. But the rules governing which presentation appears to which actor are not arbitrary decisions made by the developer who happened to write that screen. They are expressions of business truth. Who may see what is a semantic question wearing a presentational face.

When this dimension is not governed by the Datum — when the developer decides — the result is inconsistent interfaces, unauthorized data exposure, and rules that exist nowhere except in the memory of the person who wrote them. These are not edge cases. They are among the most common failure modes in production software.

The presentational dimension includes:

- **Field visibility** — which actors may see this Datum and under what conditions
- **Editability** — which actors may change this Datum and under what conditions
- **Form** — how it is structured for input, and what type of interaction it supports
- **Representation** — how it is displayed for viewing, and what format it takes in different contexts
- **Context-sensitivity** — how its appearance adapts to different roles, states, and situations

In a properly governed system, these are not decided in the frontend. They are defined in the Datum itself and served to any consumer that asks — whether that consumer is a web interface, a mobile application, an API response, or a printed document.

### 4.3 The Operational Dimension — How It Lives and Reacts

The operational dimension is the active life of the Datum within the system. It answers the question: what does this thing do, and what happens when it is acted upon?

A system exists to do things. If nothing meaningful happens when a Datum changes state — if an operation produces no consequence worth tracking, no event worth recording, no process worth triggering — then the question must be asked: what is the purpose of that operation? What is the purpose of that system?

A system in which processes happen with no meaning, operations produce no tracked consequence, and state changes propagate nowhere has lost its purpose. The operational dimension is what gives software its reason to exist beyond mere data storage.

This dimension encompasses those behaviors intrinsic to the Datum itself — the behaviors that express what the Datum is through what it does. It is distinct from system-level orchestration between Datums. A reservation's confirmation — the price being snapshotted, the allotment being decremented, the event being recorded — belongs to the reservation's operational dimension. The downstream process that generates an invoice after confirmation is system-level orchestration between the Reservation Datum and the Invoice Datum. The line between intrinsic operational behavior and external orchestration is the boundary of the Datum.

The operational dimension includes:

- **Persistence** — where and how the Datum is stored; how it is identified for retrieval and update; the storage shape is defined by the Datum, not by the infrastructure that stores it
- **Participation in processes** — how the Datum is involved in use cases, workflows, and business operations that belong to its own lifecycle
- **Reactions** — what the Datum does or triggers when it changes state; what consequences are intrinsic to its own behavior
- **Events** — what the Datum records as evidence of its own history; domain events are the Datum's memory of its own significant moments
- **Search and retrieval** — how the Datum participates in queries, federation, and discovery, including how it governs the admission of external data into its meaning
- **Validation responses** — how the Datum asserts its invariants and communicates failures; validation errors are part of the operational reality of the Datum, not external judgments

---

## 5. The Fragmentation Claim

Conventional software architecture does not think in Datums.

It thinks in layers. Because it thinks in layers, it distributes the dimensions of a Datum across those layers — one dimension per layer, coordinated manually, drifting apart over time.

The semantic dimension ends up in the domain model — if the team is disciplined enough to have one. Often, it ends up split between the model and the controller, or between the model and the database schema.

The presentational dimension ends up in the frontend. A developer writes a conditional: `if user.role === 'admin' then show this field`. That conditional is a business rule — it encodes who may see what — but it exists only in a frontend component, decided by one developer, at one moment, with no governing authority behind it. When the rule changes, someone must remember that conditional exists. Often, nobody does.

The operational dimension ends up scattered. Controllers handle some consequences. Event listeners handle others. Migration files encode the storage shape. Integration adapters handle external interactions. Each lives in a different file, a different layer, under a different team's ownership. The Datum's operational life is not described anywhere as a whole. It is implied only by the sum of disconnected implementations.

The result is predictable.

- **Security failures** — data visible to actors who should not see it because the presentational dimension was governed by a developer's assumption rather than the Datum's own authority
- **Inconsistent behavior** — the same business rule enforced on one screen and forgotten on another
- **Processes with no consequence** — operations that execute and produce nothing meaningful because the operational dimension was never fully described
- **Dead data** — records that exist but trigger nothing, connect to nothing, mean nothing operationally; data that has lost its purpose

**When you split a Datum, you do not get a smaller, cleaner system. You get a fragmented system that behaves unpredictably — and eventually a system whose behavior nobody fully understands.**

This is not a failure of discipline. It is the structural consequence of thinking in layers rather than in whole meaningful units.

---

## 6. What Is and Is Not a Datum

This question — what counts as a Datum — is the boundary of the theory, and it must be drawn precisely.

### 6.1 The Defining Criterion

A Datum is any unit of software reality that carries business identity.

Business identity means this: the thing has a meaning in the domain that is irreducible. It cannot be broken further without losing what it is. A hotel type is a Datum. A hotel is a Datum. A commission rate, depending on business context, may itself be a Datum — carrying its own semantic rules, presentational governance, and operational consequences. A phone number within a client record is a Datum. A validation error raised by a phone number is an expression of the phone number Datum's semantic dimension — part of it, not separate from it.

The test is simple: **Is this the smallest unit that still retains its own meaning within the business domain?**

### 6.2 All Datums Have All Three Dimensions

A critical clarification: there is no such thing as a Datum with only one or two dimensions.

If a unit has business identity — if it is a Datum — then it has all three dimensions. The dimensions are not optional features of a Datum. They are constitutive of it. A Datum without a presentational dimension does not have a hidden presentational dimension waiting to be discovered. It means the presentational dimension is ungoverned — decided ad hoc elsewhere by someone who should not be making that decision alone.

Similarly, a Datum without a governed operational dimension does not mean the Datum has no operational life. It means that operational life is scattered — happening somewhere in the system, triggered by something, producing some consequence — but not governed by the Datum that owns it.

The absence of a governed dimension is not a property of the Datum. It is a failure of the system that contains it.

### 6.3 What Is Not a Datum

Not everything in a software system is a Datum.

**Technical scaffolding is not a Datum.** A CSS class, a database index, a build configuration file, a deployment script — these carry no business identity. They exist to serve the expression of Datums but are not themselves meaningful units of the business domain.

**Infrastructure concerns are not Datums.** A connection pool, a cache layer, a load balancer configuration — these have no business meaning. Changing them does not change what the system means to the people who use it.

**Ephemeral technical artifacts are not Datums on their own.** A validation error is not a standalone Datum — it is an expression of the Datum that produced it. A log entry records something that happened to a Datum but is not itself a Datum unless it carries independent business meaning, such as an audit record that is itself a business-meaningful unit.

**The distinction is always the same:** does this carry irreducible business meaning? If yes, it is a Datum, and all three of its dimensions must be governed. If no, it is technical infrastructure serving the expression of Datums.

### 6.4 Datums Contain Datums

Just as molecules are composed of atoms, larger Datums are composed of smaller ones.

A `Client` is a Datum. Within it, `ClientCode` is a Datum — a smaller unit that retains its own identity and rules. A `Hotel` is a Datum. Within it, `CommissionRate` is a Datum with its own semantic rules, its own presentational governance, and its own operational consequences.

This compositional structure mirrors the physical world. Atoms combine into molecules. Molecules combine into compounds. Each level retains the governed wholeness of its constituent units while forming a larger meaningful structure.

In software terms, Datums combine into aggregates. Aggregates combine into bounded contexts. Each level retains governed wholeness. The failure of conventional architecture is that it breaks this wholeness at every level — scattering the dimensions of atoms, molecules, and compounds alike across separate technical layers.

### 6.5 The Real Question Is Not Whether — But How Well

In a real system, every meaningful unit is a Datum. The question is never "is this a Datum?" The question is always "how well are this Datum's dimensions governed?"

A phone number whose visibility is decided by a developer writing a conditional in a React component is still a Datum. But its presentational dimension is ungoverned, and ungoverned dimensions produce the failure modes described in Section 5.

A hotel type that exists only as a database row with no governed presentation and no operational consequences is still a Datum. But its dimensions are collapsed, and collapsed dimensions produce dead data: records that exist but mean nothing operationally.

The goal of Datum Theory is not to classify things as Datums or non-Datums. The goal is to recognize that every meaningful unit already has three dimensions — and to insist that all three be governed by the unit itself rather than scattered to be decided by whoever happens to touch that layer next.

---

## 7. The Three-Dimensional Nature of Software

Conventional architecture is flat.

It has layers — frontend, backend, database — but they are separate planes. A field exists in one dimension at a time. The database column exists in the persistence plane. The API response exists in the transport plane. The rendered input exists in the presentation plane. They are projections of the same underlying truth onto separate surfaces.

Datum Theory makes software three-dimensional.

A Datum exists simultaneously in all three of its dimensions — semantic, presentational, operational. Not projected across layers. Not split into fragments coordinated by discipline. Whole. Like an atom occupying real space in all dimensions at once.

When you build software according to Datum Theory, you are not building a stack of layers. You are building a collection of three-dimensional meaningful units that govern their own expression across every surface they touch. The result is software that knows what it is, software that can describe itself to any consumer, software whose truth does not drift because its truth is not distributed.

This is three-dimensional software.

---

## 8. From Ontology to Governance Doctrine

Datum Theory is a philosophical and ontological claim about software. It does not prescribe a specific implementation. It establishes a ground truth: meaningful software units are three-dimensional, and those dimensions must remain under unified authority.

What follows from that ground truth is a class of governance doctrines — architectural methodologies that take Datum Theory seriously as their foundation and derive their structural decisions from it.

A governance doctrine derived from Datum Theory must satisfy three conditions. It must place the domain as the highest authority over semantic truth — not merely as a well-modeled layer, but as the source from which all other layers derive their terms. It must require the domain to govern presentational truth — defining what consumers may see and do, not delegating that authority to delivery surfaces. And it must require the domain to govern operational truth — defining persistence shape, process participation, event records, and integration contracts, not leaving those dimensions to be invented by infrastructure.

Any architecture that satisfies these three conditions is an expression of Datum Theory in practice.

Domain-Sovereign Architecture (DSA) is one such expression — a concrete governance doctrine that translates Datum Theory into architectural law, implementation patterns, team models, and delivery constraints. It is the methodology that answers the practical question: if Datum Theory is true, how should software be built?

The relationship between Datum Theory and DSA is the relationship between ontology and doctrine. Datum Theory explains what software units are. DSA governs how systems must be built if that explanation is taken seriously.

In shorthand:

- **DDD protects the meaning of the domain**
- **Datum Theory explains the full dimensional structure of meaningful software units**
- **DSA governs the system according to that structure**

Or, as precisely as possible in one sentence:

**DSA is DDD extended from semantic modeling doctrine into full-dimensional governance doctrine.**
---

## 9. The Four Claims of Datum Theory

**Claim 1 — Ontological:**  
A meaningful unit of software reality — a Datum — has three irreducible dimensions of existence: semantic, presentational, and operational. These dimensions are not architectural choices. They are intrinsic to the nature of meaningful software units. They were always there. The phone number always had a storage face, a presentation face, and a reaction face. Conventional architecture did not create these dimensions. It only fragmented them.

**Claim 2 — Structural:**  
Conventional layer-based architecture fragments the Datum. By distributing its dimensions across technical layers — by letting developers decide presentational rules ad hoc, by scattering operational consequences across disconnected handlers — it produces systems whose truth is distributed, whose coordination cost rises over time, and whose behavior cannot be traced to any single authoritative description. The security vulnerabilities, inconsistent interfaces, and purposeless processes found in production software are not random failures. They are the predictable structural result of Datum fragmentation.

**Claim 3 — Prescriptive:**  
Software should be built from whole Datums — meaningful units that maintain authority over all three of their dimensions simultaneously. The Datum should be self-describing: able to tell any consumer what it is, how it may be seen, and how it may be acted upon. The question is never whether the dimensions exist. They always do. The question is whether they are governed by the Datum or scattered to be decided elsewhere.

**Claim 4 — Generative:**  
A system whose Datums are whole and self-describing can be described as structured data before it is emitted as code. The DNA of a system — the structured encoding of its Datums and their relationships — becomes the real asset. Code is a downstream artifact of that encoding. This is the direction in which Datum Theory points software creation: from manual layer-by-layer construction toward structured authorship of meaning that generates its own expression.

---

## 10. Relationship to Domain-Driven Design

Datum Theory is not a rejection of Domain-Driven Design. It is an extension of it.

DDD taught the software industry to take the domain seriously as a model of business meaning. It gave us entities, value objects, aggregates, bounded contexts, and ubiquitous language. It argued that software should model business concepts faithfully and that the domain model should be the center of the system.

That was a profound contribution. But DDD stopped at the boundary of the domain. It said: model the domain correctly. It did not say: let the domain be authoritative over presentation and persistence. It left those dimensions to infrastructure adapters and UI layers — well-designed ones, ideally, but still separate.

Datum Theory asks the deeper question: what is a meaningful software unit, really? And it answers: not just a well-modeled domain object. A meaningful software unit has three dimensions of existence, and all three must remain under unified authority.


---

## 11. On the Name

The word Datum is chosen deliberately.

In Latin, *datum* means "that which is given" — a given fact, a piece of information considered as a starting point. In science, data are the raw observations from which understanding is built.

But in Datum Theory, a Datum is not raw. It is the least unit that retains meaning. It is the smallest thing that is still something — still a phone number, still a hotel type, still a reservation — rather than merely a collection of bytes.

The singular form — Datum, not Data — is also deliberate. Data is plural. A Datum is one. Datum Theory is about the individual meaningful unit, not data in the aggregate sense. It is about what one thing is, in all its dimensions, before it is combined with other things.

The name also carries the chemist's instinct. A chemist does not study matter in the abstract. A chemist studies this element, this compound, this reaction. Datum Theory studies this unit — the phone number, the hotel type, the client record — not software in the abstract.

---

## Closing Statement

In 2019, I saw an ocean of atomic software. In the years that followed, I watched conventional software fragment its meaningful units across layers and pay the coordination cost. I watched developers make presentational decisions that belonged to the domain. I watched operational consequences scatter across disconnected handlers. I watched data exposed to actors who should never have seen it because nobody governed the presentational dimension of the unit that held it. I watched processes execute with no consequence because nobody governed the operational dimension of the units they touched.

And I observed that the atom — the most studied, most understood, most fundamental unit in physical science — had already solved this problem.

The atom does not ask which layer owns its charge. The atom does not distribute its bonding behavior to an adapter and its spectroscopic signature to a rendering component. The atom is whole. Its identity, its presentation, and its operational behavior are three dimensions of one reality, governed from within, expressing outward.

Software should work the same way.

A Datum is software's atom. It is the unit that retains meaning. It carries its semantic truth, its presentational truth, and its operational truth — whole, self-describing, governing its own expression across every surface it touches.

The failure modes of modern software — the security vulnerabilities, the inconsistent interfaces, the processes that mean nothing — are not mysteries. They are the result of splitting the Datum. Of deciding that its dimensions belong to different layers, different teams, different moments of implementation, different developers who each make their own judgment and then move on.

When software is built from whole Datums, under unified authority, fragmentation ends. The truth does not drift. The coordination cost does not rise. The system knows what it is. And the people who build it know where to look when something breaks, because the truth lives in one place rather than scattered across four.

That is the promise of Datum Theory.  
That is what the atom taught me about software.

---

*© 2026 Bilal Mahmud*

*Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0)*  
*https://creativecommons.org/licenses/by/4.0/*

*You are free to share, implement, adapt, and build upon this work for any purpose, provided you give appropriate credit to the original author: Bilal Mahmud.*

---

*Domain-Sovereign Architecture (DSA) is the architectural governance doctrine derived from Datum Theory.*
