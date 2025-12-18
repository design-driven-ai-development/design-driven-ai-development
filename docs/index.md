---
layout: default
title: Design-Driven AI Development (DDAD)
---

<div class="hero">
    <div class="container">
        <h1>Design-Driven AI Development</h1>
        <p>Where design artifacts, not prompts, govern execution</p>
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

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; margin: 2rem 0;">
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/concepts/what-is-ddad' | relative_url }}">What is DDAD?</a></h3>
    <p style="margin-bottom: 0;">Learn about Design-Driven AI Development and how it differs from traditional approaches.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/concepts/the-core-problem' | relative_url }}">The Core Problem</a></h3>
    <p style="margin-bottom: 0;">Understand the problems DDAD solves and why design artifacts matter.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/concepts/ddad-vs-prompt-driven' | relative_url }}">DDAD vs Prompt-Driven</a></h3>
    <p style="margin-bottom: 0;">Compare design-driven and prompt-driven approaches to AI development.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/concepts/code-review-position' | relative_url }}">Code Review Position</a></h3>
    <p style="margin-bottom: 0;">Learn why DDAD doesn't use AI code review and how verification works.</p>
  </div>
</div>

## Artifacts

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; margin: 2rem 0;">
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/artifacts/artifact-model' | relative_url }}">Artifact Model</a></h3>
    <p style="margin-bottom: 0;">Understand the DDAD artifact flow: README → AGENTS → TODO → LLD → Code</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/artifacts/agents-md' | relative_url }}">AGENTS.md</a></h3>
    <p style="margin-bottom: 0;">Governs AI behavior and defines constraints for code generation.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/artifacts/todo-md' | relative_url }}">TODO.md</a></h3>
    <p style="margin-bottom: 0;">Authorizes specific work items and references LLD sections.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/artifacts/lld-markdown' | relative_url }}">LLD Markdown</a></h3>
    <p style="margin-bottom: 0;">Defines exact implementation requirements and business rules.</p>
  </div>
</div>

## Execution

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; margin: 2rem 0;">
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/execution/execution-flow' | relative_url }}">Execution Flow</a></h3>
    <p style="margin-bottom: 0;">Step-by-step process of how humans and AI collaborate in DDAD.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/execution/human-responsibilities' | relative_url }}">Human Responsibilities</a></h3>
    <p style="margin-bottom: 0;">What humans do: design, authorize, and verify in DDAD.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/execution/ai-responsibilities' | relative_url }}">AI Responsibilities</a></h3>
    <p style="margin-bottom: 0;">What AI does: execute design according to artifacts.</p>
  </div>
</div>

## Examples & Templates

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; margin: 2rem 0;">
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/examples/backend-example' | relative_url }}">Backend Example</a></h3>
    <p style="margin-bottom: 0;">See DDAD in action with a backend service example.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/examples/ui-example' | relative_url }}">UI Example</a></h3>
    <p style="margin-bottom: 0;">Learn how DDAD applies to UI and frontend development.</p>
  </div>
  <div style="background: var(--bg-light); padding: 1.5rem; border-radius: 8px; border-left: 4px solid var(--accent);">
    <h3 style="margin-top: 0;"><a href="{{ '/templates/AGENTS' | relative_url }}">Templates</a></h3>
    <p style="margin-bottom: 0;">Get started with ready-to-use templates for AGENTS.md, TODO.md, and LLD.</p>
  </div>
</div>
