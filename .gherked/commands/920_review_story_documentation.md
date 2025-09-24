# /920_review_story_documentation

## Description
Review a single story folder's documentation in gherked_specs to ensure all required files are present and properly updated

## Actions
1. Accept story folder path as input
2. Execute 920_documentation_review_agent on the specified folder
3. Create review todo list for tracking review progress
4. Validate presence of all required documentation files
5. Check content quality and completeness
6. Cross-reference documents for consistency
7. Generate comprehensive review report
8. Update story_checklist.md with review findings

## Usage
Run with a specific story folder path to review its documentation completeness and quality

## Parameters
- story_folder: Path to the story folder in gherked_specs (e.g., "gherked_specs/story_001_user_authentication")

## Prerequisites
- Story folder must exist in gherked_specs
- At least story_*.md file should be present

## Error Handling
- Reports if story folder doesn't exist
- Lists all missing required documentation
- Flags incomplete or malformed content
- Creates todos for all issues found

## Output
- review_todo_list.md with all review tasks and their status
- documentation_review_report.md with detailed findings
- Updated story_checklist.md reflecting documentation status
- List of recommended actions to complete documentation