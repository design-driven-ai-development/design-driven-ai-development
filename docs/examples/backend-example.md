---
layout: default
title: Backend Development Example
---

# DDAD for Backend Development

## Overview

This example demonstrates using DDAD to build a backend service. DDAD controls API contracts, validation rules, error handling, persistence behavior, and transaction boundaries.

## Scenario

Build a User Registration API endpoint.

## Step 1: Create LLD Markdown

```markdown
# LLD.md

## Component: User Registration Service

### Business Rules
1. Email must be unique across the system
2. Password must meet complexity requirements:
   - Minimum 8 characters
   - At least one uppercase letter
   - At least one number
   - At least one special character
3. User account is inactive until email verification
4. Registration creates a default user profile

### Validation Rules
- **Email**: 
  - Format validation (RFC 5322)
  - Domain validation (not disposable email)
  - Uniqueness check against database
- **Password**:
  - Complexity requirements (see Business Rules)
  - Not in common password list

### Error Handling
- **DuplicateEmailException**: HTTP 409 Conflict
- **InvalidEmailFormatException**: HTTP 400 Bad Request
- **WeakPasswordException**: HTTP 400 Bad Request

### Transaction Boundaries
- User creation and profile creation must be atomic
- If profile creation fails, rollback user creation

### Security Requirements
- Passwords hashed using bcrypt (cost factor 12)
- Rate limiting: 5 attempts per IP per hour
```

## Step 2: Create TODO Item

```markdown
# TODO.md

## TODO

### Create User Registration Endpoint
- **LLD Reference**: LLD.md - "User Registration Service"
- **Dependencies**: None
- **Status**: TODO
```

## Step 3: AI Execution

AI reads:
1. **AGENTS.md**: Understands it's a Backend Service Agent
2. **TODO.md**: Finds authorized work item
3. **LLD.md**: Reads "User Registration Service" section

AI generates:
- REST endpoint code
- Validation logic
- Error handling
- Transaction management
- Unit tests

AI commits:
```
Implement user registration endpoint (TODO: Create User Registration Endpoint)
```

AI updates TODO.md:
```markdown
## DONE

### Create User Registration Endpoint
- **LLD Reference**: LLD.md - "User Registration Service"
- **Status**: DONE
```

## Step 4: Human Review and Verification

Human reviews design and verifies code:
- ✅ **Design Review**: LLD is correct and complete (if not already reviewed)
- ✅ **Code Verification**: Code matches LLD requirements exactly
- ✅ Validation rules implemented as specified
- ✅ Error handling matches LLD
- ✅ Tests pass
- ✅ Transaction boundaries respected

**Note**: In DDAD, design is reviewed and code is verified. No AI code review tools are used. Code correctness is determined by conformance to design.

## What DDAD Controlled

- ✅ **API Contract**: Endpoint structure from LLD
- ✅ **Validation Rules**: Exact rules from LLD
- ✅ **Error Handling**: Specific errors from LLD
- ✅ **Persistence**: Transaction boundaries from LLD
- ✅ **Security**: Requirements from LLD

## Key Takeaway

> **Design artifacts (LLD) defined behavior.  
> AI executed design exactly as specified.**

## Related Topics

- [UI Example]({{ '/examples/ui-example' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})

