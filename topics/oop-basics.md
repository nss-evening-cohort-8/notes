# Object Oriented Programming (OOP) Basics

### Classes
[Classes](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/03_CLASSES.md) are the blueprints for your application. All classes _**must**_ be instantiated with the `new` keyword before any of their properties or methods can be accessed or used, unless they use the `static` keyword.

If you've used classes in JavaScript, then C# is semantically similar; even if JavaScript's implementation is syntactic sugar. You always need to create an instance of a class prior to using it.

> [C# accessibility levels](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/accessibility-levels) are a popular, trivia style, question in interviews.

### Properties and Fields
[Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties) & [Fields](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/fields) are provided as a way to store the state of your class. Idiomatic C# states that fields should be prefixed with an underscore (`_myPrivateField`) and properties are named using Camel Caps (`MyPublicProperty { get; set; }`).

There is a special version of Properties called _**Auto Properties**_ that include the default getter and setter for the property.
```cs
public string HomeAddress { get; set; }
```
You can also customize the accessibility of the getter or setter.
```cs
public SocialSecurityNumber { get; private set; }
```

Fields and Properties can be functionally equivalent, but idiomatically speaking, Fields are intended for the internal state of the class and Properties are used to expose values to other areas of the application.

### Methods
You should already be familiar with [methods](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/04_METHODS.md). They are simply functions attached to an object (or instantiated Class) that perform an action.

Take a moment to familiarize yourself with what makes up a [method signature](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/methods).
```cs
public class Kangaroo
{
  public void Jump(int howHigh) // <-- method signature
  {
    // make the kangaroo jump
  }
}
```

[Constructor methods](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/concepts/csharp-language/constructor-methods.md) are used for designing the initial state of your class
```cs
public class Whozit
{
    public Whozit() // Named after the class it constructs
    {
        // initial state
    }
}
```

### Namespaces
[Namespacing](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/05_NAMESPACING.md) is just a roadmap for the compiler to follow through your code. If you put something in a different namespace, then the compiler in Visual Studio (msbuild) won't be able to find it until you include that new namespace with `using`.
> A `using` statement is semantically equivalent to `require` or `import` in JavaScript.

##### Exercises

1. Your favorite things
	- Create at least four classes, each representing one of your favorite things. Something generic like a book, a car, or a beach.
	- Give each of these things two or more properties (attributes) like Bio, Name, etc.
	- Give each of these things two or more methods (behavior) like Open, Fly, etc.
		- At this point, your methods only need to Console.WriteLine sentences to represent the behavior.
	- Inside your `Main` method, create at least two instances of each of your favorite things.
		- For instance, one of my favorite things are pets. My `Main` method might look like this.
			```cs
			var pickle = new Pet
			{
			    Name: "Pickle",
			    Type: Pet.Cat, // <-- an enum
			    Age: 13
			};
			var data = new Pet
			{
			    Name: "Data",
			    Type: Pet.Dog, // <-- an enum
			    Age: 0.5,
			};
			```
	- Access each of your instantiated favorite things and print the attributes and behaviors to the console in any way you want. For example:
		```cs
		Console.WriteLine(data.Speak("feed me"));
		// Data says "bark bark"
		```

1. Construct some Lego Minifigure Classes and make them do stuff

	That's basically it. Here's a reminder about Properties and Methods.
	###### Properties

	Hair/Hat, Head, Torso, Legs, Accessories, etc.

	###### Methods

	If you were working at [Tt Games](http://www.ttgames.com/), your minifigure classes might have actions associated with them in the form of jump, double jump, attack, special attack, look & move methods.

	There might even be certain conditions that must be met to construct (or unlock) a new character or other kind of object.
	- You don't actually need to write any functionality in these methods right away. If you just want to "stub out" a method, but you still want to see if your code compiles, you can insert this line into your method body in lieu of functionality like Console.WriteLine.
		```cs
		throw new NotImplementedException();
		```

- Bangazon
	- [Corporate Class](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/exercises/05_CLASSES.md)

- [Jungle Overloading](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/exercises/bangazon/BANGAZON_03.md)

- [Syntactic Sugar in C# 6](https://github.com/nss-evening-cohort-8/bangazon-inc/blob/master/orientation/exercises/06_%20EXPRESSION_FN_MEMBERS.md)
