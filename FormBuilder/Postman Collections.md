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
- Bulk addition of endpoints
- uploading file instead of JSON
- ability to upload swagger collections as well.
# Logical Errors
- After adding an endpoint using postman, when trying to edit it you face an issue with URL because Postman collections use an IP address which the form does not recognize as a valid URL
# Design Issues
- if endpoint name or URL is too long it exceeds the box for it in the postman-addition page