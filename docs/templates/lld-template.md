---
title: Lld Template
parent: Templates
---
# LLD.md (Low Level Design) Template

Use this template to create detailed low-level design specifications.

## Component: [Component Name]

### Business Rules
[Business logic and rules that drive this component]

Example:
1. [Rule 1]
2. [Rule 2]
3. [Rule 3]

### Validation Rules
[Input/output validation requirements]

Example:
- **Field Name**: 
  - [Validation requirement 1]
  - [Validation requirement 2]

### Error Handling
[Error scenarios and how they should be handled]

Example:
- **ExceptionName**: 
  - HTTP Status: [Status code] (for APIs)
  - Message: "[Error message]"
  - Recovery: [How to handle]

### Transaction Boundaries
[Transaction scope and management - for backend]

Example:
- [Operation 1] and [Operation 2] must be atomic
- If [Operation 2] fails, rollback [Operation 1]

### Security Requirements
[Security constraints and requirements]

Example:
- [Security requirement 1]
- [Security requirement 2]

### Performance Considerations
[Performance requirements and optimizations]

Example:
- [Performance requirement]
- [Optimization strategy]

## Component: [Another Component Name]

[Repeat structure for each component]

## Notes

[Any additional notes about the design]
