# Recipe


# Breakfast Sandwich

## How can I build a Recipe Skill for Alexa? <a id="intro"></a>

Breakfast Sandwich is a skill that will guide the user through the process to prepare and cook a meal.
The skill can give the user a list of recipe ingredients, and then guide them through all the recipe steps.
You can install the skill, and then update the text within the Lambda Javascript code to define your own Recipe and Ingredients.

### Installing the skill

At this point you should be familiar with the process of installing the skill and able to get through it on your own.  If not, feel free to review the [Detailed Instructions]() for some step-by-step guidance. Otherwise, go ahead and install the skill then proceed to the [first lab](). 

### Test

Practice speaking to the skill a few times to learn all the features of the skill.
When you ask for "ingredients", you will both hear a list of ingredients, and see the list on your Alexa app or Echo Show screen, if you have one.
When you ask to "begin cooking", the skill will guide you through each step in the process.


1. Be sure you have installed Node.JS on your laptop.
1. With the alexa-cookbook previously downloaded to a folder your laptop, open a command prompt and navigate to the cookbook folder (labs/Recipe/src).  Type in ```npm install```
1. Next, navigate back up to the (labs/BreakfastSandwich) folder.  Type in ```node testflow```
You should see a sequence of skill events be tested and the corresponding output.
This will look best with a black-background command prompt.
