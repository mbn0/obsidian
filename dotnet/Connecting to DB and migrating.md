After writing the [[dotnet/API/Models]], do the following.
write `ApplicationDBContext`class
an example for it: 
```C# 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using firstapi.Models;
using Microsoft.EntityFrameworkCore;

namespace firstapi.Data
{
    public class ApplicationDBContext : DbContext  
    {
       public ApplicationDBContext(DbContextOptions dbContextOptions) 
       : base(dbContextOptions) //passing the value to the DbContext constructor
       {
         
       } 

    public DbSet<Stock> Stocks { get; set; }
    public DbSet<Comment> Comments { get; set; }

    }
}
```

in the Program.cs file, write:
```C# 
builder.Services.AddDbContext<ApplicationDBContext>(Options => 
    Options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection"))
);
```

`DefaultConnection` can be defined like this inside the `appsettings.json` file:
```Json
  "ConnectionStrings": {
    "DefaultConnection": "Server=172.17.0.2;Database=testing;User Id=sa;Password=Testing@123;TrustServerCertificate=True;"
  },
```

or as a secret by using:
```bash
dotnet user-secrets init
dotnet user-secrets set "ConnectionStrings:DefaultConnection" "Server=localhost;Database=MyAppDb;User Id=sa;Password=yourPassword123;"
```

now to make migrations we will use:
```bash
dotnet ef migrations add init 
```
if not working try this first:
```bash
dotnet tool install --global dotnet-ef
```

finally, to migrate use: 
```
dotnet ef database update
```