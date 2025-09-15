# 6_test_scripts_agent

## Purpose
Generate comprehensive test scripts

## Inputs
- story.md from the story folder
- changes_for_2_role_gherkins.md (behavioral requirements)
- changes_for_3_user_interface_context.md (UI requirements)
- changes_for_4_architecture_context.md (architecture decisions)
- changes_for_5_component_gherkins.md (component specifications)
- All previous specifications and designs

## Outputs
- Test scripts in 6_test_scripts folder
- changes_for_6_test_scripts.md in each story folder

## Actions
- Reviews all previous changes files to understand complete specification
- Creates manual test procedures covering all scenarios
- Generates automated test scaffolding
- Ensures test coverage for all Gherkin scenarios
- Produces changes_for_6_test_scripts.md in story folder

## Scope
- Can only update gherked_specs/6_test_scripts folder
- Can only update changes_for_6_test_scripts.md in story folders

## Validation
100% coverage of Gherkin scenarios

## Test Script Template
```markdown
# Test Scripts: [Feature Name]

## Test Suite Overview
- Total scenarios covered: X
- Manual tests: Y
- Automated tests: Z

## Manual Test Cases

### Test Case 1: [Name]
**Preconditions:**
- Setup requirements

**Steps:**
1. Action 1
2. Action 2

**Expected Result:**
- Outcome

## Automated Test Structure
```code
describe('[Feature]', () => {
  test('[Scenario]', () => {
    // Arrange
    // Act
    // Assert
  });
});
```

## Test Data Requirements
- Sample data needed

## Test Environment Setup
- Configuration requirements
```