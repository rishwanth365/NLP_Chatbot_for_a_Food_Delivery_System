# End-to-End NLP Chat-Bot for a Food Delivery System

I built a chatbot in Dialogflow for a food delivery system. It will be an end-to-end project covering Dialogflow basics, building a backend in python and Fastapi, interactions with MySQL database, and much more. I covered Dialogflow fundamentals such as intents, entities, contexts, etc.

## Problem Statement:

Mr. Pandey runs a restaurant he had modorate customer base due to the area the restaurant was located he want to expand his business by opt into third-party delivery agencies like Swiggy and Zomato. Unfortunately his aplication has not been accepted. So, he decided to build a custom website for his customers which includes his food menu and delivery system. As of now everything is fine it raise his customer base but problem is there is no customer support in his website hiring customer support is not budjet friendly for him so he decided to create a chat-bot that it can understand customer intrest and displays available food menu accordingly it can take orders and displays order tracking. Now I need to build chat-bot for him here I built a chatbot in Dialogflow for a food delivery system.

![Untitled design](https://github.com/user-attachments/assets/e0049e26-26c4-4308-9c63-dbc25881d163)

1. Here My scope of work in chat bot is only on new order, track order, billing queries and store hours because Mr. Pandey asked me to implement chat bot as soon as possible with budjet friendly so I decided to go with this limited features for Phase-1 after that take some time to include other features in chat bot such as implementing payment system in chat bot etc.,
2. For Chatbot Platform Selection I chose Dialogflow rather than RASA and Amazon Lex is because Dialogflow offers powerful NLP capabalities out of the box, Cloud-based solution, Provides easy integrations with various platforms and channels and more over it relies on Google's vast pre-trained data so there is no need to gather data for training since I don't have much time so chose Dialogflow to build chat bot.
3. For backend part I chose FastApi and MySQL for database management because it is easy and very familiar to me.

Here is the big companies using Dialogflow as chat-bot and perfectly working
![image](https://github.com/user-attachments/assets/848410c5-8574-48a7-bc2d-482373e867fd)
Now Iam 100% confident that using Dialogflow is not worst decision
Specifically I used Dialogflow essentials it has Training Phrases - Phrases you can expect from users, that will trigger. When a user says something similar to a training phrase, Dialogflow matches it to the intent. You don’t have to create an exhaustive list. Dialogflow will fill out the list with similar expressions. To extract parameter values, use annotations with available system or custom entity types.
the intent.
Chat Bot Responses - Text, spoken and media rich responses the chat bot will deliver to a user.

For Example, When user type Hi or Hey the Chat Bot replies Hello, How can I help you? you can say "New Order" or "Track Order"
The work starts from creating necessary intents(In Dialogflow, an intent is a messaging object that categorizes an end-user's intention for a single conversation turn)
I created thease intents:
![image](https://github.com/user-attachments/assets/725993df-260f-41f9-a6ef-f92d0a2b573a)
order.add - context: ongoing-order
order.complete - context: ongoing-order
order.remove - context: ongoing-order
track.order - context: ongoing-tracking
for thease intents I enabled fulfillment because to create webhook for thease intents which are work in backend which contents to MySQL feel free head to backend directory to check the main.py code
Added food-item entities because sometimes user may do spell mistakes or use other food item name
At final the website URL has to paste in webhook in order to link chatbot to the website and integrate the chat bot in website.

This is the final product you can take a look
![image](https://github.com/user-attachments/assets/a682cb29-4a13-4e3e-b12f-21a6e34b0a89)
