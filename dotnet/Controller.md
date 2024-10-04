---
id: Controller
aliases: []
tags: []
---

Controller classes inherit "ControllerBase". 
and are where all the routing happens.

have to add this line in Program.cs
```C#
builder.Services.AddControllers(); // finds classes that are inherited from ControllerBase
```

example:
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using firstapi.Data;
using Microsoft.AspNetCore.Mvc;

namespace firstapi.Models.Controllers
{
    [Route("api/[Controller]")]
    //[Route("api/stocks")]
    [ApiController]
    public class StocksController : ControllerBase
    {
        private readonly ApplicationDBContext context; //variable
        
       public StocksController(ApplicationDBContext _context) //constructor
       {
            context = _context;
       } 
        
        [HttpGet] //request type
        public IActionResult GetAll() //function to return all stocks
        {
            var stocks = context.Stocks.ToList();
            return Ok(stocks);
            // return NotFound();
        }
        [HttpGet("{id}")] // function to return a single stock identified by id
        public IActionResult GetByID([FromRoute]int id)
        { 
            var stock = context.Stocks.Find(id);

            if (stock == null)
            {
                return NotFound();
            }
            return Ok(stock);
        }
    }
}
```

