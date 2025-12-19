---
layout: default
title: Human Responsibilities in DDAD
---

# Human Responsibilities in DDAD

## Overview

In DDAD, humans are responsible for design, authorization, and review. AI executes design, but humans remain in control.

## Core Responsibilities

### 1. Define Requirements and Design

**What**: Create design artifacts that define what to build

**Activities**:
- Write LLD Markdown documents
- Define business rules
- Specify validation requirements
- Document error handling
- Define transaction boundaries
- Specify security requirements

**Why**: Design defines behavior. Without clear design, AI cannot produce correct code.

### 2. Author Low Level Design (LLD) Documents

**What**: Create detailed LLD Markdown documents

**Activities**:
- Write comprehensive LLD sections
- Include all necessary details
- Cover edge cases
- Specify exact requirements
- Keep LLD updated

**Why**: LLD is the specification that AI follows. Quality LLD leads to quality code.

### 3. Approve Work via TODO.md

**What**: Authorize specific work items

**Activities**:
- Create TODO items
- Reference LLD sections
- Specify dependencies
- Authorize AI to work

**Why**: TODO.md authorizes work. AI only works on authorized items.

### 4. Review Design and Verify Code

**What**: Review design artifacts and verify code conformance

**Activities**:
- **Review Design (LLD)**: Review LLD Markdown for correctness and completeness
- **Verify Code**: Verify code matches LLD exactly
- **Run Tests**: Execute automated tests
- **Check Conformance**: Ensure implementation matches design
- Approve or request changes

**Why**: In DDAD, design is reviewed and code is verified. Code correctness is determined by conformance to design, not by AI review.

**Note**: DDAD does not use AI or agentic code review tools. Code verification is done by comparing code to LLD and running automated tests.

## Additional Responsibilities

### Maintain Artifacts
- Keep LLD current
- Update TODO status
- Maintain README.md
- Update AGENTS.md as needed

### Make Strategic Decisions
- Architecture decisions
- Technology choices
- Design trade-offs
- Business rule decisions

### Govern AI Behavior
- Define AGENTS.md constraints
- Set boundaries
- Establish rules
- Enforce governance

## What Humans Don't Do

### ❌ Write Code Manually
- AI generates code from LLD
- Humans don't write implementation code
- Focus on design, not coding

### ❌ Write Prompts
- No ad-hoc prompts
- Design artifacts replace prompts
- Formal specifications, not conversations

### ❌ Debug AI Code
- AI generates correct code from LLD
- If code is wrong, LLD may be wrong
- Fix LLD, regenerate code

## The Shift

### Traditional Development
```
Human: Write code → Test → Debug → Deploy
```

### DDAD Development
```
Human: Design → Authorize → Review → Deploy
AI:    Execute → Test → Commit
```

## Key Principles

### 1. Design First
- Always start with design
- Create LLD before TODO
- Design before code

### 2. Explicit Authorization
- Authorize via TODO.md
- Never assume AI can work
- Always explicit

### 3. Review Everything
- Review all generated code
- Compare against LLD
- Verify quality

### 4. Maintain Control
- Humans remain in control
- AI executes, doesn't decide
- Governance through artifacts

## Best Practices

### 1. Invest in Design
- Spend time on LLD
- Be specific and complete
- Quality design = quality code

### 2. Authorize Carefully
- Only authorize what's needed
- Check dependencies
- Manage scope

### 3. Review Thoroughly
- Review against LLD
- Verify tests
- Check quality

### 4. Iterate on Design
- Update LLD based on learnings
- Refine specifications
- Improve continuously

## Common Mistakes

### ❌ Vague LLD
**Problem**: Unclear requirements lead to poor code  
**Solution**: Be specific and complete in LLD

### ❌ Skipping Review
**Problem**: Assuming AI code is always correct  
**Solution**: Always review and verify

### ❌ Not Updating Artifacts
**Problem**: Artifacts become outdated  
**Solution**: Keep artifacts current

### ❌ Over-Authorization
**Problem**: Authorizing too much at once  
**Solution**: Authorize one TODO at a time

## Related Topics

- [AI Responsibilities]({{ '/execution/ai-responsibilities' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})

