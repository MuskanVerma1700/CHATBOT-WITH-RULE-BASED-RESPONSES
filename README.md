# CHATBOT-WITH-RULE-BASED-RESPONSES
Build a simple chatbot that responds to user inputs based on predefined rules. Use if-else statements or pattern matching techniques to identify user queries and provide appropriate responses. This will give you a basic understanding of natural  language processing and conversation flow.

#code
# Define the chatbot's responses
responses = {
    "hi": "Hello there! How can I assist you?",
    "hello": "Hi! How can I help you?",
    "hey": "Hey! How can I assist you?",
    "what's your name?": "I'm a chatbot. You can call me ChatBot!",
    "default": "I'm sorry, I didn't understand that. Could you please rephrase?",
}

# Function to get chatbot response
def get_response(user_input):
    user_input = user_input.lower()
    
    for pattern, response in responses.items():
        if pattern in user_input:
            return response
    
    return responses["default"]

# Main chat loop
print("ChatBot: Hi! I'm here to help. You can type 'exit' to end the conversation.")
while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        print("ChatBot: Goodbye!")
        break
    else:
        bot_response = get_response(user_input)
        print("ChatBot:", bot_response)
