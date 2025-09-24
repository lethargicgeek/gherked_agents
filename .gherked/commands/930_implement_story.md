# /930_implement_story

## Description
Create a todo list for implementing all changes in a single story folder, then execute the implementation with test verification

## Actions
1. Accept story folder path as parameter
2. Execute 930_story_implementation_agent on the specified folder
3. Create implementation todo list based on story documentation
4. Execute each todo item sequentially:
   - Implement code changes
   - Validate against Gherkin scenarios
   - Run tests to verify correctness
5. Track progress through todo list updates
6. Generate comprehensive implementation report
7. Update story status to "implemented" upon success

## Usage
Run with a specific story folder path to implement all its documented changes

## Parameters
- story_folder: Path to the story folder in gherked_specs (e.g., "gherked_specs/story_001_user_authentication")

## Prerequisites
- Complete documentation in story folder (all changes_for_*.md files)
- Story marked as "complete" or "pending" in stories_status.md
- Development environment properly configured
- Test framework available and configured

## Execution Flow
1. Parse all documentation files in story folder
2. Generate comprehensive todo list
3. Start executing todos in sequence
4. Validate each implementation step
5. Run tests after each component
6. Update todo status in real-time
7. Generate final report

## Error Handling
- Backs up files before modification
- Attempts rollback on critical errors
- Documents all errors in implementation log
- Adds fix tasks to todo for recoverable issues
- Continues with independent tasks when possible
- Stops execution on blocking errors

## Output
- implementation_todo_list.md with task status tracking
- implementation_report.md with detailed results
- Updated source code files
- New test files as specified
- Test execution results
- Coverage report
- Updated story_checklist.md
- Updated stories_status.md with "implemented" status

## Success Indicators
- All todos marked as completed
- All tests passing (new and existing)
- All Gherkin scenarios satisfied
- No compilation or runtime errors
- Code quality checks pass