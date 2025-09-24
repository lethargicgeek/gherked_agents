# /8_implement_code_change

## Description
Implement code changes based on all documentation generated in gherked_specs for pending stories

## Actions
1. Reads stories_status.md for "pending" or "complete" stories
2. For each story, reads all generated documentation:
   - story_*.md for requirements
   - changes_for_role_gherkins.md for role-based scenarios
   - changes_for_user_interface_context.md for UI requirements
   - changes_for_architecture_context.md for architectural changes
   - changes_for_component_gherkins.md for component specifications
   - changes_for_test_scripts.md for test requirements
   - conflicts_report.md for potential issues to avoid
3. Implements code changes based on the documentation:
   - Creates new files as specified
   - Modifies existing files following the documented changes
   - Ensures all Gherkin scenarios are satisfied
   - Implements test scripts as specified
4. Validates implementation against all documentation
5. Updates story status to "implemented" upon successful completion

## Usage
Run after all documentation has been generated (agents 1-7) to implement the actual code changes

## Prerequisites
- All changes_for_*.md files must exist for the story
- conflicts_report.md should be reviewed before implementation

## Error Handling
- Creates backup of modified files before changes
- Reports specific implementation failures
- Rolls back changes if critical errors occur
- Preserves partial progress where possible

## Output
- Implemented code changes in the project
- Implementation report documenting all changes made
- Updated stories_status.md with "implemented" status
- List of files created/modified