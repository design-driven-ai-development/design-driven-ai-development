---
layout: default
title: AGENTS.md Artifact
---

# AGENTS.md Artifact

## Overview

The `AGENTS.md` artifact governs AI behavior and defines constraints. It specifies what AI agents can and cannot do.

## Purpose

- Define AI agent roles and responsibilities
- Specify agent capabilities and constraints
- Establish agent interaction patterns
- Govern AI behavior

## Structure

```markdown
# AGENTS.md

## Agent Definitions

### [Agent Name]
- **Role**: [Primary responsibility]
- **Capabilities**: [What this agent can do]
- **Constraints**: [Limitations]
- **Inputs**: [Required artifacts]
- **Outputs**: [Generated artifacts]

## Agent Interactions

[How agents work together]

## Governance Rules

[Rules that all agents must follow]
```

## Key Sections

### Agent Definitions
Define each AI agent:
- What it can do
- What it cannot do
- What it needs as input
- What it produces as output

### Agent Interactions
Specify how agents work together:
- Order of execution
- Data flow between agents
- Coordination patterns

### Governance Rules
Rules that all agents must follow:
- Code quality standards
- Testing requirements
- Documentation requirements
- Security constraints

## Example

```markdown
# AGENTS.md

## Agent Definitions

### Backend Service Agent
- **Role**: Generate backend service implementations
- **Capabilities**: 
  - Generate REST API endpoints from LLD
  - Implement business logic
  - Create repository layer code
  - Generate unit tests
- **Constraints**:
  - Must follow LLD exactly
  - Cannot add features not in LLD
  - Must include error handling as specified
- **Inputs**: 
  - LLD Markdown (specific section)
  - TODO.md item
- **Outputs**:
  - Service implementation
  - Repository implementation
  - Unit tests

## Governance Rules

1. All code must follow project coding standards
2. All public methods must have documentation
3. All code must have unit tests (80%+ coverage)
4. No code outside TODO scope
5. All changes must be committed with clear messages
```

## Best Practices

### 1. Be Explicit
- Clearly define capabilities
- Explicitly state constraints
- Leave no ambiguity

### 2. Set Boundaries
- Define what agents cannot do
- Prevent scope creep
- Maintain control

### 3. Reference Artifacts
- Link to LLD sections
- Reference TODO items
- Connect to README

### 4. Update Regularly
- Refine based on experience
- Add constraints as needed
- Improve governance

## Common Constraints

### Scope Constraints
- Work only on authorized TODO items
- No speculative changes
- No unrelated modifications

### Quality Constraints
- Follow coding standards
- Include tests
- Add documentation
- Handle errors properly

### Process Constraints
- Commit changes transparently
- Update TODO status
- Run tests before committing

## Related Artifacts

- [TODO.md]({{ '/artifacts/todo-md' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})
- [Artifact Model]({{ '/artifacts/artifact-model' | relative_url }})

## Template

See [AGENTS.md Template]({{ '/templates/AGENTS' | relative_url }})
