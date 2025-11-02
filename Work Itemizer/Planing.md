# Requirements

A chatbot interface for Azure DevOps where the user can ask about work items, add them, delete them, and stuff.
# Ways to connect with Azure DevOps Work Items

## 1. Using Azure DevOps REST API 

## 2. Using Azure DevOps SDKs (Current Plan)
[[Testing AzureDevOps SDK|Testing Azure DevOps SDK]]
# Approaches

# 1. Make the Chatbot Create a Custom Query
The user requests a certain thing from the chatbot, the chatbot creates a proper Query.
# 2. Make the Chatbot Answer
Also has two approaches: 
1. The chatbot receives all data and answers depending on it.
2. The chatbot requests data depending on question.
# How to make the chatbot call the backend??
## Static Backend Calls (~~Current Plan~~) Canceled
Note: This was cancelled because the chatbot has to call different stuff anyways.
- Make a single endpoint to retrieve all Work Items from the backend 
- Make endpoints for addition, Bulk Addition
- Give all info to the chatbot and let it answer according to that.
## Custom WIQL Calls (Current)
 After the user asks a question, the bot is prompted to create a WIQL Query, so he requires the user the necessary info to create the Query (Such as project name, person name, etc.)
After that, the query created by the LLM is shown to the user and the user is prompted to allow sending this query to the backend or not.
- (check if work items are less than 1000, if so give them to chatbot as context.)
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

# Does The Project Need a database?
Short answer is: NO
Long answer is: 
A database is beneficial in case of:
- if caching is required,
- saving user preferences.
# is a RAG required? 
NO
# Is using the PAT in the frontend safe? 
Probably, since access to source control is only available in the company's network.

Call Azure REST API from frontend?? [Using Azure DevOps REST API]
# To Check Out 
[Azure DevOps REST API Documentation](https://learn.microsoft.com/en-us/rest/api/azure/devops/?view=azure-devops-rest-7.2)