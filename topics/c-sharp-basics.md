# C# Basics

### Data Types
In C#, you define the [types of your variables](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/built-in-types-table). That type is invariant and cannot be changed.
```cs
string yourInstructor = "Nathan"; // double quotes are required for strings
```
If you would like your string to include non-visible characters like new lines, then you can use a verbatim string literal with an `@` sign before the quotes.
```cs
string poem = @"
Roses are red
Violets are blue
; expected
On line 32
";
```

You can get a single character from a string by accessing the index position of the character.
```cs
char firstLetterOfPoem = poem[1]; // R
```

```cs
char lastLetter = 'Z'; // single quotes are required for characters
```
```cs
int nssAge = 6;
```
```cs
bool isCool = true;
```

Everything "inherits" from `object`. You'll learn more about inheritance later, but it's usage is not all that dissimilar to the `extends` keyword that you've been using with React. Below is an example of [boxing](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/boxing-and-unboxing) data into it's inherited type. :boxing_glove:
```cs
// Avoid this behavior
object myCustomThing1 = ""; // a boxed string
object myCustomThing2 = ''; // a boxed char
object myCustomThing3 = 0; // a boxed int
object myCustomThing4 = true; // a boxed bool
```
Arrays are available in C#, but the syntax is slightly different. There are also more convenient replacements for an array. More on that later.
```cs
string[] instructors = { "Nathan", "Martin", "Ben" };
int[] favoriteNumbers = new int[3] { 42, 52, 111 };
// initialized to length of 3  ^^^
// What happens if you try to add a 4th entry to favoriteNumbers?
favoriteNumbers[3] = 13;
```

### String Concatenation
There are [several ways to combine strings](https://docs.microsoft.com/en-us/dotnet/csharp/how-to/concatenate-multiple-strings) in C#.
```cs
string firstName = "Martin";
string firstNameAndMiddleInitial = firstName + " " + "N";
Console.WriteLine(firstNameAndMiddleInitial) // Martin N
```
One of the easiest ways to inject variables in a string is to use string interpolation.
```cs
string fullName = $"{firstNameAndMiddleInitial} Cross";
int age = 35;
var intro = $"My name is {fullName} and I'm {age} years old";
/*
BTW, you can use `var` instead of the type
 and the compiler will infer the type for you.
*/
```

There's also a utility in .NET called StringBuilder to... well... build strings.
```cs
var sb = new StringBuilder();
sb.Append("that's ")
    .Append("what ")
    .Append("she ")
    .Append("said.");
sb.ToString(); // that's what she said
```
Also, notice that `new` keyword? That creates an instance of the StringBuilder class for you to use. We'll cover more on classes soon.

### Default Values & Nullability
C# value types have a variety of [default values](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/default-values-table), particularly if they are prohibited from being set to null.
```cs
bool inClass; // defaults to false
int countOfStudents; // defaults to 0
char letterGrade; // defaults to '\0'
string groupName; // string is a special one. It defaults to null.
```

If you want one of the value types to allow assignment of null, then you can suffix the variable type with `?`.
```cs
bool? inClass = null;
int? countOfStudents = null;
char? letterGrade = null;
```

### Logical Operators
- [C# operators](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/)

	- C# does not have type coercion :raised_hands: so the only way to check for equality is `==`.
	- There are also a variety of type checking/casting keywords such as [`is` v. `as`](https://stackoverflow.com/a/3786390), [`is` with type pattern matching in C# 7](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/is#-type-pattern-), or just brute force [casting](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/casting-and-type-conversions#explicit-conversions).

### Control Flow in C#
- Branching
	- `if` :twisted_rightwards_arrows: `else`
	- `switch`
- Looping
	- `for`, `foreach`, `while`, `do` :arrow_right_hook: `while`
	- [`continue`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/continue) v. [`break`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/break)
	- `return` v. `throw`
- [`try` and `catch` Exceptions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/exceptions/index)
- [`async` and `await`](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/control-flow-in-async-programs)

***

##### Exercises

- [C# Tutorial on Repl.it](https://repl.it/community/classrooms/20702)
- [LetterLoops](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/exercises/LetterLoops.md) :abc: :arrows_clockwise:
- [Number Multiplier](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/exercises/NumberMultiplier.md)

Let's go through [this exercise](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/02_FIRST_EXECUTABLE.md) to get an idea of some of the primary differences between C# and JavaScript, and learn a few extra commands that make our [command line interactive](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/13_CLI_IO.md).

> You can also optionally begin [Koans](https://github.com/NotMyself/DotNetCoreKoans) which are test driven way to understand the language syntax and available data structures. It's best to take your time and make sure you understand each section before progressing. Just making the test pass doesn't mean you learned the lesson. If you reach a section that we haven't covered, feel free to do some preliminary research until class covers that concept.

***

## How can I talk about what I'm learning?

[.NET can mean a lot of things](https://www.microsoft.com/net/learn/what-is-dotnet). It is a complex ecosystem and you're only going to get experience with a part of it here in class.

[.NET Core & .NET Framework are different](https://docs.microsoft.com/en-us/dotnet/standard/choosing-core-framework-server). _.NET Framework_ requires a Windows (virtual) environment. _.NET Core_ is newer, different, and can run on multiple operating systems, but several features overlap between the two frameworks.

[NuGet](https://www.nuget.org/) (newget, not nugget) is a package manager for .NET, similar to how you you've used `npm` in the frontend class.
