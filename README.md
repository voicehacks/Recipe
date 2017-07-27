# Recipe


# Breakfast Sandwich

## How can I build a Recipe Skill for Alexa? <a id="intro"></a>

Breakfast Sandwich is a skill that will guide the user through the process to prepare and cook a meal.
The skill can give the user a list of recipe ingredients, and then guide them through all the recipe steps.
You can install the skill, and then update the text within the Lambda Javascript code to define your own Recipe and Ingredients.

### Installing the skill

The instructor will walk you through the high level steps (check the full [Fact Skill Tutorial](https://github.com/alexa/skill-sample-nodejs-fact) for reference):

* Create a new AWS Lambda function:
  1. Choose the **Fact** blueprint template.
  1. Setup "Alexa Skills Kit" as the function trigger.
  1. Name the function ```BreakfastSandwich```
  1. Replace the existing code by pasting in the code from [src/index.js](src/index.js).
  1. Choose your default role ```lambda_basic_execution```
  1. Click "Create Function"

* Create a new skill
  1. Call the skill "Breakfast Sandwich" with invocation name ```breakfast sandwich```
  1. Launch "Skill Builder Beta"
  1. Click the Code Editor tab (just below the turqoise Dashboard tab on the top left)
  1. Copy and paste the ```speechAssets/InteractionModel.json``` contents into the Skill Builder Beta.
  1. Click Save, then Build
  1. Advance to the Configuration page, choose AWS Lambda ARN, and paste in the ARN from the function you created.


### Test

Practice speaking to the skill a few times to learn all the features of the skill.
When you ask for "ingredients", you will both hear a list of ingredients, and see the list on your Alexa app or Echo Show screen, if you have one.
When you ask to "begin cooking", the skill will guide you through each step in the process.


1. Be sure you have installed Node.JS on your laptop.
1. With the alexa-cookbook previously downloaded to a folder your laptop, open a command prompt and navigate to the cookbook folder (labs/Recipe/src).  Type in ```npm install```
1. Next, navigate back up to the (labs/BreakfastSandwich) folder.  Type in ```node testflow```
You should see a sequence of skill events be tested and the corresponding output.
This will look best with a black-background command prompt.
