🤖 Python Chatbot

A simple rule-based chatbot built in Python that responds to user input with predefined answers or default fallback messages. It’s perfect for beginners learning Python, conditional logic, and basic AI concepts.

🌟 Features

-Friendly greetings (hello)

-Answers basic questions (how are you, name)

-Farewell responses (bye)

-Default responses when input is unrecognized

-Continuous conversation until the user types exit

🛠️ Technologies Used

~Python 3.x

~Random module for selecting varied responses

💬 How It Works

-Stores predefined responses in a dictionary.

-Converts user input to lowercase for easy matching.

-Checks if any keywords match the input:

 #If yes → returns a random predefined response

 #If no → returns a default response

-Loop continues until user types exit.

💻 Sample Code
import random

responses = {
    "hello": ["Hi there!", "Hello!", "Hey! How can I help you?"],
    "how are you": ["I'm fine!", "Doing great!", "All good!"],
    "bye": ["Goodbye!", "See you later!", "Take care!"],
    "name": ["I am your chatbot!", "You can call me Python Bot."],
}

default_responses = ["I don't understand that.", "Can you say that again?", "Interesting... tell me more!"]

def chatbot():
    print("🤖 Chatbot: Hello! Type 'exit' to quit.\n")
    while True:
        user_input = input("You: ").lower()
        if user_input == "exit":
            print("🤖 Chatbot: Goodbye!")
            break
        found = False
        for key in responses:
            if key in user_input:
                print("🤖 Chatbot:", random.choice(responses[key]))
                found = True
                break
        if not found:
            print("🤖 Chatbot:", random.choice(default_responses))

chatbot()

🎯 Learning Outcomes

-Working with Python dictionaries and lists

-Handling user input

-Using conditional statements and loops

-Leveraging the random module for varied responses

-Understanding basic chatbot logic

🚀 Usage

-Clone this repository:

-git clone <your-repo-url>

-Run the Python script:

=python chatbot.py

Type messages and chat with the bot. Type exit to quit.

👨‍💻 Author

Bhavika Sharma
