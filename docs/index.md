---
layout: default
title: Design-Driven AI Development (DDAD)
---

# Design-Driven AI Development (DDAD)

![DDAD Logo]({{ '/images/DDAD.png' | relative_url }})

## Overview

Design-Driven AI Development (DDAD) is a methodology for using AI in software development
where **design artifacts, not prompts, govern execution**.

DDAD ensures that AI accelerates delivery **without compromising design intent,
governance, or engineering discipline**.

This approach applies uniformly to:
- Backend development (APIs, services, integrations)
- UI and frontend development (components, screens, flows)
- Full-stack systems

DDAD is tool-agnostic and vendor-neutral.

---

## The Core Problem DDAD Solves

AI can generate code quickly, but speed introduces risk when:
- Requirements are implicit
- Prompts replace specifications
- Context changes between executions
- Decisions are not recorded

This results in:
- Non-deterministic output
- Architectural drift
- Review fatigue
- Loss of accountability

DDAD replaces **prompt-driven development** with **design-driven execution**.

---

## Core Principle

> **Design defines behavior.  
> AI executes design.**

AI is treated as a **governed engineering participant**, not an autonomous author.

---

## DDAD Artifact Model

DDAD is implemented using a small, explicit set of repository artifacts:

```
README.md
  ↓ explains purpose

AGENTS.md
  ↓ governs AI behavior

TODO.md
  ↓ authorizes work

LLD Markdown
  ↓ defines implementation

Code + Tests
```

---

## Roles and Responsibilities

### Human Responsibilities
- Define requirements and design
- Author Low Level Design (LLD) documents
- Approve work via TODO.md
- Review and accept changes

### AI Responsibilities
- Follow AGENTS.md constraints
- Execute exactly one TODO item at a time
- Implement strictly according to LLD
- Avoid speculative or unrelated changes
- Commit changes transparently

---

## DDAD Execution Flow

1. Human defines design in LLD Markdown
2. Human adds a TODO item referencing the LLD
3. AI reads AGENTS.md for constraints
4. AI executes the TODO according to the LLD
5. AI runs tests or validations
6. AI commits changes
7. AI moves the TODO item to DONE
8. Human reviews and continues

Autonomy is always **explicitly granted**, never assumed.

---

## DDAD for Backend Development

DDAD controls:
- API contracts
- Validation rules
- Error handling
- Persistence behavior
- Transaction boundaries

---

## DDAD for UI Development

DDAD controls:
- Component hierarchy
- Props and state
- Interaction flows
- Accessibility requirements
- Error and empty states

---

## Benefits of DDAD

- Predictable outcomes
- Reduced hallucination
- Clear audit trail
- Safer AI adoption
- Easier reviews
- Scales across teams

---

## What DDAD Is Not

DDAD is not:
- Fully autonomous AI development
- A framework or SDK
- Prompt engineering guidance
- A replacement for design or reviews
- AI-based code review (design is reviewed, code is verified)

---

## Code Review in DDAD

DDAD intentionally **does not use agentic or LLM-based code review tools**.

> **In DDAD, design is reviewed.  
> Code is verified.**

Code correctness is determined by conformance to design. Design artifacts are reviewed by humans. Code is verified to match design through comparison and automated tests.

[Learn more about DDAD's code review position →]({{ '/concepts/code-review-position' | relative_url }})

## Closing Statement

AI can write code.
Only design can define behavior.

> **Design-Driven AI Development keeps humans in control  
> while letting AI do the work.**

---

## Quick Navigation

### Core Concepts
- [What is DDAD?]({{ '/concepts/what-is-ddad' | relative_url }})
- [The Core Problem]({{ '/concepts/the-core-problem' | relative_url }})
- [DDAD vs Prompt-Driven]({{ '/concepts/ddad-vs-prompt-driven' | relative_url }})
- [Code Review Position]({{ '/concepts/code-review-position' | relative_url }})

### Artifacts
- [AGENTS.md]({{ '/artifacts/agents-md' | relative_url }})
- [TODO.md]({{ '/artifacts/todo-md' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})

### Execution
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [Human Responsibilities]({{ '/execution/human-responsibilities' | relative_url }})
- [AI Responsibilities]({{ '/execution/ai-responsibilities' | relative_url }})

### Examples
- [Backend Example]({{ '/examples/backend-example' | relative_url }})
- [UI Example]({{ '/examples/ui-example' | relative_url }})

### Templates
- [AGENTS.md Template]({{ '/templates/AGENTS' | relative_url }})
- [TODO.md Template]({{ '/templates/TODO' | relative_url }})
- [LLD Template]({{ '/templates/lld-template' | relative_url }})

### Adoption
- [Getting Started]({{ '/adoption/getting-started' | relative_url }})
- [Team Adoption]({{ '/adoption/team-adoption' | relative_url }})