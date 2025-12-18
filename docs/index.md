---
title: Home
---
# Design-Driven AI Development (DDAD)

> **Design governs AI execution**

A governance-first methodology for AI-assisted software development.

## Start Here

1. Read the [DDAD Manifesto](/manifesto.md)
2. Understand the [DDAD Overview](/DDAD.md)
3. Explore the core artifacts under **Artifacts**


<div class="hero bg-light py-5 mb-4 border-bottom">
    <div class="container">
        <h1 class="display-4 fw-bold mb-3">Design-Driven AI Development</h1>
        <p class="lead mb-4">Where design artifacts, not prompts, govern execution</p>
        <a href="{{ '/adoption/getting-started' | relative_url }}" class="btn btn-primary btn-lg me-2">Get Started</a>
        <a href="{{ '/concepts/what-is-ddad' | relative_url }}" class="btn btn-outline-primary btn-lg">Learn More</a>
    </div>
</div>

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

## Core Concepts

<div class="row g-4 my-4">
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/concepts/what-is-ddad' | relative_url }}" class="text-decoration-none">What is DDAD?</a></h5>
        <p class="card-text">Learn about Design-Driven AI Development and how it differs from traditional approaches.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/concepts/the-core-problem' | relative_url }}" class="text-decoration-none">The Core Problem</a></h5>
        <p class="card-text">Understand the problems DDAD solves and why design artifacts matter.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/concepts/ddad-vs-prompt-driven' | relative_url }}" class="text-decoration-none">DDAD vs Prompt-Driven</a></h5>
        <p class="card-text">Compare design-driven and prompt-driven approaches to AI development.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/concepts/code-review-position' | relative_url }}" class="text-decoration-none">Code Review Position</a></h5>
        <p class="card-text">Learn why DDAD doesn't use AI code review and how verification works.</p>
      </div>
    </div>
  </div>
</div>

## Artifacts

<div class="row g-4 my-4">
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/artifacts/artifact-model' | relative_url }}" class="text-decoration-none">Artifact Model</a></h5>
        <p class="card-text">Understand the DDAD artifact flow: README → AGENTS → TODO → LLD → Code</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/artifacts/agents-md' | relative_url }}" class="text-decoration-none">AGENTS.md</a></h5>
        <p class="card-text">Governs AI behavior and defines constraints for code generation.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/artifacts/todo-md' | relative_url }}" class="text-decoration-none">TODO.md</a></h5>
        <p class="card-text">Authorizes specific work items and references LLD sections.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-3">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/artifacts/lld-markdown' | relative_url }}" class="text-decoration-none">LLD Markdown</a></h5>
        <p class="card-text">Defines exact implementation requirements and business rules.</p>
      </div>
    </div>
  </div>
</div>

## Execution

<div class="row g-4 my-4">
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/execution/execution-flow' | relative_url }}" class="text-decoration-none">Execution Flow</a></h5>
        <p class="card-text">Step-by-step process of how humans and AI collaborate in DDAD.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/execution/human-responsibilities' | relative_url }}" class="text-decoration-none">Human Responsibilities</a></h5>
        <p class="card-text">What humans do: design, authorize, and verify in DDAD.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/execution/ai-responsibilities' | relative_url }}" class="text-decoration-none">AI Responsibilities</a></h5>
        <p class="card-text">What AI does: execute design according to artifacts.</p>
      </div>
    </div>
  </div>
</div>

## Examples & Templates

<div class="row g-4 my-4">
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/examples/backend-example' | relative_url }}" class="text-decoration-none">Backend Example</a></h5>
        <p class="card-text">See DDAD in action with a backend service example.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/examples/ui-example' | relative_url }}" class="text-decoration-none">UI Example</a></h5>
        <p class="card-text">Learn how DDAD applies to UI and frontend development.</p>
      </div>
    </div>
  </div>
  <div class="col-md-6 col-lg-4">
    <div class="card h-100 border-start border-primary border-4">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ '/templates/AGENTS' | relative_url }}" class="text-decoration-none">Templates</a></h5>
        <p class="card-text">Get started with ready-to-use templates for AGENTS.md, TODO.md, and LLD.</p>
      </div>
    </div>
  </div>
</div>
