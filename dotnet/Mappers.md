Mappers are basically creating public function to turn a default model object into another object with less info depending on what is necessary on the request.

[example](https://github.com/teddysmithdev/FinShark/blob/master/api/Mappers/StockMappers.cs)
all the functions in this file turn a Stock object into other Stock Objects identified in the [[Data Transfer Objects (DTO's)]] files