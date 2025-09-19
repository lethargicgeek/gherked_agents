# Gherked Agents

This folder contains specialized agents for the Gherked BDD (Behavior-Driven Development) workflow system. Each agent handles a specific phase in the process of transforming user requirements into test-driven development specifications.

## Available Agents

### 0. Initializer Agent (`0_initializer.md`)
**Purpose**: Bootstrap the project structure and initial configuration
**Responsibilities**:
- Creates the complete gherked_specs folder structure
- Installs usage rules from external repositories
- Initializes status tracking files
- Sets up initial configuration templates

### 1. Stories Agent (`1_stories.md`)
**Purpose**: Transform user prompts into formalized user stories
**Responsibilities**:
- Analyzes given prompts for feature intent
- Creates structured user stories in "As a..., I want..., So that..." format
- Identifies and documents acceptance criteria
- Creates story checklists for tracking progress
- Updates story status tracking

### 2. Role Gherkins Agent (`2_role_gherkins.md`)
**Purpose**: Generate role-based Gherkin specifications
**Responsibilities**:
- Creates role actor definitions
- Generates role-specific behavior scenarios
- Defines role-based acceptance tests

### 3. User Interface Context Agent (`3_user_interface_context.md`)
**Purpose**: Define and manage UI context specifications
**Responsibilities**:
- Documents UI components and interactions
- Creates UI-specific test scenarios
- Manages UI state transitions and validations

### 4. Architecture Context Agent (`4_architecture_context.md`)
**Purpose**: Manage architecture and technical context
**Responsibilities**:
- Documents technology stack decisions
- Manages architectural patterns and constraints
- Maintains technical debt and decision records

### 5. Component Gherkins Agent (`5_component_gherkins.md`)
**Purpose**: Generate component-level Gherkin specifications
**Responsibilities**:
- Creates component behavior specifications
- Defines component integration tests
- Documents component interfaces and contracts

### 6. Test Scripts Agent (`6_test_scripts.md`)
**Purpose**: Generate executable test scripts from specifications
**Responsibilities**:
- Transforms Gherkin scenarios into test code
- Creates test fixtures and data
- Generates test execution reports

### 7. Conflict Checker Agent (`7_conflict_checker.md`)
**Purpose**: Validate consistency across specifications
**Responsibilities**:
- Checks for conflicts between different specification levels
- Validates dependencies and prerequisites
- Ensures test coverage completeness

## Usage

Each agent is designed to be invoked through the Claude Code agent system. They reference their actual implementation from the `.gherked/agents/` directory using the `@include` directive.

## Workflow

The agents are typically executed in numerical order:
1. Initialize project structure (Agent 0)
2. Create user stories from requirements (Agent 1)
3. Define role-based behaviors (Agent 2)
4. Specify UI interactions (Agent 3)
5. Document architecture decisions (Agent 4)
6. Create component specifications (Agent 5)
7. Generate test scripts (Agent 6)
8. Validate consistency (Agent 7)

## Dependencies

- Agents rely on the folder structure created by the Initializer Agent
- Each agent may depend on outputs from previous agents in the workflow
- All agents share common status tracking through `stories_status.md`

## Error Handling

Each agent includes specific error handling for:
- Missing prerequisites
- Invalid input formats
- Conflicting specifications
- File system permissions issues

## Contributing

When adding new agents:
1. Follow the numerical naming convention
2. Create both the agent file and its implementation in `.gherked/agents/`
3. Update this README with the new agent's description
4. Ensure proper error handling and validation