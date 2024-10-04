# async
when a method is declared as async, it means that other operations could continue without blocking the method in case the method takes time.

# await
specifies which operations should be run async. it needs to be followed by an async method (e.g SelectAsync, ToListAsync) most methods from database context can use async.


example:
```C#
[HttpGet]
public async Task<IActionResult> GetAll()
{
    //for normal(sync):
    //var stocks = await context.Stocks.ToList()
    //  .Select(s => s.ToStockDTO())    

    //for async:
    //var stocks = await context.Stocks.ToListAsync().SelectAsync(s => s.ToStockDTO());
    //or:
    var stocks = await context.Stocks.ToListAsync();
    var stocksDTOs = stocks.Select(s => s.ToStockDTO())    if (stocks == null || !stocks.Any())
    {
        return NotFound();
    }
    return Ok(stocks)}

```
# Task and Task\<T>
these are return types for the async methods, Task if the method returns nothing, and Task\<T> if it returns something.j

