- the directive "FieldOptionsDirective" is not being used anywhere inside the project folder.


## No encryption for passwords when adding database connections or datasets
## Port commented while building SQL Server Connections

 in file `DatabaseConnectionRepository.cs`, the duplicated function `BuildConnectionString`, the port is commented out of `DataSource` info, which causes `SqlConnectionBuilder` to default to 1433. which means the user input in the field is not taken into account.
When uncommented: 
- works as expected for `testingConnection`
- no info of how it works with `ExcuteDatabaseQuery`
Action taken: 
- uncommented port in function for connection testing
- left the original function (inside `ExcuteDatabaseQuery`) as is.
## Two components with the same selector.
app-dialog in components/form-designer/components/dialog
and in components/shared/app-dialog
## tester-component
The tester component has many issues, including:
- Dynamic sizing issue.
- `skipValidation()` function giving two notifications in the end of form, (1- validation skipped, 2- end of form)
- icon unknown issue.
- no error message when string is typed into number field 
- repeated boxes around same field 

![[Pasted image 20251020132000.png]]

## form creation
- the preview does not show actual components but rather a simplified version.
- unknown error when trying to save changes in form `noureddine testing`
![[Pasted image 20251020134341.png]]
![[Pasted image 20251020134416.png]]

