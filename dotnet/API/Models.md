## Models folder
this is where models are created(duh) similar to django.
each file is a single model or table in the database (as far as i know)
### example:
```C#
﻿using System.ComponentModel.DataAnnotations;

namespace MoviesMenuAPI.Models;

public class Movie
{
    [Key] // to identify the primary key
    public int? Id { get; set; } // question mark to set as nullable

    [Required] // ensure it is not null
    public string? Title { get; set; } // confilct? 

    [Required]
    public string? Director { get; set; }

    [Required]
    public int? ReleaseYear { get; set; }

    [Required]
    public string? Genre { get; set; }

    [Required]
    public decimal? Price { get; set; }
}
```
from : [buudi's MoviesMenuAPI(love you bro)](https://github.com/buudi/MoviesMenuAPI/blob/master/MoviesMenuAPI/Models/Movie.cs)

# Primary key
if the primary key is not specified, EF Core will search for one by looking for `Id` in the name.

[[(dotnet) Connecting to DB and migrating]].