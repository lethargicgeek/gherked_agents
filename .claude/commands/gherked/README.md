# Gherked Commands

This folder contains command definitions for the Gherked BDD (Behavior-Driven Development) workflow system. These commands provide a streamlined interface to execute the various agents and orchestrate the complete specification generation process.

## Available Commands

### `/0_init`
**Purpose**: Initialize the project structure
**Actions**:
- Executes the 0_initializer agent
- Creates complete folder structure under `gherked_specs/`
- Installs usage rules into architecture_context folder
- Creates initial `stories_status.md` file
- Sets up story checklist templates

**Usage**: Run this command first when starting a new project

### `/1_stories_generate_story`
**Purpose**: Generate user stories from given prompts
**Actions**:
- Processes `given_prompt.md` files
- Creates structured user stories
- Generates story checklists
- Updates story status tracking

**Prerequisites**: Project must be initialized with `/0_init`

### `/2_role_gherkins_generate_changes`
**Purpose**: Generate role-based Gherkin specifications and change files
**Actions**:
- Creates role actor definitions
- Generates role-specific scenarios
- Produces `changes_for_role_gherkins.md` files
- Updates specification status

**Prerequisites**: User stories must be created

### `/3_user_interface_context_generate_changes`
**Purpose**: Generate UI context specifications and change files
**Actions**:
- Documents UI components and interactions
- Creates UI test scenarios
- Produces `changes_for_user_interface_context.md` files
- Links UI elements to user stories

**Prerequisites**: Role gherkins should be defined

### `/4_architecture_context_generate_changes`
**Purpose**: Generate architecture context documentation and change files
**Actions**:
- Documents technology stack decisions
- Records architectural patterns
- Produces `changes_for_architecture_context.md` files
- Maintains decision records

**Prerequisites**: UI context should be established

### `/5_component_gherkins_generate_changes`
**Purpose**: Generate component-level specifications and change files
**Actions**:
- Creates component behavior specs
- Defines component interfaces
- Produces `changes_for_component_gherkins.md` files
- Maps components to features

**Prerequisites**: Architecture context must be defined

### `/6_test_scripts_generate_changes`
**Purpose**: Generate test scripts and change files
**Actions**:
- Transforms Gherkin scenarios into executable tests
- Creates test fixtures
- Produces `changes_for_test_scripts.md` files
- Generates test execution plans

**Prerequisites**: Component gherkins should be complete

### `/7_check_conflicts`
**Purpose**: Validate consistency across all specifications
**Actions**:
- Checks for specification conflicts
- Validates dependencies
- Ensures test coverage
- Reports inconsistencies

**Prerequisites**: All specifications should be generated

### `/generate_all_changes`
**Purpose**: Execute the complete workflow from stories to test scripts
**Actions**:
- Runs all generation commands in sequence
- Processes all stories in the project
- Creates complete change documentation
- Performs final conflict checking

**Prerequisites**: Project must be initialized and stories created

## Command Structure

Each command file:
- References its implementation from `.gherked/commands/` using `@include`
- Follows a numerical naming convention indicating execution order
- Contains clear prerequisites and error handling

## Typical Workflow

1. **Initialize**: `/0_init` - Set up project structure
2. **Create Stories**: `/1_stories_generate_story` - Transform requirements
3. **Generate Specifications**:
   - `/2_role_gherkins_generate_changes`
   - `/3_user_interface_context_generate_changes`
   - `/4_architecture_context_generate_changes`
   - `/5_component_gherkins_generate_changes`
4. **Create Tests**: `/6_test_scripts_generate_changes`
5. **Validate**: `/7_check_conflicts`

Or use `/generate_all_changes` to run steps 2-5 automatically.

## Error Handling

Commands include error handling for:
- Missing prerequisites
- Invalid project structure
- File permission issues
- Incomplete specifications
- Circular dependencies

## Output Files

Commands generate various output files:
- `story.md` - Formatted user stories
- `story_checklist.md` - Progress tracking
- `changes_for_*.md` - Change documentation for each phase
- `stories_status.md` - Overall status tracking

## Best Practices

1. Always run `/0_init` before other commands
2. Create stories before generating specifications
3. Review conflict checker output before proceeding
4. Use `/generate_all_changes` for batch processing
5. Maintain clean folder structure between iterations

## Troubleshooting

Common issues and solutions:
- **"gherked_specs already exists"**: Clean up existing structure or use different directory
- **"No stories found"**: Ensure `given_prompt.md` files exist in story folders
- **"Conflicts detected"**: Review specifications for inconsistencies
- **"Missing dependencies"**: Run prerequisite commands first

## Contributing

When adding new commands:
1. Follow the numerical naming pattern
2. Create implementation in `.gherked/commands/`
3. Update this README
4. Ensure proper error handling
5. Document prerequisites clearly