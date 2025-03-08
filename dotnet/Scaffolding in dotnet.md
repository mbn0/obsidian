---
id: Scaffolding in dotnet
aliases: []
tags: []
---

scaffolding is the process of pulling the already-created database to the code in the database-first approach.

to scaffold, write the following command in the terminal:

```bash
dotnet ef dbcontext scaffold "Server=172.17.0.2;Database=task1;User Id=sa;Password=Testing@123;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer --output-dir Models
```
