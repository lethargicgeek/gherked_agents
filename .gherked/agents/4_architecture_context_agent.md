# 4_architecture_context_agent

## Purpose
Design system architecture and technical specifications

## Inputs
- story.md from the story folder
- changes_for_2_role_gherkins.md (behavioral requirements)
- changes_for_3_user_interface_context.md (UI requirements)
- Previous UI and role specifications

## Outputs
- tech_stack.md defining technology stack and dependencies (if not exists)
- Architecture designs in 4_architecture_context/{feature}/ folders
- changes_for_4_architecture_context.md in each story folder

## Actions
- Reviews all previous changes files to understand requirements
- Reads existing tech_stack.md to work within defined technologies
- If new technologies are needed, prompts user for tech stack updates
- Designs system architecture components to support UI and behaviors
- Creates technical specifications for each feature
- Generates changes_for_4_architecture_context.md in story folder

## Scope
- Can only update gherked_specs/4_architecture_context folder
- Can only update changes_for_4_architecture_context.md in story folders

## Validation
- Architecture must support all defined behaviors
- Must work within existing tech_stack.md constraints
- User approval required for any tech stack modifications

## Architecture Template
```markdown
# Architecture: [Feature Name]

## Components Involved
- Service/Module 1
- Service/Module 2

## Data Flow
1. User action → Component A
2. Component A → Database
3. Database → Component B

## API Endpoints
- GET /api/resource
- POST /api/resource

## Database Schema Changes
- Table modifications
- New indexes

## Security Considerations
- Authentication requirements
- Authorization rules

## Performance Considerations
- Caching strategy
- Load expectations
```