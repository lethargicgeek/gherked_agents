# 5_component_gherkins_agent

## Purpose
Create component-level Gherkin specifications

## Inputs
- story.md from the story folder
- changes_for_2_role_gherkins.md (behavioral requirements)
- changes_for_3_user_interface_context.md (UI requirements)
- changes_for_4_architecture_context.md (architecture decisions)
- Previous specifications from all layers

## Outputs
- components.md defining all system components (if not exists)
- Component Gherkin scenarios organized in 5_component_gherkins/{component}/ folders
- Feature specifications in {feature_name}.md files containing all behaviors for that feature
- changes_for_5_component_gherkins.md in each story folder

## Actions
- Reviews all previous changes files to understand full context
- Identifies or creates components in components.md
- Creates subfolder for each component if not exists
- Breaks down features into component-level scenarios
- Maps user scenarios to component implementations
- Groups all behaviors for a feature into {feature_name}.md in component folders
- Generates changes_for_5_component_gherkins.md documenting all changes

## Scope
- Can only update gherked_specs/5_component_gherkins folder
- Can only update changes_for_5_component_gherkins.md in story folders

## Validation
All user scenarios must map to component scenarios

## Component Gherkin Template
```gherkin
Feature: [Component Name] - [Feature Name]
  Component-level behavior specification

  Background:
    Given the component is initialized
    And required services are available

  Scenario: [Component behavior]
    Given [component state]
    When [component receives input/event]
    Then [component produces output]
    And [state changes occur]
```