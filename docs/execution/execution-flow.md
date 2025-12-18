---
layout: default
title: DDAD Execution Flow
---

# DDAD Execution Flow

## Overview

The DDAD execution flow defines the step-by-step process of how humans and AI collaborate to build software using design artifacts.

## The Flow

```
1. Human defines design in LLD Markdown
    ↓
2. Human adds a TODO item referencing the LLD
    ↓
3. AI reads AGENTS.md for constraints
    ↓
4. AI executes the TODO according to the LLD
    ↓
5. AI runs tests or validations
    ↓
6. AI commits changes
    ↓
7. AI moves the TODO item to DONE
    ↓
8. Human reviews and continues
```

## Step-by-Step Details

### Step 1: Human Defines Design in LLD Markdown

**Who**: Human  
**What**: Create or update LLD Markdown document  
**Why**: Define exact implementation requirements

**Activities**:
- Write business rules
- Specify validation requirements
- Define error handling
- Document transaction boundaries
- Specify security requirements

**Output**: LLD Markdown document

### Step 2: Human Adds TODO Item

**Who**: Human  
**What**: Add TODO item to TODO.md  
**Why**: Authorize specific work

**Activities**:
- Create TODO item
- Reference LLD section
- Specify dependencies (if any)
- Set status to TODO

**Output**: Updated TODO.md

### Step 3: AI Reads AGENTS.md

**Who**: AI  
**What**: Read AGENTS.md for constraints  
**Why**: Understand governance and boundaries

**Activities**:
- Read agent definitions
- Understand capabilities
- Note constraints
- Understand interaction patterns

**Output**: AI understands what it can and cannot do

### Step 4: AI Executes TODO According to LLD

**Who**: AI  
**What**: Implement according to LLD  
**Why**: Generate code that matches design

**Activities**:
- Read referenced LLD section
- Understand requirements
- Generate code
- Follow LLD exactly

**Output**: Generated code

### Step 5: AI Runs Tests or Validations

**Who**: AI  
**What**: Run tests and validations  
**Why**: Ensure code works correctly

**Activities**:
- Run unit tests
- Run integration tests
- Validate against LLD
- Check code quality

**Output**: Test results

### Step 6: AI Commits Changes

**Who**: AI  
**What**: Commit changes to repository  
**Why**: Record work transparently

**Activities**:
- Stage changes
- Write commit message
- Reference TODO item
- Commit changes

**Output**: Committed code

### Step 7: AI Moves TODO to DONE

**Who**: AI  
**What**: Update TODO status  
**Why**: Track completion

**Activities**:
- Update TODO.md
- Change status to DONE
- Move item to DONE section

**Output**: Updated TODO.md

### Step 8: Human Reviews Design and Verifies Code

**Who**: Human  
**What**: Review design and verify code conformance  
**Why**: Ensure design correctness and code matches design

**Activities**:
- **Review Design**: Review LLD for correctness (if not already done)
- **Verify Code**: Compare code against LLD section by section
- **Run Tests**: Execute automated tests
- **Check Conformance**: Ensure implementation matches design exactly
- Approve or request changes (to design if needed)
- Continue with next TODO

**Output**: Design reviewed and code verified (or design changes requested)

**Note**: In DDAD, design is reviewed and code is verified. No AI code review tools are used. Code correctness is determined by conformance to design.

## Key Principles

### 1. Explicit Authorization
- Autonomy is explicitly granted via TODO.md
- Never assumed
- Always documented

### 2. One TODO at a Time
- AI executes exactly one TODO item
- Complete before moving to next
- Clear scope boundaries

### 3. Follow LLD Exactly
- Implement strictly according to LLD
- No additions outside LLD
- No omissions from LLD

### 4. Transparent Execution
- All changes committed
- Clear commit messages
- Traceable to TODO and LLD

## Example Flow

### Scenario: Create User Registration Endpoint

1. **Human**: Creates LLD.md section "User Registration Service"
2. **Human**: Adds TODO item "Create User Registration Endpoint" referencing LLD
3. **AI**: Reads AGENTS.md, understands it's a Backend Service Agent
4. **AI**: Reads LLD section, understands requirements
5. **AI**: Generates endpoint code according to LLD
6. **AI**: Runs tests, validates code
7. **AI**: Commits code with message "Implement user registration endpoint (TODO: Create User Registration Endpoint)"
8. **AI**: Updates TODO.md, moves item to DONE
9. **Human**: Reviews code, compares to LLD, approves
10. **Human**: Continues with next TODO item

## Common Patterns

### Pattern 1: Sequential Execution
```
TODO 1 → DONE → TODO 2 → DONE → TODO 3 → DONE
```
Execute TODO items one at a time in order.

### Pattern 2: Parallel Execution
```
TODO 1 → DONE
TODO 2 → DONE  (can execute in parallel if no dependencies)
TODO 3 → DONE
```
Execute independent TODO items in parallel.

### Pattern 3: Dependent Execution
```
TODO 1 → DONE → TODO 2 (depends on 1) → DONE → TODO 3 (depends on 2) → DONE
```
Execute TODO items respecting dependencies.

## Best Practices

### 1. Complete Before Moving On
- Finish one TODO completely
- Don't start next until current is DONE
- Maintain focus

### 2. Review Regularly
- Review after each TODO
- Don't accumulate unreviewed work
- Catch issues early

### 3. Update Artifacts
- Keep LLD current
- Update TODO status
- Maintain artifacts

### 4. Document Decisions
- Record decisions in LLD
- Update artifacts as needed
- Maintain history

## Related Topics

- [Human Responsibilities]({{ '/execution/human-responsibilities' | relative_url }})
- [AI Responsibilities]({{ '/execution/ai-responsibilities' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})

