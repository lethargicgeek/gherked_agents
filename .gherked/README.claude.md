# Claude Code Integration for Gherked Agents

This folder contains the Claude Code configuration for the Gherked Agents system.

## Structure

- `claude_project.json` - Main configuration file that references all agents, commands, and templates
- All actual content is stored in `.gherked/` folder

## Usage with Claude Code

1. Open Claude Code in this project directory
2. Claude will automatically recognize the agents and commands from the configuration
3. Use commands like `/0_init` to initialize a project
4. Use `/generate_all_changes` to run the full workflow

## Available Commands

- `/0_init` - Initialize project structure
- `/1_stories_generate_story` - Generate stories from prompts
- `/2_role_gherkins_generate_changes` - Generate role-based Gherkin scenarios
- `/3_user_interface_context_generate_changes` - Generate UI specifications
- `/4_architecture_context_generate_changes` - Generate architecture designs
- `/5_component_gherkins_generate_changes` - Generate component specifications
- `/6_test_scripts_generate_changes` - Generate test scripts
- `/7_check_conflicts` - Check for conflicts across specifications
- `/generate_all_changes` - Run all agents in sequence
- `/sync_gherked` - Sync changes from prompt.md to .gherked folder

## Agents

Each agent has a specific role in the specification generation pipeline:
1. **Initializer** - Sets up project structure
2. **Stories** - Converts prompts to user stories
3. **Role Gherkins** - Creates behavioral specifications by role
4. **UI Context** - Designs user interfaces
5. **Architecture** - Defines technical architecture
6. **Component Gherkins** - Creates component-level specs
7. **Test Scripts** - Generates test coverage
8. **Conflict Checker** - Validates consistency

## Syncing with prompt.md

Run `/sync_gherked` to update the `.gherked` folder with any changes made to `prompt.md`