## error handler has three public functions
### 1- `handleHttpError()`
	-  Detects if the issue is from the client-side or server-side
	- creates a readable message.
	- logs it
	- shows a notification using [[notification.service.ts]]
###  2- `handleFormValidationErrors()`
###  3- `handle ApplicationError()`

## and three private functions used inside the public ones
- `getMessageFromStatus()`
- `getErrorTypeFromStatus()`
- `getValidationErrorMessage()`