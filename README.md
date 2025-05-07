# python-simple-chat-bot

# Simple Chatbot in Python

def chatbot_response(user_input):
    responses = {
        "hello": "Hi there! How can I help you today?",
        "how are you": "I'm just a bunch of code, but I'm here to help you!",
        "bye": "Goodbye! Have a great day!",
        "what is your name": "I'm a simple chatbot created in Python."
    }
    
    # Convert user input to lowercase to make the bot case-insensitive
    user_input = user_input.lower()
    
    # Check if the user input is in the predefined responses
    if user_input in responses:
        return responses[user_input]
    else:
        return "I'm sorry, I don't understand that. Can you please rephrase?"

def main():
    print("Chatbot: Hello! Type 'bye' to exit.")
    while True:
        user_input = input("You: ")
        if user_input.lower() == "bye":
            print("Chatbot: Goodbye! Have a great day!")
            break
        response = chatbot_response(user_input)
        print(f"Chatbot: {response}")

if __name__ == "__main__":
    main()
