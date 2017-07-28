### Installing the skill

The instructor will walk you through the high level steps (check the full [Fact Skill Tutorial](https://github.com/alexa/skill-sample-nodejs-fact) for reference):

* Create a new AWS Lambda function:
  1. Choose the **Fact** blueprint template.
  1. Setup "Alexa Skills Kit" as the function trigger.
  1. Name the function ```BreakfastSandwich```
  1. Replace the existing code by pasting in the code from [src/index.js](../src/index.js).
  1. Choose your default role ```lambda_basic_execution```
  1. Click "Create Function"

* Create a new skill
  1. Call the skill "Breakfast Sandwich" with invocation name ```breakfast sandwich```
  1. Launch "Skill Builder Beta"
  1. Click the Code Editor tab (just below the turqoise Dashboard tab on the top left)
  1. Copy and paste the ```speechAssets/InteractionModel.json``` contents into the Skill Builder Beta.
  1. Click Save, then Build
  1. Advance to the Configuration page, choose AWS Lambda ARN, and paste in the ARN from the function you created.

### Next Step:


https://github.com/voicehacks/Recipe/tree/master/Lab%201
