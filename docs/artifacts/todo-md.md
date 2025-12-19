---
layout: default
title: TODO.md Artifact
---

# TODO.md Artifact

## Overview

The `TODO.md` artifact authorizes specific work items. It tells AI what work is authorized and references the LLD that defines how to do it.

## Purpose

- Authorize specific work items
- Reference LLD sections
- Track work status
- Manage dependencies

## Structure

```markdown
# TODO.md

## TODO

### [Task Description]
- **LLD Reference**: [Section in LLD]
- **Dependencies**: [Other TODO items]
- **Status**: TODO

### [Another Task]
- **LLD Reference**: [Section in LLD]
- **Dependencies**: None
- **Status**: TODO

## DONE

### [Completed Task]
- **LLD Reference**: [Section in LLD]
- **Status**: DONE
```

## Key Principles

### 1. One TODO Item at a Time
- AI executes exactly one TODO item
- Complete before moving to next
- Clear scope boundaries

### 2. Reference LLD
- Each TODO references LLD section
- LLD defines implementation
- TODO authorizes work

### 3. Track Dependencies
- Specify task dependencies
- Execute in correct order
- Manage relationships

### 4. Update Status
- Move TODO to DONE when complete
- Keep status current
- Maintain history

## Example

```markdown
# TODO.md

## TODO

### Create User Registration Endpoint
- **LLD Reference**: LLD.md - "User Registration Service"
- **Dependencies**: None
- **Status**: TODO

### Create User Login Endpoint
- **LLD Reference**: LLD.md - "User Authentication Service"
- **Dependencies**: User Registration Endpoint
- **Status**: TODO

### Create User Profile Endpoint
- **LLD Reference**: LLD.md - "User Profile Service"
- **Dependencies**: User Registration Endpoint
- **Status**: TODO

## DONE

### Create User Model
- **LLD Reference**: LLD.md - "User Entity"
- **Status**: DONE
```

## AI Execution Rules

### When AI Reads TODO.md
1. Find items with Status: TODO
2. Check dependencies (must be DONE)
3. Select one TODO item
4. Read referenced LLD section
5. Execute according to LLD
6. Update status to DONE

### What AI Must Do
- ✅ Execute exactly one TODO item
- ✅ Follow LLD exactly
- ✅ Complete before moving to next
- ✅ Update status when done
- ✅ Commit changes transparently

### What AI Must Not Do
- ❌ Work on multiple TODO items
- ❌ Add features not in LLD
- ❌ Skip dependencies
- ❌ Leave TODO incomplete

## Best Practices

### 1. Break Down Work
- Small, focused TODO items
- Clear scope
- Manageable chunks

### 2. Reference LLD Clearly
- Specific LLD sections
- Clear references
- Easy to find

### 3. Manage Dependencies
- Specify all dependencies
- Order correctly
- Avoid circular dependencies

### 4. Keep Status Current
- Update when complete
- Maintain history
- Track progress

## Related Artifacts

- [AGENTS.md]({{ '/artifacts/agents-md' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})

## Template

See [TODO.md Template]({{ '/templates/TODO' | relative_url }})
