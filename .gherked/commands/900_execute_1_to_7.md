# /900_execute_1_to_7

## Description
Execute agents 1 through 7 in sequence for a complete story generation workflow.  Play a tune to get the attention of the claude code user if claude code needs input. 

## Actions
1. Executes 1_stories_agent to generate story documentation
2. Executes 2_role_gherkins_agent for role-based Gherkin scenarios
3. Executes 3_user_interface_context_agent for UI context documentation
4. Executes 4_architecture_context_agent for architecture documentation
5. Executes 5_component_gherkins_agent for component-level Gherkins
6. Executes 6_test_scripts_agent for test script generation
7. Executes 7_conflict_checker_agent to check for conflicts

## Usage
Run to execute the complete workflow from story generation to conflict checking

## Error Handling
- Stops execution if any agent fails
- Reports which agent failed and error details
- Preserves partial progress from successfully completed agents

## Output
- story_*.md file from agent 1
- changes_for_*.md files from agents 2-6
- conflicts_report.md from agent 7
- Updated story_checklist.md and stories_status.md