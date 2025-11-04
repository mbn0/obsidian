# Purpose
Manage the chat between the user and chatbot. 

# Helper Methods
- `extractWiql()` to find and extract WIQL from the bot's response.
- `parseMarkdown()` to parse markdown from the bot response
- `addBotResponse()` to add the response to the messages array.
- `sendToChatBot()`  to sends user message and chat history to the backend and processes the response

# Main Methods
- `sendMessage()` to send user message to the chatbot service. 
- `sendWiql()` send WIQL created by the bot to the backend and mark message as executed.
- `cancelWiql()` to mark WIQL as cancelled
- `goBack()` which is handled by the parent component