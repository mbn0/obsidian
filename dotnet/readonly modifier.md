- In C#, the readonly modifier is used to declare fields in a class (or struct) that can only be assigned a value during their declaration or within the constructor of the class. 

example: 
```C#
class Person
{
	private readonly string firstname;
	private readonly string lastname;
	private readonly DateOnly birthday;

	public Person(string first, string last, DateOnly birth)
	{
	firstname = first; lastname = last; birthday = birth;
	}
}
```


- Unlike `const`, which requires a value to be assigned at the time of declaration and the value must be a compile-time constant, `readonly` fields can be assigned values at runtime, particularly in constructors.