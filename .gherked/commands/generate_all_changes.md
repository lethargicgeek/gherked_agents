# /generate_all_changes

## Description
Generate all missing changes files for pending stories in sequence

## Actions
1. Reads stories_status.md for "pending" stories
2. For each pending story, checks story_checklist.md
3. Executes agents in sequence for missing changes:
   - 2_role_gherkins_agent
   - 3_user_interface_context_agent
   - 4_architecture_context_agent
   - 5_component_gherkins_agent
   - 6_test_scripts_agent
4. Runs 7_conflict_checker_agent after all changes generated
5. Updates story_checklist.md after each generation
6. Updates stories_status.md to "complete" when all changes generated

## Usage
Run to automatically generate all documentation for pending stories

## Error Handling
- Stops processing a story if any agent fails
- Reports which stories completed and which had errors

## Output
- Complete set of changes_for_*.md files for each story
- conflicts_report.md for each story
- Updated status tracking