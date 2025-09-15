# /2_role_gherkins_generate_changes

## Description
Generate changes_for_2_role_gherkins.md for pending stories

## Actions
1. Reads stories_status.md for "pending" stories
2. Checks story_checklist.md for uncompleted role_gherkins changes
3. Executes 2_role_gherkins_agent for eligible stories
4. Creates/updates role_actors.md with identified actors
5. Creates actor subfolders in 2_role_gherkins/
6. Generates behavioral specifications in actor/{feature}.md files
7. Creates changes_for_2_role_gherkins.md in story folder
8. Updates story_checklist.md

## Prerequisites
- story.md must exist in the story folder

## Output
- Updated role_actors.md
- New actor folders with feature specifications
- changes_for_2_role_gherkins.md in story folder
- Updated story_checklist.md