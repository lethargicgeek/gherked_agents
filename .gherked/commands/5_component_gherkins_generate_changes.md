# /5_component_gherkins_generate_changes

## Description
Generate changes_for_5_component_gherkins.md for pending stories

## Actions
1. Reads stories_status.md for "pending" stories
2. Checks story_checklist.md for uncompleted component gherkins changes
3. Executes 5_component_gherkins_agent for eligible stories
4. Creates/updates components.md with identified components
5. Creates component subfolders in 5_component_gherkins/
6. Generates feature specifications in component/{feature}.md files with all behaviors
7. Creates changes_for_5_component_gherkins.md in story folder
8. Updates story_checklist.md

## Prerequisites
- Architecture context must be defined

## Output
- Updated components.md
- New component folders with feature specifications
- changes_for_5_component_gherkins.md in story folder
- Updated story_checklist.md