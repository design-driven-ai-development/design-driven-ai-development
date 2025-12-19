---
layout: default
title: DDAD Artifact Model
---

# DDAD Artifact Model

## Overview

DDAD is implemented using a small, explicit set of repository artifacts that govern AI execution.

## The Artifact Flow

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

## Artifact Descriptions

### README.md
**Purpose**: Explains the project purpose and context

**Contains**:
- Project overview
- Purpose and goals
- High-level architecture
- Getting started guide

**Role**: Provides context for all other artifacts

### AGENTS.md
**Purpose**: Governs AI behavior and constraints

**Contains**:
- AI agent definitions
- Capabilities and limitations
- Constraints and boundaries
- Interaction patterns

**Role**: Defines what AI can and cannot do

### TODO.md
**Purpose**: Authorizes specific work items

**Contains**:
- Work items (TODO)
- References to LLD sections
- Dependencies between items
- Status tracking (TODO → DONE)

**Role**: Authorizes AI to work on specific tasks

### LLD Markdown
**Purpose**: Defines exact implementation requirements

**Contains**:
- Business rules
- Validation rules
- Error handling
- Transaction boundaries
- Security requirements
- Performance considerations

**Role**: Specifies exactly how to implement

## Artifact Relationships

```
README.md (context)
    ↓
AGENTS.md (governance)
    ↓
TODO.md (authorization)
    ↓ references
LLD Markdown (specification)
    ↓
Code + Tests (implementation)
```

## Key Principles

### 1. Explicit Over Implicit
- All requirements are explicit
- No hidden assumptions
- Clear and unambiguous

### 2. Version Controlled
- All artifacts in version control
- History preserved
- Changes tracked

### 3. Human Authored
- Humans create artifacts
- AI reads and executes
- Clear separation of concerns

### 4. Single Source of Truth
- Each requirement in one place
- No duplication
- Easy to maintain

## Artifact Quality

### Good Artifacts
- ✅ Clear and specific
- ✅ Complete and comprehensive
- ✅ Structured and organized
- ✅ Maintained and updated

### Poor Artifacts
- ❌ Vague or ambiguous
- ❌ Incomplete or missing details
- ❌ Unstructured or disorganized
- ❌ Outdated or inconsistent

## Best Practices

### 1. Start with README.md
- Establish project context
- Define purpose and goals
- Set the foundation

### 2. Define AGENTS.md Early
- Establish governance
- Set boundaries
- Guide AI behavior

### 3. Create LLD Before TODO
- Design before work
- Specify before authorize
- Plan before execute

### 4. Keep Artifacts Synchronized
- Update together
- Maintain consistency
- Version control changes

## Related Topics

- [AGENTS.md]({{ '/artifacts/agents-md' | relative_url }})
- [TODO.md]({{ '/artifacts/todo-md' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})

