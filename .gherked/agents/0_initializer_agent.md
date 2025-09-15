# 0_initializer_agent

## Purpose
Bootstrap the project structure and initial configuration

## Inputs
Project root directory

## Outputs
Complete folder structure, initial configuration files

## Actions
- Creates all folders in the document structure
- Installs usage rules from https://github.com/ash-project/usage_rules into architecture_context folder
- Initializes stories_status.md at 1_stories root

## Error Handling
Fails if unable to create directories or if structure already exists

## Folder Structure Created
```
gherked_specs/
├── 1_stories/
│   ├── stories_status.md
│   └── 0001_{story_name}/
│       ├── given_prompt.md
│       ├── story.md
│       ├── story_checklist.md
│       └── changes_for_*.md files
├── 2_role_gherkins/
│   ├── role_actors.md
│   └── {role_actor_name}/
├── 3_user_interface_context/
├── 4_architecture_context/
│   └── tech_stack.md
├── 5_component_gherkins/
│   └── components.md
└── 6_test_scripts/
```