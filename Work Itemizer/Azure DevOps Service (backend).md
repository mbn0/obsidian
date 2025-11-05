---
tags:
  - backend
  - services
  - documentation
---
# Main Methods
- `GetWorkItemsAsync()` to get work items for a project
- `GetProjectsAsync()` to get all projects using user's PAT.
- `GetTeamMembersAsync()` to give the bot some context about the project.
- `ExecuteGenericRequestAsync()` to execute REST API calls to the backend.
- `ExecuteWIQLAsync()`  @deprecated.

# Helper Methods
- `ExecuteRequestAsync()` to execute HTTP request with PAT auth and return JSON response
- `FetchWorkItemDetailsAsync()` fetch work items details from ID's
- `ExecuteWiqlForIdsAsync()` @deprecated to  Execute WIQL query and return work item IDs.