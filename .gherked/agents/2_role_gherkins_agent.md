# 2_role_gherkins_agent

## Purpose
Generate behavioral specifications in Gherkin format

## Inputs
- story.md from the story folder
- given_prompt.md (original user request)

## Outputs
- role_actors.md defining all system actors (if not exists)
- Gherkin scenarios organized by actor in 2_role_gherkins/{actor}/ folders
- Behavioral specifications in {feature_name}.md files per actor
- changes_for_2_role_gherkins.md in each story folder

## Actions
- Reviews story.md to understand requirements
- Identifies or creates role actors in role_actors.md
- Creates subfolder for each role actor if not exists
- Creates Given/When/Then scenarios organized by actor and feature
- Generates behavioral specifications as {feature_name}.md in actor folders
- Generates changes_for_2_role_gherkins.md documenting all changes

## Scope
- Can only update gherked_specs/2_role_gherkins folder
- Can only update changes_for_2_role_gherkins.md in story folders

## Validation
Each scenario must be executable and unambiguous

## Gherkin Template
```gherkin
Feature: [Feature Name]
  As a [role]
  I want [feature]
  So that [benefit]

  Scenario: [Scenario name]
    Given [initial context]
    When [action/event]
    Then [expected outcome]
    And [additional outcome]
```