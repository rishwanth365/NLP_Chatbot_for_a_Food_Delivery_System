# End-to-End NLP Chat-Bot for a Food Delivery System

I built a chatbot using **Dialogflow** for a food delivery system, covering the end-to-end process from Dialogflow basics to backend integration with **FastAPI** and a **MySQL** database. This project aims to solve a real-world problem faced by Mr. Pandey, a restaurant owner looking to automate customer support in a budget-friendly manner.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Solution Overview](#solution-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Conclusion](#conclusion)

## Problem Statement

Mr. Pandey runs a restaurant with a website that includes a food menu and delivery system supported by customer service. As his customer base grew, hiring customer support agents became costly. To address this, he decided to implement a chatbot that could handle customer interactions, such as taking orders, tracking them, and answering billing queries, thereby reducing costs and improving efficiency.

## Solution Overview

To meet Mr. Pandey's needs, I developed a chatbot using **Dialogflow**, leveraging its powerful **Natural Language Processing (NLP)** capabilities and cloud-based infrastructure. The chatbot handles the following functionalities:

- **New Order**: Takes customer orders based on menu selection.
- **Order Tracking**: Provides real-time tracking updates for orders.
- **Billing Queries**: Answers common billing-related questions.
- **Store Hours**: Shares information about the restaurant's operating hours.

I focused on implementing the above features in **Phase 1** due to time constraints. Future phases will include additional features like payment integration and user personalization.

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

1. **Interactive Chatbot**: Handles new orders, tracks existing orders, and answers billing questions.
2. **Database Integration**: Uses MySQL for storing order details and customer interactions.
3. **Webhook Integration**: Utilizes Dialogflow fulfillment to trigger backend operations.
4. **Spell Correction**: Handles minor typos and variations in food item names.
5. **Scalable Architecture**: Built with scalability in mind for future enhancements.

## Project Structure

```plaintext
NLP Chat-Bot for a Food Delivery System/
├── app.py                 # FastAPI backend code
├── database.py            # MySQL database connection
├── dialogflow_intents/    # JSON files for Dialogflow intents
├── requirements.txt       # List of dependencies
└── README.md              # Project documentation
```
## Installation

To set up the project on your local machine:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/food-delivery-chatbot.git
    cd food-delivery-chatbot
    ```

2. **Create a virtual environment** (optional but recommended):
    ```bash
    conda create --name chatbot-env python=3.9
    conda activate chatbot-env
    ```

3. **Install the dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up the MySQL Database**:
    - Ensure MySQL is running on your system.
    - Create a database and run the provided SQL scripts (if any) to set up tables.

5. **Run the FastAPI server**:
    ```bash
    uvicorn app:app --reload
    ```

6. **Dialogflow Integration**:
    - Import the intents JSON files in the `dialogflow_intents/` directory into your Dialogflow console.
    - Set up your webhook URL in Dialogflow to point to your FastAPI server.
