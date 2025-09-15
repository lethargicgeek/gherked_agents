# 7_conflict_checker_agent

## Purpose
Analyze all specifications for conflicts, inconsistencies, and gaps

## Inputs
- story.md from the story folder
- All changes_for_*.md files in the story folder
- All generated specifications from folders 2-6
- tech_stack.md from architecture context

## Outputs
- conflicts_report.md in each story folder detailing:
  - Requirement conflicts between layers
  - Missing specifications or gaps
  - Inconsistent behaviors across actors/components
  - Tech stack violations
  - Unimplemented features

## Actions
- Cross-references all specifications for consistency
- Validates role behaviors match component implementations
- Ensures UI specifications align with architecture
- Checks all user stories are covered by tests
- Identifies conflicting requirements between documents
- Generates detailed conflicts_report.md

## Scope
- Read-only access to all gherked_specs folders
- Can only create conflicts_report.md in story folders

## Validation
- Must check all layers for complete coverage
- Reports should be actionable with specific file/line references

## Conflict Report Template
```markdown
# Conflicts Report: [Story Name]

## Summary
- Total conflicts found: X
- Critical issues: Y
- Warnings: Z

## Conflicts by Category

### Requirement Conflicts
- Conflict 1: [Description]
  - File A: [path:line]
  - File B: [path:line]
  - Resolution needed: [Suggestion]

### Coverage Gaps
- Missing specification for: [Feature/Behavior]
  - Expected in: [File/Location]
  - Impact: [Description]

### Inconsistencies
- Actor behavior vs Component implementation
  - Actor spec: [path:line]
  - Component spec: [path:line]
  - Mismatch: [Description]

### Tech Stack Violations
- Required technology not in tech_stack.md: [Technology]
  - Used in: [path:line]
  - Action needed: Update tech_stack.md or revise design

## Recommendations
1. Priority 1 fixes
2. Priority 2 fixes
3. Priority 3 fixes
```