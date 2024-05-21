# Eco Eatery - Food Ordering Chatbot

## Project Overview

Eco Eatery is a user-friendly chatbot built with Dialogflow and FastAPI. It allows customers to place orders for food items from a virtual eatery, offering a seamless and conversational ordering experience. Users can add or remove items, track order status, and complete their orders via the chatbot. The system integrates with a MySQL database to store order details and track order statuses.  

## Features

* **Chat-Based Ordering:**  Natural language interaction for placing and managing orders.
* **Order Tracking:**  Provides real-time updates on order status.
* **Order Completion:**  Process orders, generate order IDs, and calculate total order costs.
* **Database Integration:**  Stores order data and statuses for future reference.
* **Web Interface:**  A simple HTML page provides a visual representation of the menu and a chatbot integration.

## Getting Started

1. **Prerequisites:**
   * Python 3.6+
   * Dialogflow account (https://dialogflow.cloud.google.com/)
   * MySQL database
   * `pip install -r requirements.txt`

2. **Setup:**
   * **Dialogflow:** Create an agent, intents (new order, add to order, etc.), and fulfillment settings (pointing to your FastAPI server).
   * **Database:** Create a database with tables for orders, order items, and order tracking. (See the `db_support.py` file for database schema)
   * **Configuration:** Modify the database connection parameters in `db_support.py` to match your environment.

3. **Run the App:**
   * Run `python main.py`

4. **Interact with the Chatbot:**
    * Go to the `page.html` file and open it in a browser.

## Code Structure

* **`main.py`:**  Handles API requests, routes requests to the appropriate functions, and interacts with the Dialogflow webhook.
* **`db_support.py`:**  Provides functions for database interaction, including order insertion, retrieval, and order status updates.
* **`generic_helper.py`:** Contains utility functions for extracting information from Dialogflow responses and formatting order data.
* **`page.html`:**  Simple HTML page for the website interface and chatbot integration.

## Future Improvements

* **Menu Management:** Implement a way to dynamically load menu items from the database.
* **Payment Integration:**  Integrate a payment gateway for online payments.
* **User Authentication:**  Allow users to create accounts for personalized ordering.

## Code Improvements

* **Error Handling:** Enhance error handling throughout the code. Implement more specific error messages in both the chatbot responses and the logs.
* **Database Schema:** Ensure the database schema is designed to support future features, like user accounts and payment processing.
* **Data Validation:** Add validation checks for user inputs (e.g., order quantities).
* **Code Structure:** Consider using classes or modules to organize the code further, especially if the project grows in complexity.
* **Testing:** Implement unit tests for core functions, particularly for the database interactions and order processing logic.

## Acknowledgements

This project was inspired by [Code Basics Youtube Channel].
