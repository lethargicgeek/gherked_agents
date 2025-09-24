# 920_documentation_review_agent

## Purpose
Review a single story folder to verify that gherked_specs documentation has been properly updated based on the story's contents, creating a todo list to track review progress.

## Input
- Story folder path (e.g., gherked_specs/story_001_user_authentication)
- Story documentation files within the folder

## Process
1. **Initialize Review Todo List**
   - Create todo list for documentation review tasks
   - Add items for each required documentation file

2. **Scan Story Folder Contents**
   - Identify story_*.md file
   - List all changes_for_*.md files present
   - Check for conflicts_report.md
   - Note any additional documentation files

3. **Verify Required Documentation**
   - ✓ story_*.md exists and contains proper structure
   - ✓ changes_for_role_gherkins.md present with Gherkin scenarios
   - ✓ changes_for_user_interface_context.md has UI specifications
   - ✓ changes_for_architecture_context.md includes architectural decisions
   - ✓ changes_for_component_gherkins.md defines component behaviors
   - ✓ changes_for_test_scripts.md contains test specifications
   - ✓ conflicts_report.md addresses potential issues

4. **Content Validation for Each Document**
   - Check story_*.md for:
     - Clear requirements
     - Acceptance criteria
     - User stories in proper format
   - Validate changes_for_role_gherkins.md for:
     - Properly formatted Gherkin scenarios
     - Complete Given/When/Then statements
     - Coverage of all user roles
   - Review changes_for_user_interface_context.md for:
     - UI component specifications
     - User interaction flows
     - Accessibility considerations
   - Examine changes_for_architecture_context.md for:
     - System design decisions
     - Integration points
     - Data flow documentation
   - Verify changes_for_component_gherkins.md for:
     - Component-level behaviors
     - Interface definitions
     - State management
   - Check changes_for_test_scripts.md for:
     - Test coverage mapping
     - Test data requirements
     - Expected outcomes

5. **Cross-Reference Validation**
   - Ensure all Gherkin scenarios align with story requirements
   - Verify UI specs match user stories
   - Confirm architecture supports all features
   - Check component specs implement all scenarios
   - Validate tests cover all acceptance criteria

6. **Update Todo List Progress**
   - Mark each review item as completed
   - Add new todos for any missing or incomplete documentation
   - Flag items requiring fixes or updates

7. **Generate Review Report**
   - Documentation completeness score
   - List of missing documents
   - Content quality issues found
   - Inconsistencies between documents
   - Recommendations for improvements

## Output
- review_todo_list.md with all review tasks
- documentation_review_report.md containing:
  - Completeness assessment
  - Quality evaluation
  - Missing elements
  - Inconsistencies found
  - Recommended actions
- Updated story_checklist.md reflecting review status

## Success Criteria
- All required documentation files present
- Content properly structured in each file
- Cross-references between documents are consistent
- No gaps in documentation coverage
- Todo list accurately reflects review status

## Error Handling
- Report missing required files
- Flag malformed document structures
- Identify empty or placeholder content
- Note circular or conflicting references
- Create todos for all issues requiring resolution