# NLP Chat-Bot for a Food Delivery System Using Dialoflow

I built a chatbot using **Dialogflow** for a food delivery system, covering the end-to-end process from Dialogflow basics to backend integration with **FastAPI** and a **MySQL** database. This project aims to solve a real-world problem faced by Mr. Pandey, a restaurant owner looking to automate customer support in a budget-friendly manner.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Solution Overview](#solution-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Directory Structure](#directory-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Conclusion](#conclusion)

## Problem Statement

Mr. Pandey runs a restaurant with a website that includes a food menu and delivery system supported by customer service. As his customer base grew, hiring customer support agents became costly. To address this, he decided to implement a chatbot integrated in his website as fast as possible and budjet friendly that could handle customer interactions, such as taking orders, tracking them, and answering about the restaurant's operating hours, thereby reducing costs and improving efficiency.

## Solution Overview

To meet Mr. Pandey's needs, I developed a chatbot using **Dialogflow**, leveraging its powerful **Natural Language Processing (NLP)** capabilities and cloud-based infrastructure. The chatbot handles the following functionalities:

- **New Order**: Takes customer orders based on menu selection.
- **Order Tracking**: Provides real-time tracking updates for orders.
- **Store Hours**: Shares information about the restaurant's operating hours.

I focused on implementing the above features in **Phase 1** due to time constraints. Future phases will include additional features like payment integration and user personalization.

![Untitled design](https://github.com/user-attachments/assets/e0049e26-26c4-4308-9c63-dbc25881d163)

### Why Dialogflow?
I chose Dialogflow over other platforms like **RASA** and **Amazon Lex** due to its:
- Pre-trained NLP models and cloud-based solutions.
- Easy integration with various platforms (web, mobile, etc.).
- Minimal training data requirements, making it ideal for quick deployment.

### Tech Stack
- **Chatbot Platform**: Dialogflow Essentials
- **Backend Framework**: FastAPI
- **Database**: MySQL
- **Languages**: Python, SQL

## Features

1. **Interactive Chatbot**: Handles new orders, tracks existing orders, and answers store hours.
2. **Database Integration**: Uses MySQL for storing order details and customer interactions.
3. **Webhook Integration**: Utilizes Dialogflow fulfillment to trigger backend operations.
4. **Spell Correction**: Handles minor typos and variations in food item names.
5. **Scalable Architecture**: Built with scalability in mind for future enhancements.

## Directory Structure

```plaintext
NLP Chat-Bot for a Food Delivery System/
├── backend
    ── main.py               # FastAPI backend code
    ── db_helper.py          # MySQL database connection
    ── generic_helper.py
├── dialogflow_intents/      # JSON files for Dialogflow intents
├── db
    ── pandeyji_eatery.sql   # SQL Database
├── frontend                 # Website frontend using HTML & CSS
├── requirements.txt         # List of dependencies
└── README.md                # Project documentation
```
## Installation

To set up the project on your local machine:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/rishwanth365/NLP_Chat-Bot_for_a_Food_Delivery_System.git
    cd NLP_Chat-Bot_for_a_Food_Delivery_System
    ```

2. **Install the dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up the MySQL Database**:
    - Ensure MySQL is running on your system.
    - Import the database server and run the provided SQL scripts to set up tables.

4. **Run the FastAPI backend server**:
    - Open VScode and run main.py to start the FastAPI backend server

5. **ngrok for https tunneling**:
    - Since the Dialogflow webhook allows only https POST requests rather than http we have to do tunneling to make http to https
    - To install ngrok, go to https://ngrok.com/download and install ngrok version that is suitable for your OS
    - Extract the zip file and place ngrok.exe in a backend folder.
    - Open windows command prompt, go to that backend folder and run this command: ngrok http 8000
    - It gives a temporary https URL that maps to your localhost:8000 FastAPI server copy that URL
NOTE: ngrok can timeout. you need to restart the session if you see session expired message.

6. **Dialogflow Integration**:
    - Import the intents JSON files in the `dialogflow_intents/` directory into your Dialogflow console.
    - Paste your webhook URL in Dialogflow Fulfillment section to point to your FastAPI server.

## Usage
- Go to Integrations section/ Web Demo to test the chat bot.
- Now integrate the chat bot in your website or you can just test it.

Here it is mine you can take a look "https://console.dialogflow.com/api-client/demo/embedded/c29081ce-f2ca-4efe-a644-80804955b75d"

## Future Enhancements
- Payment Gateway Integration: Allow users to pay directly via the chatbot.
- User Authentication: Implement login and signup functionalities.
- Personalized Recommendations: Use machine learning to suggest menu items based on user history.
- Multilingual Support: Expand chatbot capabilities to handle multiple languages.

## Conclusion
This chatbot project demonstrates how automation can significantly enhance customer service for food delivery systems. Leveraging Dialogflow for NLP and FastAPI for backend integration, Created a scalable and efficient solution for restaurant owners like Mr. Pandey.

This is the final product you can take a look
![image](https://github.com/user-attachments/assets/a682cb29-4a13-4e3e-b12f-21a6e34b0a89)
