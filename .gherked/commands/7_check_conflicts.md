# /7_check_conflicts

## Description
Run conflict analysis on pending stories to identify inconsistencies

## Actions
1. Reads stories_status.md for "pending" stories
2. For each pending story with completed changes:
   - Executes 7_conflict_checker_agent
   - Analyzes all specifications across layers
   - Generates conflicts_report.md in story folder
3. Summarizes conflicts across all stories

## Prerequisites
- At least some changes_for_*.md files must exist

## Output
- Individual conflicts_report.md per story
- Summary of critical conflicts requiring resolution

## Conflict Categories Checked
- Requirement conflicts between layers
- Missing specifications or gaps
- Inconsistent behaviors across actors/components
- Tech stack violations
- Unimplemented features
- Test coverage gaps