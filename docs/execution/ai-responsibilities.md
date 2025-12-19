---
layout: default
title: AI Responsibilities in DDAD
---

# AI Responsibilities in DDAD

## Overview

In DDAD, AI is a **governed engineering participant** that executes design, not an autonomous author that makes decisions.

## Core Responsibilities

### 1. Follow AGENTS.md Constraints

**What**: Read and follow AGENTS.md governance rules

**Activities**:
- Read AGENTS.md before starting work
- Understand capabilities and limitations
- Follow constraints strictly
- Respect boundaries

**Why**: AGENTS.md governs AI behavior and prevents scope creep.

### 2. Execute Exactly One TODO Item at a Time

**What**: Work on exactly one authorized TODO item

**Activities**:
- Find TODO items with Status: TODO
- Check dependencies are DONE
- Select one TODO item
- Execute completely
- Don't start next until current is DONE

**Why**: Focused execution ensures quality and prevents scope creep.

### 3. Implement Strictly According to LLD

**What**: Follow LLD Markdown exactly

**Activities**:
- Read referenced LLD section
- Understand requirements
- Implement exactly as specified
- Don't add features not in LLD
- Don't omit features from LLD

**Why**: LLD defines behavior. Following LLD ensures correct implementation.

### 4. Avoid Speculative or Unrelated Changes

**What**: Only make changes related to the TODO item

**Activities**:
- Stay within TODO scope
- Don't add unrelated features
- Don't make speculative improvements
- Don't refactor unrelated code

**Why**: Scope control prevents architectural drift and maintains focus.

### 5. Commit Changes Transparently

**What**: Commit all changes with clear messages

**Activities**:
- Stage all changes
- Write clear commit messages
- Reference TODO item
- Commit transparently

**Why**: Transparent commits enable review and audit.

## Additional Responsibilities

### Run Tests or Validations
- Run unit tests
- Run integration tests
- Validate against LLD
- Check code quality

### Update TODO Status
- Move TODO to DONE when complete
- Update TODO.md
- Maintain status

### Generate Tests
- Create unit tests
- Create integration tests
- Ensure coverage
- Follow testing standards

## What AI Doesn't Do

### ❌ Make Design Decisions
- AI doesn't decide what to build
- Humans define design in LLD
- AI only implements

### ❌ Authorize Work
- AI doesn't create TODO items
- Humans authorize via TODO.md
- AI only executes authorized work

### ❌ Skip Review
- AI doesn't bypass human review
- All code must be reviewed
- Humans approve changes

### ❌ Work Autonomously
- AI doesn't work without authorization
- Always needs TODO item
- Always follows governance

## The Mental Model

> **AI is a governed engineering participant,  
> not an autonomous author.**

AI executes design. Humans define design.

## Key Principles

### 1. Explicit Authorization Required
- Never assume authorization
- Always check TODO.md
- Only work on authorized items

### 2. Follow LLD Exactly
- Implement strictly according to LLD
- No additions outside LLD
- No omissions from LLD

### 3. One TODO at a Time
- Focus on one item
- Complete before moving on
- Maintain scope

### 4. Transparent Execution
- Commit all changes
- Clear commit messages
- Reference TODO and LLD

## Best Practices

### 1. Read Artifacts Carefully
- Read AGENTS.md for constraints
- Read TODO.md for authorization
- Read LLD for requirements

### 2. Execute Completely
- Finish TODO completely
- Don't leave partial work
- Ensure tests pass

### 3. Stay Within Scope
- Only work on authorized TODO
- Don't add unrelated features
- Maintain focus

### 4. Commit Transparently
- Clear commit messages
- Reference TODO item
- Document changes

## Common Mistakes

### ❌ Working Without Authorization
**Problem**: Starting work without TODO item  
**Solution**: Always check TODO.md first

### ❌ Adding Features Not in LLD
**Problem**: Implementing features not specified  
**Solution**: Follow LLD exactly, no additions

### ❌ Working on Multiple TODOs
**Problem**: Trying to do multiple items at once  
**Solution**: One TODO at a time, complete before next

### ❌ Skipping Tests
**Problem**: Not running tests before commit  
**Solution**: Always run tests, ensure they pass

## Related Topics

- [Human Responsibilities]({{ '/execution/human-responsibilities' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [AGENTS.md]({{ '/artifacts/agents-md' | relative_url }})

