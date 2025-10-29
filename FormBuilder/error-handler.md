---
tags:
  - "#core"
  - services
---
# error handler has three public functions
### 1- `handleHttpError()`
- Detects if the issue is from the client-side or server-side
- creates a readable message.
- logs it
- shows a notification using the [[notification.service.ts|notification service]]
###  2- `handleFormValidationErrors()`
- Takes Angular form validation errors and turns them into clear, user-friendly texts
- combines error messages from different fields that are generated using `getValidationErrorMessage()` into one long message
###  3- `handle ApplicationError()`
- Handles errors on runtime (not HTTP errors)
- logs the error, and shows a notification to the user
# and three private helper functions used inside the public ones

### 1- `getMessageFromStatus()`
- Converts HTTP status code (404, 501) into human-readable message.
### 2- `getErrorTypeFromStatus()`
- Decides whether it is an error or a warning (decides how to call notification service)
### 3- `getValidationErrorMessage()`
- gives an error message to a single feild.