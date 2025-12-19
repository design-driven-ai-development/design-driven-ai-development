---
layout: default
title: LLD Markdown
---

# LLD Markdown (Low Level Design)

## Overview

LLD Markdown documents define the exact implementation requirements. They specify business rules, validation, error handling, and all implementation details.

## Purpose

- Define exact implementation requirements
- Specify business rules and logic
- Document validation requirements
- Define error handling
- Specify transaction boundaries
- Document security requirements

## Structure

```markdown
# LLD.md

## Component: [Component Name]

### Business Rules
[Business logic and rules]

### Validation Rules
[Input/output validation requirements]

### Error Handling
[Error scenarios and handling]

### Transaction Boundaries
[Transaction scope and management]

### Security Requirements
[Security constraints and requirements]

### Performance Considerations
[Performance requirements and optimizations]
```

## Key Sections

### Business Rules
The core logic that drives the component's behavior:
- What the component does
- Why it does it
- Business constraints

### Validation Rules
Input and output validation requirements:
- What data is acceptable
- How to validate
- Validation error handling

### Error Handling
Error scenarios and how to handle them:
- Error types
- Error responses
- Recovery strategies

### Transaction Boundaries
Transaction scope and management:
- What operations are atomic
- Rollback strategies
- Consistency requirements

### Security Requirements
Security constraints and requirements:
- Authentication
- Authorization
- Data protection
- Input sanitization

### Performance Considerations
Performance requirements and optimizations:
- Response time targets
- Throughput requirements
- Optimization strategies

## Example

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
- **Username** (if applicable):
  - 3-20 characters
  - Alphanumeric and underscore only
  - Unique check

### Error Handling
- **DuplicateEmailException**: When email already exists
  - HTTP Status: 409 Conflict
  - Message: "Email already registered"
- **InvalidEmailFormatException**: When email format is invalid
  - HTTP Status: 400 Bad Request
  - Message: "Invalid email format"
- **WeakPasswordException**: When password doesn't meet requirements
  - HTTP Status: 400 Bad Request
  - Message: "Password does not meet security requirements"

### Transaction Boundaries
- User creation and profile creation must be atomic
- If profile creation fails, rollback user creation
- Email verification token generation is part of transaction

### Security Requirements
- Passwords must be hashed using bcrypt (cost factor 12)
- Email verification tokens must be cryptographically secure
- Rate limiting: 5 registration attempts per IP per hour
- Input sanitization for all user inputs

### Performance Considerations
- Email uniqueness check should use database index
- Password hashing should be asynchronous
- Cache email domain validation results (TTL: 24 hours)
```

## Best Practices

### 1. Be Specific
- Include exact rules and requirements
- Specify exact values and constraints
- Leave no ambiguity

### 2. Cover Edge Cases
- Document error scenarios
- Specify boundary conditions
- Handle all cases

### 3. Define Constraints
- Specify security requirements
- Define performance requirements
- Set quality standards

### 4. Keep Updated
- Maintain LLD as implementation evolves
- Update based on learnings
- Keep synchronized with code

## LLD for Backend Development

LLD controls:
- API contracts
- Validation rules
- Error handling
- Persistence behavior
- Transaction boundaries

## LLD for UI Development

LLD controls:
- Component hierarchy
- Props and state
- Interaction flows
- Accessibility requirements
- Error and empty states

## Related Artifacts

- [AGENTS.md]({{ '/artifacts/agents-md' | relative_url }})
- [TODO.md]({{ '/artifacts/todo-md' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})

## Template

See [LLD Template]({{ '/templates/lld-template' | relative_url }})

