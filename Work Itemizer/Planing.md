# Requirements
A chatbot interface for Azure DevOps where the user can ask about work items, add them, delete them, and more.
# Ways to connect with Azure DevOps Work Items

## 1. Using Azure DevOps REST API

## 2.  Using Azure DevOps SDKs
[[Testing AzureDevOps SDK|Testing Azure DevOps SDK]]
# Approaches

# 1. Make the Chatbot Create a Custom Query
The user requests a certain thing from the chatbot, the chatbot creates a proper Query.
# 2. Make the Chatbot Answer
Also has two approaches: 
1. The chatbot receives all data and answers depending on it.
2. The chatbot requests data depending on question.

# is a RAG required? 
(Not needed for now)

# How to make the chatbot call the backend??
## Current Plan
- Make a single endpoint to retrieve all Work Items from the backend 
- Make endpoints for addition, Bulk Addition
- Give all info to the chatbot and let it answer according to that.
## Alternative (Good if Work Items are too much to handle)
Note: this alternative approach is only good if work items are in a size that affects the smoothness of the application 
 After the user asks a question, the bot is prompted to create a WIQL Query, so he requires the user the necessary info to create the Query (Such as project name, person name, etc.)
After that, the query created by the LLM is shown to the user and the user is prompted to allow sending this query to the backend or not.
- the frontend reads the chatbot and takes out the WIQL and sends it to the backend, 
- the backend executes the WIQL
- the backend sends the output data to the frontend
- the frontend displays the data table.
- the chatbot reads the data received.
### example from Copilot 
![[Pasted image 20251102124616.png]]
### Key points:
- LLM never calls backend directly, it just generates WIQL.
- The user is the gateway to prompt calling backend endpoints.
## Or...
Call Azure REST API from frontend?? [Using Azure DevOps REST API]
# To Check Out 
[Azure DevOps REST API Documintation](https://learn.microsoft.com/en-us/rest/api/azure/devops/?view=azure-devops-rest-7.2)