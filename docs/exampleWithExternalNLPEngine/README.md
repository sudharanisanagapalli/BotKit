
This BotKit example demonstrates how external NLP engines can be plugged to enhance Kore.ai Bot experience

Steps to import example files(path:./docs/exampleWithExternalNLPEngine) in api.ai,luis.ai and Kore.ai:

Steps to import the zip file(SearchHotels_apiai.zip) into api.ai account

- Login into your api.ai account (for first time loggers, you will be asked if you would like to create a new agent)
- Create a new Agent
- Go to your agent settings, select 'Export and Import' from the horizontal menu, and click on the 'IMPORT FROM ZIP' button. 
- Upload agent pop-up opens up, now choose the downloaded 'SearchHotels_apiai.zip' file and click on 'IMPORT' button
- Once the Import is done you be directed to 'General' tab,copy the Client access token from API Key section,store it and update it in the exampleWithExternalNLPEngine.js file (apiaiClientAccesstoken variable)
- Delete the "Default welcome Intent" and "Default Fallback Intent" in Intents section.


Steps to import luis json file (SearchHotels_luis.json) into luis.ai account

- Login into your luis.ai account 
- You will directed to My Apps section, where New app tab is highlighted.
- Click on Import App tab, a pop is displayed for Importing a new app from from your local drive (here you need to select the downloaded  file SearchHotels_luis.json file and click on Import button.
- Once the app is imported, you are directed to the dashboard page, click on 'Publish App' in the left panel of the page.
- In the Publish App section, you need to choose the 'Endpoint key' (choose default Bootstrap key) for assigning to the       
 application and 'Train' the app before publishing it.
- Once the app is published you will get 'Endpoint url' with the format:
    https://westus.api.cognitive.microsoft.com/luis/v2.0/apps/{appID}?subscription-key={subscription-key}&verbose=true&timezoneOffset=0&q=
- Copy the appId and subscription key and update it in the exampleWithExternalNLPEngine.js file (luisAppID, luisSubscriptionKey variables)


Steps to import Kore dialog json file (SearchHotels_Kore.json) into Kore account

- Login into your Kore account.
- Create a new Bot and Dialog task.
- Edit the created dialog task and click on the ellipsis botton on the top right corner then click on 'Import' option from the list 
- 'Import a Dialog' pop-up is dislayed, choose the downloaded (SearchHotels_Kore.json) file.
- Once file is imported is succssfully, click on 'Exit' button displayed at the top right corner of the 'Edit Dialog' page.
- Navigate to bot Settings tab, click on 'SDK Configuration' section for creating app credentials.
- Now create app and copy the 'CLIENT ID', 'CLIENT SECRET' and update those details in the config.json file (appId,apikey varibales)
- Open the exampleWithExternalNLPEngine.js file and update botId and botName variables with corresponding values.

Now you have the following ready-
1. Intent trained agent in api.ai
2. Intent & entity trained app in luis.ai
3. Dialog to show the results on Kore.ai.

To interact with bot follow the below steps:
1. Navigate to root folder of the BotKit.
2. Run following command in root location of the downloaded folder- "node app.js" and hit enter.
3. Now server will run on '8003' port.

----------------------------------------------

Follow the below steps to run this example Bot

- Define Bot under Kore.ai with a dialog task
- Define the intent under Api.ai, train and update the example code for API and keys
- Define the intent and entities with Luis.ai for entity extraction, train and update the example code for API and keys
- Run BotKit node.js server with app.js pointing to "exampleWithExternalNLPEngine.js"
- Enable BotKit module inside Kore.ai, point it to the BotKit server running, to intercept user and bot messages

