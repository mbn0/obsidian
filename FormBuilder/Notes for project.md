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
and in components/shared/app-dialog (mostly used)

## Get endpoints with POST header? 
![[Pasted image 20251030120445.png]]

# Detailed Issues
- [[Tester Component Issues]]
- [[Form Creation Issue]]
