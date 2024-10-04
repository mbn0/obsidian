## Example
```C#
// Specify the data source.
int[] scores = [97, 92, 81, 60];

// Define the query expression.
IEnumerable<int> scoreQuery =

	from score in scores
	where score > 80
	orderby score descending
	select score;

// Execute the query.
foreach (var i in scoreQuery)
{
	Console.Write(i + " ");
}
// Output: 97 92 81
```

- the `IEnumerable<T>` can be used on any type of data. For more info check [[Interfaces in CSharp]]
- The value of scoreQuery is not calculated until it is called.

## another way to write it
```C#
int[] scores = [97, 92, 81, 60];

var scoreQuery = scores.Where(s => s>80).OrderByDescending(s => s);

foreach (var i in scoreQuery)
{
	Console.WriteLine(i + " ");
}
```

check: https://learn.microsoft.com/en-us/dotnet/csharp/linq/