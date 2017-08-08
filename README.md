# Recipe
<a href="https://github.com/voicehacks/setup-local-recommendations">Local Recommendations</a>

[Detailed Setup](Detailed-Setup-Instructions/README.md)

<a href="Lab 1/README.md">Lab 1</a>


<a href="Lab 2/README.md">Lab 2</a>

# Breakfast Sandwich

## How can I build a Recipe Skill for Alexa? <a id="intro"></a>
This lab will teach you how to use a database to persist information so users can pause and resume a skill, or exit then return to the same place in the conversation that they had left off.

Have you ever played music and needed to pause in the middle of a song? What about ordering a pizza online, and we leave the page for a while. In both cases, on our return, we have the option of continuing right where we left off, or starting over from the beginning. By persisting information in a database, we can give Alexa the capability to store a memory of a recent conversation just as a human would. Which will lead to a more natural, conversational feel to your skill from a user's perspective.

<!-- TODO:  Re-word this and provide the option for more detailThis lesson consists of 3 main steps: Use the code provided in [src/index.js](src/index.js) and in [speechAssets/IntentSchema.json](speechAssets/IntentSchema.json) -->

### Task 1: Build the Skill
Create your skill using the Lambda code given in [src/index.js](src/index.js) and the [Interaction Model](speechAssets/InteractionModel.json). If you're comfortable completing this step on your own, feel free to do it and move to Task 2. Otherwise, follow the steps in the

### Task 2: Enable Permissions
We can configure a DynamoDB database table to remember which step the user was on when they stop or pause the skill.
Then, the skill can prompt the user to continue with the next step when re-launching the skill.

We will need to prepare our skill's Lambda function to use a database called [DynamoDB](https://aws.amazon.com/dynamodb/).

<!-- Every skill is lowest-needed permissions first, need to add them as necessary -->

If you've never done this before or need a refresher, use [this guide]() to walk you through how to enable permission for a database before we define it within our Lambda function. If you're comfortable doing this on your own, go ahead and move to Task 3.
#### Configure Permissions for DynamoDB
Steps:
1. Open a browser to the [AWS Console](https://aws.amazon.com/console)
1. In the search box titled **AWS services**, type ```IAM``` then click the option reading **IAM** (Manage User Access and Encryption Keys)
1. On the new page reading **Welcome To Identity and Access Management** your navbar to the left should have an option called **Roles**. Click that.
1. On this page, you should see the name of your standard Lambda role, ```lambda_basic_execution```. Click the role name.
1. In the **Permissions** tab, under "Managed Policies", click the blue button titled "Attach Policy"
1. In the filter field, type "dynamo" and then locate the policy named ```DynamoDBFullAccess``` and click the checkbox.
1. Click "Attach Policy"

### Task 3: Enable Database
Now that we've added permission to our database, it's time to enable it within our Lambda function. In the source code provided, uncomment the line that looks like this: ```// alexa.dynamoDBTableName = 'RecipeSkillTable'; ```

#### Enable the table within your Lambda code
Steps:
1. Review your Lambda function code within the AWS Lambda console.
1. Locate the line ```// alexa.dynamoDBTableName = 'RecipeSkillTable'; ``` which is at around line 53.
1. Uncomment out this line by removing the first two ```//``` characters.
1. Scroll up and click the blue "Save" button.
1. Test your skill.  
1. Open the skill using [echosim.io](https://echosim.io). Once it's up and ready, say "begin cooking", and then say "stop".  You may encounter errors the first couple of times the skill runs.  This is okay.  The skill code is setting up a new table in DynamoDB which may take 60 seconds to complete.



### Test

Practice speaking to the skill a few times to learn all the features of the skill.
When you ask for "ingredients", you will both hear a list of ingredients, and see the list on your Alexa app or Echo Show screen, if you have one.
When you ask to "begin cooking", the skill will guide you through each step in the process.

### Extra Credit
These are some suggestions for building and customizing this recipe skill

#### Add Additional Recipes

Currently this skill tells you how to make one kind of sandwich. Expand your skill to allow users to choose a recipe first, and then hear the recipe. You'll probably want to add some new intents to prompt your users for a type of sandwich if they fail to specify (Hint: If you opt for a custom slot, you may want to make it required to fulfill the intent. The skill builder tool has a way to do this.) Reading and understanding the code provided, then modifying it is a great way to understand what you just built.

#### Add More Card images

If you looked through the source code for this skill, you probably noticed that we have a welcome card image being used. Add to your current skill to display different images according to the state of your skill.
