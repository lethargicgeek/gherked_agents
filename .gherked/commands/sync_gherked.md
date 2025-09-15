# /sync_gherked

## Description
Synchronize the .gherked folder with the latest specifications from prompt.md

## Actions
1. Parses prompt.md for agent definitions
2. Parses prompt.md for command definitions
3. Updates agent files in .gherked/agents/
4. Updates command files in .gherked/commands/
5. Updates claude_project.json with any new agents/commands
6. Reports changes made

## Usage
Run after updating prompt.md to keep .gherked folder in sync

## Output
- Updated agent and command files in .gherked/
- Summary of changes applied
- List of any conflicts or manual reviews needed

## Implementation Notes
This command should:
- Extract agent definitions between `### [N]_*_agent` headers
- Extract command definitions between `### /[command]` headers
- Preserve existing customizations in .gherked files where possible
- Create new files for any new agents/commands found
- Update the claude_project.json references

## Sync Process
1. **Backup** - Create backup of current .gherked folder
2. **Parse** - Extract definitions from prompt.md
3. **Compare** - Identify changes between prompt.md and .gherked
4. **Apply** - Update files with changes
5. **Validate** - Ensure all references are valid
6. **Report** - Show summary of changes