
### Lab 2: Allow the user to Pause and Resume
We can configure a DynamoDB database table to remember which step the user was on when they stop or pause the skill.
Then, the skill can prompt the user to continue with the next step when re-launching the skill.

We will need to prepare our skill Lambda function to use a database called [DynamoDB](https://aws.amazon.com/dynamodb/).

#### Configure Permissions for DynamoDB
Steps:
1. Open a browser to the [AWS Console](https://aws.amazon.com/console)
1. Find the **IAM** service, click Roles, and click on the name of your standard Lambda role, such as ```lambda_basic_execution```.
1. Click the blue button to "Attach Policy"
1. There are over 200 possible policies.  Search for "dyn" and then locate the policy named ```DynamoDBFullAccess``` and click the checkbox.
1. Click "Attach Policy"

#### Enable the table within your Lambda code
Steps:
1. Review your Lambda function code within the AWS Lambda console.
1. Locate the line ```// alexa.dynamoDBTableName = 'RecipeSkillTable'; ``` which is at around line 53.
1. Uncomment out this line by removing the first two ```//``` characters.
1. Scroll up and click the blue "Save" button.
1. Test your skill.  Open the skill, say "begin cooking", and then say "stop".  You may encounter errors the first couple of times the skill runs.  This is okay.  The skill code is setting up a new table in DynamoDB which may take 60 seconds to complete.


Test your skill again.  Say Next a couple of times to advance through the recipe steps.  Next, say "Stop" or "Pause".
Launch the skill again and you should be prompted to continue where you left off.


### Practice and Demo
Practice all the features of your skill.  You can use [EchoSim.IO](https://echosim.io), the Amazon shopping app on your phone, or an Echo device.

Be ready to demo the skill to your fellow event attendees, friends, and family.  Ask them to try the skill and observe how they say their requests.

<hr />
