
Create/update a set of agents and commands for claude code that can easily be copied to claude code.   Would like to use igniter 
  
# Key points of this expansion  
  
# Document Folder Structure  
Folder structure pre-requisites. Create the following folders if they don't already exist  
  
- context_specs  
  - 1_features
    - 0001-{feature namesa} (incremented folder, increment for each new feature)  
      - given_prompt.md (supplied by user when creating a new feature)  
      - changes_for_2_behaviors.md  
      - changes_for_3_architecture.md
      - changes_for_4_implementation_design.md
      - changes_for_5_test_scripts.md
    - checklist_for_stories.md  (lists all the folders in the 01_stories folder and tracks whether all it's sub check list tasks have been completed)
	    - creates a sub-check list for each story that checks off whether each of the following has been created and executed:
		    - created changes_for_product_requirements.md 
		    - created changes_for_architecture_design.md
		    - created changes_for_implementation.md
		    - created changes_for_acceptance_tests.md
		    - applied changes_for_product_requirements.md 
		    - applied changes_for_architecture_design.md
		    - applied changes_for_implementation.md
		    - applied changes_for_acceptance_tests.md
  - 2_role_gherkins
	  - user_actors.md
  - 3_user_interface_context
  - 4_architecture_context
	  - Divided into folders for each feature (groups of stories)
	  - Should already be sharded
  - 5_component_gherkins
  - 6_test_scripts
    -   Should contain manual tests 

# Agents  
## Agent Rules  
- Agents should never update any files prefixed with 'given_'.  These files were designed by a user.  The exception is the initializer agent  
  
## The Agents  
  
### 0_initializer  
- Creates all the initial files in the document structure  
  
### 1_features_agent
- Based bmad-core/agent/analyst.md  
- Looks through all the given_prompts and creates a story.md file within the story's folder to formalize the given_prompt

### 2_role_gherkins_agent
- Only able to update context_specs/2_behavior folder
- output files into the context_specs/02_product_requirements and updates the appropriate feature folder

### 3_architecture_context_agent
- based on bmad-core/agent/architect.md
- output files into the context_specs/03_architecture_design and updates the appropriate feature folder

## 4_test_scripts
- based on bmad-core/agent/qa.md
- output files into the context_specs/04_acceptance_criteria
  
  
# Commands  
  
## /init  
- Creates the initial docs folder structure.
- Installs usage rules from https://github.com/ash-project/usage_rules
	- mix usage_rules.sync .rules --all
  
## /execute_story_updates
- for each folder, check to see if 01_stories/checklist_for_stories.md has all the story folders listed.  If a folder is not listed, add it with the status of pending.  A story folder is not checked off until 

## /execute_specs_from_stories
- Updates all the documentation.  Does not update code.




----------- 
Notes: 
Example comparison

Let's use the example of a feature for an e-commerce website that allows a user to "add items to their cart."

**User story**  
_As a shopper, I want to add items to my cart, so that I can purchase them later_. 

This user story provides the feature's core intent and value, but it leaves many questions unanswered:

- What happens if the item is out of stock?
- What happens if the cart is already full?
- What happens if the user tries to add the same item twice?

**Gherkin scenarios**  
The Gherkin scenarios define the acceptance criteria for the user story, covering the different variations and outcomes. 

**Scenario 1: Adding an item to an empty cart**

gherkin

```
Given a user is on the product page for "Cool T-shirt"
When the user clicks "Add to Cart"
Then the cart icon displays a count of 1
And the user sees a confirmation message
```

Use code with caution.

**Scenario 2: Adding a second, different item to the cart**

gherkin

```
Given the cart contains "Cool T-shirt"
And the user is on the product page for "Awesome Socks"
When the user clicks "Add to Cart"
Then the cart icon displays a count of 2
```

Use code with caution.

**Scenario 3: Adding an item that is out of stock**

gherkin

```
Given the product "Cool T-shirt" is out of stock
And a user is on the product page for "Cool T-shirt"
When the user clicks "Add to Cart"
Then the user sees an "Out of Stock" message
And the cart count remains unchanged
```
