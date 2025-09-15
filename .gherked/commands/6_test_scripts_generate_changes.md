# /6_test_scripts_generate_changes

## Description
Generate changes_for_6_test_scripts.md for pending stories

## Actions
1. Reads stories_status.md for "pending" stories
2. Checks story_checklist.md for uncompleted test scripts changes
3. Executes 6_test_scripts_agent for eligible stories
4. Creates changes_for_6_test_scripts.md in story folder
5. Updates story_checklist.md

## Prerequisites
- All previous specifications must exist

## Output
- Test scripts in 6_test_scripts folder
- changes_for_6_test_scripts.md in story folder
- Updated story_checklist.md