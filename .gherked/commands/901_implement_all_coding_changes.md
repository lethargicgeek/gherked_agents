# /901_implement_all_coding_changes

## Description
Implement all coding changes to align the codebase with the gherked specifications. This command reads all documentation from gherked_specs and applies the necessary code modifications.

## Actions
1. Scan gherked_specs directory for all pending/complete stories
2. For each story with complete documentation:
   - Read story_*.md for requirements and acceptance criteria
   - Parse changes_for_role_gherkins.md for behavior specifications
   - Review changes_for_user_interface_context.md for UI implementations
   - Analyze changes_for_architecture_context.md for structural changes
   - Process changes_for_component_gherkins.md for component updates
   - Extract changes_for_test_scripts.md for test implementations
   - Consider conflicts_report.md to avoid breaking changes
3. Generate implementation plan based on documentation
4. Execute code changes in order:
   - Create new directories and files as specified
   - Modify existing files following documented patterns
   - Implement interfaces and contracts from Gherkins
   - Add UI components per specifications
   - Create/update tests to match test scripts
   - Apply architectural patterns as documented
5. Validate each change against Gherkin scenarios
6. Run existing tests to ensure no regressions
7. Update story_checklist.md marking implementation steps complete
8. Update stories_status.md to "implemented" for completed stories

## Prerequisites
- Complete documentation set in gherked_specs for each story
- All agents 1-7 must have been run successfully
- Backup of current codebase recommended

## Usage
Run after documentation generation (commands 1-7 or 900) to implement all pending code changes

## Error Handling
- Creates file backups before modifications
- Validates syntax after each file change
- Rolls back individual file changes on errors
- Continues with next story if one fails
- Generates detailed error log with:
  - Failed file operations
  - Syntax errors encountered
  - Unmet dependencies
  - Conflict resolutions needed

## Output
- Modified/created source code files
- Updated test files
- Implementation summary report including:
  - Files created (count and paths)
  - Files modified (count and paths)
  - Tests added/updated
  - Gherkin scenarios satisfied
  - Any unresolved issues
- Updated story_checklist.md with completed items
- Updated stories_status.md with "implemented" status
- Detailed change log for version control

## Validation
- Ensures all Gherkin scenarios have corresponding implementations
- Verifies UI components match specifications
- Confirms architectural patterns are followed
- Validates test coverage for new features