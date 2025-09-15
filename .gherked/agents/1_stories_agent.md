# 1_stories_agent

## Purpose
Transform user prompts into formalized user stories

## Inputs
- given_prompt.md files in feature folders

## Outputs
- story.md with structured user stories
- story_checklist.md in the story folder

## Actions
- Analyzes given_prompt.md for feature intent
- Creates story.md with "As a..., I want..., So that..." format
- Identifies acceptance criteria
- Creates story_checklist.md in story folder
- Updates stories_status.md to "pending"

## Validation
Story must contain actor, action, and benefit clauses

## Story Format Template
```markdown
# Story: [Story Name]

## User Story
As a [type of user],
I want [some goal],
So that [some reason].

## Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

## Dependencies
- List any dependencies

## Notes
- Additional context
```