---
tags:
  - feature
---
# Requirements
add a feature to the system to add a dataset by uploading a postman collection folder.
# Actions
-  Added new button in `dataset-list` component.
 - Created new component, `postman-dataset`. 
 - Dataset can now be added by pasting the JSON inside a text box.
# Needs to be considered
- Bulk addition of endpoints (parked for now)
- uploading file instead of JSON (parked)
- ability to upload swagger collections as well.
# Logical Errors
- After adding an endpoint using postman, when trying to edit it you face an issue with URL because Postman collections use an IP address (is that default?)which the form does not recognize as a valid URL
- when saving multiple datasets with save name and description, no error is retrieved, normal response and nothing happens.

# Design Issues
- if endpoint name or URL is too long it exceeds the box for it in the postman-addition page
- Temp fix: truncate link string if it exceeds 30 characters. issue: not dynamic, does not scale with window size.
# Interfaces
Interfaces inside the component (all private, nothing exported)
- `PostmanCollection` has:
	- `PostmanItem` has: 
		- `PostmanRequest`
		- `PostmanItem` (recursive)
		
- `ParsedEndpoint`
# Functions 
A list of helper functions and their explanation
### - `extractEndpoints()`
- Recursively extract endpoints from Postman items.
### - `extractParametersFromRequest()`
- Extracts parameters from a request (body and URL) and calls
	- `extractParametersFromUrl()`
	- `extractParametersFromBody()`
		- checks for the type of body and calls a proper function from:
		- `extractParametersFromJsonObject()`
		- `extractVariablesFromText()`
