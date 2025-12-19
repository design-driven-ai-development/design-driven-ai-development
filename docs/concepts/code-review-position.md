---
layout: default
title: DDAD Position on Code Review
---

# DDAD Position on Code Review

## Overview

Design-Driven AI Development intentionally **does not use agentic or LLM-based code review tools**.

In DDAD, code is generated strictly from approved design artifacts (Low Level Design Markdown). As a result:

- Code correctness is determined by conformance to design
- Design is the primary review surface
- Code review becomes a verification activity, not a subjective critique

## Why No AI Code Review?

Introducing AI-based code review would:
- **Reintroduce heuristic judgment**: AI review would add subjective opinions
- **Create a second source of truth**: Design artifacts are the source of truth, not AI review
- **Undermine design authority**: Design decisions are made by humans, not AI

## What Review Means in DDAD

DDAD distinguishes clearly between **review** and **verification**.

### Allowed

#### Human Review of Design (LLD)
- Review LLD Markdown documents
- Verify design correctness
- Ensure completeness
- Validate business rules
- Check architectural alignment

#### Human Verification of Code
- Verify code matches LLD
- Check conformance to design
- Ensure implementation correctness
- Validate against specifications

#### Automated Verification
- Automated tests (unit, integration)
- Linters and static analysis
- Code quality tools
- Security scanners

### Not Allowed

#### AI or Agentic Code Review
- ❌ LLM-based code review tools
- ❌ Agentic review systems
- ❌ AI-generated review comments
- ❌ Automated "best practice" suggestions

#### Heuristic Feedback
- ❌ Subjective "best practice" feedback
- ❌ Opinion-based refactoring suggestions
- ❌ Style preferences not in design
- ❌ "Better way" suggestions

## The Principle

> **In DDAD, design is reviewed.  
> Code is verified.**

### Design Review
- Humans review LLD documents
- Verify design correctness
- Ensure completeness
- Validate requirements

### Code Verification
- Verify code matches LLD
- Check conformance to design
- Run automated tests
- Ensure correctness

## Why This Matters

### Design as Source of Truth
- Design artifacts define behavior
- Code implements design
- Verification ensures conformance
- No second source of truth needed

### Avoiding Confusion
- AI review would introduce opinions
- Could conflict with design
- Creates ambiguity
- Undermines design authority

### Maintaining Control
- Humans control design
- Design controls code
- Verification ensures conformance
- Clear accountability

## The Verification Process

### Step 1: Design Review
```
Human reviews LLD Markdown
    ↓
Verifies correctness
    ↓
Approves design
```

### Step 2: Code Generation
```
AI generates code from LLD
    ↓
Code matches design
```

### Step 3: Code Verification
```
Human verifies code matches LLD
    ↓
Runs automated tests
    ↓
Checks conformance
    ↓
Approves if correct
```

## Common Misconceptions

### ❌ "AI review would catch bugs"
**Reality**: If code matches LLD and LLD is correct, there are no bugs. If code doesn't match LLD, verification catches it.

### ❌ "AI review improves code quality"
**Reality**: Code quality is defined by design. If design is good, code is good. If design needs improvement, improve design.

### ❌ "AI review is faster"
**Reality**: Verification against LLD is faster and more reliable than AI review. Clear specification enables quick verification.

## Best Practices

### 1. Invest in Design Review
- Thoroughly review LLD before code generation
- Ensure design is correct and complete
- Fix design issues before implementation

### 2. Verify Against Design
- Compare code to LLD section by section
- Verify business rules implemented
- Check validation rules applied
- Ensure error handling matches

### 3. Use Automated Tools
- Run tests to verify functionality
- Use linters for code quality
- Run static analysis for issues
- Use security scanners

### 4. Trust the Process
- If design is correct and code matches design, code is correct
- Don't second-guess with AI review
- Trust verification over AI opinions

## Related Topics

- [What is DDAD?]({{ '/concepts/what-is-ddad' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [Human Responsibilities]({{ '/execution/human-responsibilities' | relative_url }})

