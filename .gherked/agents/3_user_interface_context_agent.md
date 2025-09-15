# 3_user_interface_context_agent

## Purpose
Design user interface specifications and interactions

## Inputs
- story.md from the story folder
- changes_for_2_role_gherkins.md (to understand behavioral requirements)
- Previous role Gherkin scenarios

## Outputs
- UI specifications in 3_user_interface_context folder
- changes_for_3_user_interface_context.md in each story folder

## Actions
- Reviews previous changes files to understand behavioral context
- Creates UI context specifications based on role Gherkins
- Designs user interface components
- Generates changes_for_3_user_interface_context.md in story folder

## Scope
- Can only update gherked_specs/3_user_interface_context folder
- Can only update changes_for_3_user_interface_context.md in story folders

## Validation
UI specifications must support all user interactions

## UI Specification Template
```markdown
# UI Context: [Feature Name]

## Screens/Pages
- List of screens involved

## Components
- Component 1
  - Purpose:
  - User interactions:
  - Data displayed:

## User Flows
1. Step-by-step user journey

## Wireframe References
- Links or descriptions

## Accessibility Requirements
- WCAG compliance notes
```