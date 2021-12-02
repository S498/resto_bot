## Resto Bot

I've built a simple chatbot the Resto Bot where users can search restaurants through the Zomato API based location and cuisine. 

If user request matches with in-flow intents and if there are no or missing entities in the utterance then bot should ask required entities (cuisine and location in this phase) to complete the action (search restaurant from Zomato API). 
Here I trained the model to extract cuisine.

#### Setup and installation instructions:
* Please follow the installation instruction mentioned here: [Installation instructions](installation-instructions.md)

Once we're done with the installation,

Now it’s time to train the bot. 
Execute below command and explore this for more training options: https://rasa.com/docs/rasa/user-guide/command-line-interface/#train-a-model  
`rasa train`  

Now, use the below command to start the rasa server.
`rasa run`

Let’s see how bot performs with limited training data and let’s explore rasa x and improve it.
Run the following command in every new tab.
`rasa run actions`

Once, the servers are up, we need to route the local server to the web using Ngrok.

Install Ngrok, and then the below command, (5005 is the port at which the rasa server is being hosted)
ngrok http 5005

Now, we need to integrate the application with the facebook's messenger

Go to facebook's developer portal and create an Application.

Once the application is created, go to the messager settings of the application,
create a page on facebook so that the page can have it's own chatbot.

Once the page is created generate the web token for the page. And enter that token in the credentials file, under the access token.
Create a name for the token under the verify.
And enter the secret key from the Settings -> Basic in the created application in Facebook.

Now, go to the webhooks part of the messenger settings, and create a webhook using the HTTPS url generated in Ngrok and the name of the access token given in  the credentials file.

Now, Start the RASA Server using the `rasa run` command.

Now, you're good to go!