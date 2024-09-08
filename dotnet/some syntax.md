# foreach loops
## an example using for loop:
```C#
var names = new List<string> {"Scott", "Ana", "Felipe" };

for (int i = 0; i < names.Count; i++)
{
Console.WriteLine($"hello {names[i]}");
}
```
## an example using foreach loop:
```C#
var names = new List<string> {"Scott", "Ana", "Felipe" };

foreach (var name in names)
{
Console.WriteLine($"Hello {name}");
}
```
## Declaring Lists

```C#
// different ways to declare lists
var names = new List<string> { "Scott", "Ana", "Felipe" };
List<string> namess = ["Scott", "Ana", "Felipe"];
var names = new HashSet<int>();
```
## Declaring Arrays

```C#
// different ways to declare arrays
string[] days = ["Scott", "Ana", "Felipe"];
string[] dayss = new string[]{"Scott", "Ana", "Felipe"};
int[] num = new int[3];
int[] scores = [97, 92, 81, 60];
var daysss = new string[]{"Scott", "Ana", "Felipe"};
```
