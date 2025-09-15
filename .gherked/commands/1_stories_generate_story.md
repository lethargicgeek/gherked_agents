# /1_stories_generate_story

## Description
Generate story.md and story_checklist.md from given_prompt.md for pending stories

## Actions
1. Reads stories_status.md to identify stories with "new" or "pending" status
2. For each identified story:
   - Executes 1_stories_agent on given_prompt.md
   - Creates story.md with formalized user story
   - Creates story_checklist.md if not already present
   - Updates stories_status.md to "pending"

## Usage
Run after creating new given_prompt.md files to generate formal user stories

## Validation
- Ensures given_prompt.md exists before processing
- Skips stories that already have story.md

## Prerequisites
- given_prompt.md must exist in story folder
- stories_status.md must be initialized

## Output
- story.md in each processed story folder
- story_checklist.md with task tracking
- Updated stories_status.md