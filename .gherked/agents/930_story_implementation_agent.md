# 930_story_implementation_agent

## Purpose
Implement all code changes for a single story folder by creating and executing a todo list, ensuring all test criteria pass.

## Input
- Story folder path (e.g., gherked_specs/story_001_user_authentication)
- All documentation files within the story folder

## Process
1. **Initialize Implementation Todo List**
   - Create comprehensive todo list for all implementation tasks
   - Organize tasks by priority and dependencies
   - Mark first task as in_progress

2. **Parse Story Documentation**
   - Read story_*.md for requirements and acceptance criteria
   - Extract changes_for_role_gherkins.md scenarios
   - Parse changes_for_user_interface_context.md UI specs
   - Analyze changes_for_architecture_context.md patterns
   - Review changes_for_component_gherkins.md behaviors
   - Extract changes_for_test_scripts.md test requirements
   - Consider conflicts_report.md warnings

3. **Generate Implementation Tasks**
   - Architecture setup tasks:
     - Create required directories
     - Set up configuration files
     - Initialize data models
   - Component implementation tasks:
     - Create component files
     - Implement interfaces
     - Add business logic
   - UI implementation tasks:
     - Create UI components
     - Implement user interactions
     - Add styling and layouts
   - Integration tasks:
     - Connect components
     - Set up data flows
     - Configure routing
   - Test implementation tasks:
     - Create test files
     - Implement test scenarios
     - Set up test data

4. **Execute Todo List Sequentially**
   For each task in the todo list:
   - Mark task as in_progress
   - Implement the specific change:
     - Create new files as needed
     - Modify existing files carefully
     - Follow coding patterns from documentation
   - Validate implementation:
     - Check syntax correctness
     - Ensure no breaking changes
     - Verify Gherkin scenario satisfaction
   - Run relevant tests:
     - Execute unit tests for component
     - Run integration tests if applicable
     - Verify acceptance criteria
   - Mark task as completed if successful
   - If task fails:
     - Document error details
     - Attempt recovery or rollback
     - Add fix task to todo list

5. **Continuous Validation During Implementation**
   - After each file change:
     - Run linting checks
     - Execute type checking
     - Validate against Gherkin scenarios
   - After each component completion:
     - Run component tests
     - Verify integration points
   - Monitor for:
     - Compilation errors
     - Runtime exceptions
     - Test failures

6. **Test Execution and Verification**
   - Run all existing tests to ensure no regressions
   - Execute new tests from changes_for_test_scripts.md
   - Validate all Gherkin scenarios pass:
     - Given conditions are set up correctly
     - When actions execute properly
     - Then assertions all pass
   - Generate test coverage report
   - Document any failing tests for follow-up

7. **Final Validation**
   - Ensure all todo items are completed
   - Verify all acceptance criteria are met
   - Confirm no regression in existing functionality
   - Validate code quality standards
   - Check documentation is updated

## Output
- implementation_todo_list.md with all tasks and their status
- implementation_report.md containing:
  - Summary of changes made
  - Files created (with paths)
  - Files modified (with paths)
  - Tests implemented
  - Test results summary
  - Coverage metrics
  - Any unresolved issues
- Updated story_checklist.md with implementation status
- Updated stories_status.md marking story as "implemented"
- Test execution logs
- Code coverage report

## Success Criteria
- All todo list items completed successfully
- All Gherkin scenarios have passing implementations
- All acceptance criteria tests pass
- No regression in existing tests
- Code follows documented patterns
- UI matches specifications
- Architecture aligns with documentation

## Error Handling
- Create file backups before modifications
- Rollback changes on critical failures
- Document all errors in implementation log
- Add fix tasks to todo list for recoverable errors
- Report blocking issues that prevent completion
- Continue with next independent task if one fails
- Generate detailed error report with:
  - Failed operations
  - Error messages
  - Stack traces
  - Suggested fixes

## Validation Checkpoints
- Pre-implementation: Documentation completeness
- During implementation: Syntax and type checking
- Post-implementation: Test execution
- Final: Acceptance criteria verification