---
layout: default
title: Getting Started with DDAD
---

# Getting Started with DDAD

## Quick Start

### 1. Create README.md
Start with a README.md that explains your project:
```markdown
# My Project

## Purpose
[What this project does]

## Architecture
[High-level architecture]
```

### 2. Create AGENTS.md
Define AI agents and governance:
```markdown
# AGENTS.md

## Agent Definitions

### Backend Service Agent
- **Role**: Generate backend service implementations
- **Capabilities**: Generate REST APIs, implement business logic
- **Constraints**: Must follow LLD exactly, no additions outside LLD
```

### 3. Create LLD.md
Write your first Low Level Design:
```markdown
# LLD.md

## Component: [Your Component]

### Business Rules
[Your business rules]

### Validation Rules
[Your validation rules]
```

### 4. Create TODO.md
Authorize your first work item:
```markdown
# TODO.md

## TODO

### [Your Task]
- **LLD Reference**: LLD.md - "[Your Component]"
- **Dependencies**: None
- **Status**: TODO
```

### 5. Let AI Execute
AI will:
1. Read AGENTS.md for constraints
2. Read TODO.md for authorization
3. Read LLD.md for requirements
4. Generate code according to LLD
5. Commit changes
6. Update TODO status

### 6. Review
Review the generated code against LLD and approve.

## Key Principles

1. **Design First**: Create LLD before TODO
2. **Authorize Explicitly**: Use TODO.md to authorize work
3. **Follow Exactly**: AI follows LLD exactly
4. **Review Always**: Review all generated code

## Next Steps

- [Team Adoption]({{ '/adoption/team-adoption' | relative_url }})
- [Examples]({{ '/examples/backend-example' | relative_url }})
- [Templates]({{ '/templates/AGENTS' | relative_url }})

