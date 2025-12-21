---
title: References
layout: default
---

# References

This document consolidates the primary concepts, practices, and bodies of work referenced across the **Design-Driven AI Development (DDAD)** documentation and article series.

DDAD is not presented as a standalone invention. It is an extension and formalization of established **design-first, specification-first, and governance-oriented engineering practices**, adapted for environments where AI participates directly in software execution.

---

## Design-First and Architecture-First Engineering

While there is no single standardized methodology formally named *Design-Driven Development*, the principle of **design preceding execution** is well-established across software architecture and systems engineering.

### Architectural Decision Records (ADR)
- Michael Nygard – *Documenting Architecture Decisions*  
  https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions

Establishes architectural decisions as first-class artifacts captured prior to implementation.

---

### Software Architecture and Design Authority
- Martin Fowler – Software Architecture  
  https://martinfowler.com/architecture/

Provides foundational guidance on architectural responsibility, trade-offs, and long-lived system design.

---

### Model-Based and Design-Centric Engineering
- INCOSE – Model-Based Systems Engineering (MBSE)  
  https://www.incose.org/systems-engineering/model-based-systems-engineering

Demonstrates design authority and model-first execution in complex systems.

---

## Spec-Driven Development and Spec-Driven Architecture

Spec-Driven Development defines system behavior through explicit specifications that implementations must conform to.

### Specification by Example
- Martin Fowler  
  https://martinfowler.com/bliki/SpecificationByExample.html

Introduces executable specifications as a means to capture intent before implementation.

---

### Contract-First / API-First Design
- OpenAPI Initiative  
  https://www.openapis.org/
- Swagger – API-First Approach  
  https://swagger.io/resources/articles/adopting-an-api-first-approach/

Defines APIs as contracts before implementation.

---

### Consumer-Driven Contracts
- Martin Fowler – Consumer Driven Contracts  
  https://martinfowler.com/articles/consumerDrivenContracts.html

Establishes consumer-owned specifications validated against provider implementations.

---

### Protocol and Standards-Based Design
- Internet Engineering Task Force (IETF)  
  https://www.ietf.org/standards/
- World Wide Web Consortium (W3C)  
  https://www.w3.org/standards/

Illustrates long-lived systems governed by specifications rather than implementations.

---

## Verification, Validation, and Quality

### Test-Driven Development (TDD)
- Kent Beck – *Test Driven Development: By Example*

Establishes verification as a mechanism for enforcing intent after decisions are made.

---

### Static Analysis and Security Verification
- OWASP Code Review Guide  
  https://owasp.org/www-project-code-review-guide/

Provides guidance on verification techniques independent of subjective review.

---

### Software Quality Models
- ISO/IEC 25010 – Software Quality Model  
  https://www.iso.org/standard/35733.html

Defines quality characteristics relevant to governance and maintainability.

---

## Review Models and Governance

### Traditional Code Review Practices
- Google Engineering Practices – Code Review  
  https://google.github.io/eng-practices/review/

Describes review models developed for human-authored codebases.

---

### Decision-Making vs Execution
- Herbert A. Simon – *The Sciences of the Artificial*

Introduces the foundational distinction between decision-making and execution in complex systems.

---

## AI and Software Engineering

### AI-Assisted Development
- GitHub Copilot Documentation  
  https://docs.github.com/en/copilot
- GitHub Engineering Blog  
  https://github.blog/

Provides context on AI-assisted coding and emerging execution models.

---

## Systems Thinking and Control

### Separation of Concerns
- Edsger W. Dijkstra – *On the Role of Scientific Thought*

Establishes separation of responsibility as a prerequisite for scalable systems.

---

### Control vs Automation
- Norbert Wiener – *Cybernetics: Or Control and Communication in the Animal and the Machine*

Foundational work on control systems versus automated execution.

---

## Relationship to Design-Driven AI Development

Design-Driven AI Development builds on these bodies of work to address a new condition:

> **AI dramatically reduces the cost of execution while increasing the risk of implicit decision-making.**

DDAD introduces explicit governance for:
- AI behavior
- Decision authority
- Execution boundaries
- Scope containment

It does not replace specifications, architecture, or verification practices.  
It extends them to remain effective in AI-mediated environments.

---

## Canonical DDAD Reference

Primary documentation for Design-Driven AI Development is available at:

https://design-driven-ai-development.github.io/design-driven-ai-development/

---

## Citation Guidance

When referencing DDAD externally, the following description is recommended:

> *Design-Driven AI Development (DDAD) is an approach to AI-assisted software engineering that separates human decision-making from AI execution, ensuring design intent remains explicit, reviewable, and auditable at scale.*

---

End of references.
