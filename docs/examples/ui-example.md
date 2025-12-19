---
layout: default
title: UI Development Example
---

# DDAD for UI Development

## Overview

This example demonstrates using DDAD to build a UI component. DDAD controls component hierarchy, props and state, interaction flows, accessibility requirements, and error and empty states.

## Scenario

Build a User Profile editing component.

## Step 1: Create LLD Markdown

```markdown
# LLD.md

## Component: User Profile Editor

### Component Hierarchy
- UserProfileEditor (parent)
  - UserProfileForm (form component)
    - TextInput (name)
    - TextInput (email)
    - TextArea (bio)
  - SaveButton
  - CancelButton

### Props and State
- **Props**: 
  - user: User object
  - onSave: callback function
  - onCancel: callback function
- **State**:
  - formData: { name, email, bio }
  - errors: { name?, email?, bio? }
  - isSubmitting: boolean

### Interaction Flows
1. User clicks Edit → form becomes editable
2. User modifies fields → validation runs on blur
3. User clicks Save → validation runs → API call → success/error
4. User clicks Cancel → form resets to original values

### Validation Rules
- **Name**: Required, 2-50 characters
- **Email**: Required, valid email format
- **Bio**: Optional, max 500 characters

### Error States
- Validation errors shown below each field
- API errors shown at top of form
- Network errors show retry option

### Empty States
- Loading: Show spinner
- No user: Show "No profile found" message

### Accessibility Requirements
- All inputs have labels
- Error messages associated with inputs (aria-describedby)
- Keyboard navigation supported
- Focus management on save/cancel
```

## Step 2: Create TODO Item

```markdown
# TODO.md

## TODO

### Create User Profile Editor Component
- **LLD Reference**: LLD.md - "User Profile Editor"
- **Dependencies**: None
- **Status**: TODO
```

## Step 3: AI Execution

AI reads:
1. **AGENTS.md**: Understands it's a Frontend Component Agent
2. **TODO.md**: Finds authorized work item
3. **LLD.md**: Reads "User Profile Editor" section

AI generates:
- Component code with hierarchy
- Props and state management
- Validation logic
- Interaction handlers
- Error and empty states
- Accessibility attributes
- Component tests

AI commits:
```
Implement user profile editor component (TODO: Create User Profile Editor Component)
```

AI updates TODO.md:
```markdown
## DONE

### Create User Profile Editor Component
- **LLD Reference**: LLD.md - "User Profile Editor"
- **Status**: DONE
```

## Step 4: Human Review and Verification

Human reviews design and verifies code:
- ✅ **Design Review**: LLD is correct and complete (if not already reviewed)
- ✅ **Code Verification**: Component hierarchy matches LLD
- ✅ Props and state match LLD exactly
- ✅ Interaction flows implemented as specified
- ✅ Validation rules applied correctly
- ✅ Error states match LLD
- ✅ Accessibility requirements met
- ✅ Tests pass

**Note**: In DDAD, design is reviewed and code is verified. No AI code review tools are used. Code correctness is determined by conformance to design.

## What DDAD Controlled

- ✅ **Component Hierarchy**: Structure from LLD
- ✅ **Props and State**: Exact definition from LLD
- ✅ **Interaction Flows**: Flows from LLD
- ✅ **Accessibility**: Requirements from LLD
- ✅ **Error States**: States from LLD

## Key Takeaway

> **Design artifacts (LLD) defined UI behavior.  
> AI executed design exactly as specified.**

## Related Topics

- [Backend Example]({{ '/examples/backend-example' | relative_url }})
- [Execution Flow]({{ '/execution/execution-flow' | relative_url }})
- [LLD Markdown]({{ '/artifacts/lld-markdown' | relative_url }})

