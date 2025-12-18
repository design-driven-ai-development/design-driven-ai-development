---
layout: default
title: What is DDAD?
---

# What is Design-Driven AI Development (DDAD)?

![DDAD Concept]({{ '/images/DAD_AI_Current.png' | relative_url }})

## Overview

Design-Driven AI Development (DDAD) is a methodology for using AI in software development
where **design artifacts, not prompts, govern execution**.

DDAD ensures that AI accelerates delivery **without compromising design intent,
governance, or engineering discipline**.

## Key Characteristics

### Design Artifacts Govern Execution
In DDAD, design artifacts (not prompts) control what AI does:
- **AGENTS.md** governs AI behavior and constraints
- **TODO.md** authorizes specific work items
- **LLD Markdown** defines exact implementation requirements

### Tool-Agnostic and Vendor-Neutral
DDAD is not tied to any specific:
- AI tool or platform
- Programming language
- Framework or SDK
- Development methodology

### Universal Application
This approach applies uniformly to:
- **Backend development**: APIs, services, integrations
- **UI and frontend development**: Components, screens, flows
- **Full-stack systems**: End-to-end features

## Core Principle

> **Design defines behavior.  
> AI executes design.**

AI is treated as a **governed engineering participant**, not an autonomous author.

## The Artifact Model

DDAD uses a small, explicit set of repository artifacts:

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

## What Makes DDAD Different

### Traditional AI-Assisted Development
- Ad-hoc prompts
- Implicit requirements
- Context loss between sessions
- No audit trail

### DDAD Approach
- ✅ Formal design artifacts
- ✅ Explicit requirements
- ✅ Persistent context
- ✅ Clear audit trail

## Benefits

- **Predictable outcomes**: Design artifacts ensure consistent results
- **Reduced hallucination**: Clear specifications reduce AI errors
- **Clear audit trail**: Artifacts document all decisions
- **Safer AI adoption**: Governance and control built-in
- **Easier reviews**: Review artifacts, not just code
- **Scales across teams**: Standardized approach works at scale

## What DDAD Is Not

DDAD is not:
- ❌ Fully autonomous AI development
- ❌ A framework or SDK
- ❌ Prompt engineering guidance
- ❌ A replacement for design or reviews
- ❌ AI-based code review (design is reviewed, code is verified)

## Related Concepts

- [The Core Problem]({{ '/concepts/the-core-problem' | relative_url }})
- [DDAD vs Prompt-Driven]({{ '/concepts/ddad-vs-prompt-driven' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})
