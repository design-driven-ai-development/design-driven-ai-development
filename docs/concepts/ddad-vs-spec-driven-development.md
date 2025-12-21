---
title: Design-Driven AI Development vs Spec-Driven Development
layout: default
---

# Design-Driven AI Development vs Spec-Driven Development

As Design-Driven AI Development (DDAD) gains adoption, it is reasonable to ask how it relates to existing engineering practices—particularly **Spec-Driven Development (SDD)** and closely related ideas such as **Spec-Driven Architecture**.

At a high level, these approaches share foundational principles. However, they address **different governance concerns**. This document clarifies the relationship and explains why DDAD is not a rebranding of Spec-Driven Development, but an extension required for **AI-mediated execution**.

---

## Spec-Driven Development and Spec-Driven Architecture

Spec-Driven Development is an established engineering practice grounded in the following premise:

> **System behavior is defined by explicit specifications, and implementations are required to conform to those specifications.**

Closely related concepts are often discussed under the term *Spec-Driven Architecture*, where specifications act as the primary architectural contract between systems and teams.

Representative references include:

- **Martin Fowler – Specification by Example**  
  https://martinfowler.com/bliki/SpecificationByExample.html

- **OpenAPI / Contract-First API Design**  
  https://swagger.io/resources/articles/adopting-an-api-first-approach/

- **Consumer-Driven Contracts (CDC)**  
  https://martinfowler.com/articles/consumerDrivenContracts.html

- **Protocol-Oriented / Spec-First Design (IETF, W3C)**  
  https://www.ietf.org/standards/  
  https://www.w3.org/standards/

These approaches emphasize that **implementation must not be the authority**; specifications are.

---

## Areas of Alignment Between SDD and DDAD

Design-Driven AI Development intentionally aligns with the core principles of Spec-Driven Development.

Both approaches assume that:
- Implementation should not be the primary source of truth
- Decisions should be made prior to execution
- Review should focus on intent rather than outcomes alone
- Deterministic behavior is preferable to improvisation at scale

DDAD does not reject Spec-Driven Development. It builds upon these foundations.

---

## The Key Difference: What Is Being Governed

The fundamental distinction lies in **what each approach governs**.

- **Spec-Driven Development governs system behavior**
- **Design-Driven AI Development governs AI execution behavior**

Spec-Driven Development answers questions such as:
- What should the system do?
- How is behavior specified?
- Does the implementation conform to the specification?

Design-Driven AI Development addresses additional questions that arise when AI systems participate directly in software development:
- Who is authorized to make decisions when intent is unclear?
- How is AI prevented from inferring or inventing intent?
- What constraints apply to AI behavior?
- When is AI execution permitted to proceed?
- When must AI execution stop?

These questions fall outside the traditional scope of Spec-Driven Development and Spec-Driven Architecture.

---

## The Governance Gap Introduced by AI

### Absence of AI-Specific Controls in SDD

Spec-Driven Development does not typically define:
- Rules governing AI behavior
- Boundaries on AI inference
- Mechanisms for limiting execution scope
- Explicit separation between decision authority and execution authority

In AI-assisted workflows, this absence becomes material.

Design-Driven AI Development introduces explicit governance artifacts to address this gap, including:
- **AGENTS.md** — defines allowed and disallowed AI behavior
- **TODO.md** — authorizes discrete execution units
- Clear separation of human decision authority and AI execution responsibility

These constructs do not exist in classical Spec-Driven Development.

---

### Preventing Unintentional Decision Delegation

In AI-mediated development, a new risk emerges:

```
Incomplete specification + AI execution → AI fills decision gaps
```

Spec-Driven Development assumes that humans resolve ambiguity during implementation.

Design-Driven AI Development assumes the opposite:

> **AI will infer intent unless explicitly constrained.**

As a result, DDAD treats ambiguity as a failure condition rather than a flexibility point. This stricter posture is necessary to preserve decision ownership.

---

## Decision Ownership as a First-Class Concern

Spec-Driven Development primarily governs *what* the system should do.

Design-Driven AI Development adds an explicit model for *who is allowed to decide*.

| Concern | Spec-Driven Development | Design-Driven AI Development |
|------|-------------------------|------------------------------|
| Defines system behavior | Yes | Yes |
| Formalizes specifications | Yes | Yes |
| Assigns decision authority | No | Yes |
| Constrains AI behavior | No | Yes |
| Authorizes execution | No | Yes |
| Prevents scope creep | No | Yes |

DDAD governs authority and accountability in addition to behavior.

---

## Why “Design-Driven” Rather Than “Spec-Driven”

The term *design* is used deliberately.

Specifications typically capture:
- Interfaces and contracts
- Formal behavior
- Structural constraints

Design captures a broader intent surface, including:
- Architectural trade-offs
- Non-functional requirements
- Constraints and prohibitions
- Rationale behind decisions

AI systems require this broader context because, absent constraints, they will:
- Optimize beyond intent
- Refactor opportunistically
- Infer behavior from partial information

DDAD therefore requires **design authority**, not specification alone.

---

## Relationship Between SDD and DDAD

The relationship can be summarized succinctly:

```
Spec-Driven Development
→ Governs system behavior

Design-Driven AI Development
→ Governs AI execution behavior
```

The two approaches are complementary.

DDAD does not replace Spec-Driven Development. It extends it to address governance challenges introduced by AI-mediated execution.

---

## Summary

- Spec-Driven Development and Spec-Driven Architecture remain essential for defining system behavior
- AI introduces new risks related to decision delegation and intent inference
- Design-Driven AI Development addresses these risks explicitly
- DDAD adds governance for AI execution without discarding existing engineering discipline

AI reduces the cost of execution.  
DDAD ensures the value of decisions is preserved.