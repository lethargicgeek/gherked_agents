# /3_user_interface_context_generate_changes

## Description
Generate changes_for_3_user_interface_context.md for pending stories

## Actions
1. Reads stories_status.md for "pending" stories
2. Checks story_checklist.md for uncompleted UI context changes
3. Executes 3_user_interface_context_agent for eligible stories
4. Creates changes_for_3_user_interface_context.md in story folder
5. Updates story_checklist.md

## Prerequisites
- story.md and role_gherkins must exist

## Output
- UI specifications in 3_user_interface_context folder
- changes_for_3_user_interface_context.md in story folder
- Updated story_checklist.md