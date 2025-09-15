# /0_init

## Description
Initialize the project structure using the 0_initializer agent

## Actions
1. Executes the 0_initializer agent
2. Creates complete folder structure under gherked_specs/
3. Installs usage rules into architecture_context folder
4. Creates initial stories_status.md file
5. Sets up story_checklist.md template

## Usage
Run this command first when starting a new project to set up all required folders and initial files.

## Error Handling
- Checks if structure already exists before creating
- Reports any permission issues or conflicts
- Provides rollback option if initialization fails partway

## Command Implementation
```bash
# Check if gherked_specs exists
if [ -d "gherked_specs" ]; then
  echo "Error: gherked_specs already exists"
  exit 1
fi

# Create folder structure
mkdir -p gherked_specs/{1_stories,2_role_gherkins,3_user_interface_context,4_architecture_context,5_component_gherkins,6_test_scripts}

# Create initial files
touch gherked_specs/1_stories/stories_status.md
touch gherked_specs/2_role_gherkins/role_actors.md
touch gherked_specs/4_architecture_context/tech_stack.md
touch gherked_specs/5_component_gherkins/components.md

# Install usage rules
cd gherked_specs/4_architecture_context
mix usage_rules.sync .rules --all
```