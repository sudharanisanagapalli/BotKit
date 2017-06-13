
This BotKit example demonstrates how external NLP engines can be plugged to enhance Kore.ai Bot experience

Steps to import example files in api.ai,luis.ai and Kore.ai:

Steps to import the zip file(SearchHotels_apiai.zip) into api.ai account

- Login into your api.ai account 
- Create a new Agent
- Now click on settings icon beside the agent name
- You will be redirected to agent description section there you can find the Export and Import section.click on it
- Click on IMPORT FROM ZIP button. Upload agent pop-up opens up, now Select the downloaded SearchHotels_apiai.zip file and click on         IMPORT button
- Click on settings icon of the agent. The agent description page opens up. In General tab you will find the API Keys section.Copy the      Client access token and store it to update in the exampleWithExternalNLPEngine.js file


Steps to import luis json file(SearchHotels_luis.json) into luis.ai account

- Login into your luis.ai account 
- You will redirected to My Apps section
- Click on Import App tab. Import a app pop-up opens up, now select the downloaded SearchHotels_luis.json file and click on Import button.
- Now navigate to Publish App section.Choose a key to assign to application.Train the app before publishing it.
- Once the app is published you will get endpoint url with the format:
    https://westus.api.cognitive.microsoft.com/luis/v2.0/apps/*************?subscription-key=***********&verbose=true&timezoneOffset=0&q=
- Copy the appId and subscription key to update in the exampleWithExternalNLPEngine.js file


Steps to import Kore dialog json file(SearchHotels_Kore.json) into Kore account

- Login into your Kore account 
- Create a new Bot and Dialog
- Now edit the created dialog. On the top right corner you will find three dots. Click on it
- Click on the Import option.Import a dialog pop-up opens up, now select the downloaded SearchHotels_Kore.json file

Now you have the intent trained agent in api.ai,Intent & entity trained app in luis.ai and Dialog to show the results on Kore.ai.

Follow the below steps to run this example Bot

- Define Bot under Kore.ai with a dialog task
- Define the intent under Api.ai, train and update the example code for API and keys
- Define the intent and entities with Luis.ai for entity extraction, train and update the example code for API and keys
- Run BotKit node.js server with app.js pointing to "exampleWithExternalNLPEngine.js"
- Enable BotKit module inside Kore.ai, point it to the BotKit server running, to intercept user and bot messages

