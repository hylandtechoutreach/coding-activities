# <span>C#</span>: ASCII Art
An activity to introduce C# in 45-60m. **C#** is an object-oriented programming language, often used to make desktop applications. This lesson covers console output and methods. The goal of the lesson is to build a simple piece of [ASCII art](https://en.wikipedia.org/wiki/ASCII_art) using the C# console.

## Setup
Follow the [Setup](Setup.md) guide to get ready to build an introductory program with `repl.it`!

## Introduction to ASCII Art
**ASCII Art** is a graphic design technique that uses text characters to create images.

### Examples
Check out some examples of ASCII Art here: [imgur.com/a/u9Rjhov](https://imgur.com/a/u9Rjhov)

![](https://i.imgur.com/x45b2mV.png)

![](https://i.imgur.com/28xDLDY.jpg)

![](https://i.imgur.com/LY7fELk.png)

## Drawing a Bunny in <span>C#</span>
Start by placing this bunny in a text file:

```
 () ()
 (^ ^)
 (___)
```

Using the C# console, it is possible to create interesting text-based art (like bunnies) using `Console.WriteLine`. Right now, it should show some text containing a message, but it can show any text at all! A developer simply needs to write out each line of ASCII text in the proper order. Try to recreate the bunny in the C# console!

1. Remove the existing code from **body** of the `Main` method
1. Add a `Console.WriteLine` statement to draw the bunny's ears
1. Add another `Console.WriteLine` statement to draw the bunny's face
1. Add a third `Console.WriteLine` statement to draw the bunny's body
1. Add an empty `Console.WriteLine` statement to add some space under the bunny
1. Make sure each piece of text starts with a space
1. Click the "run" button to see the bunny appear in the console!

```cs
using System;

class MainClass {
  public static void Main (string[] args) {
    Console.WriteLine(" () () ");
    Console.WriteLine(" (^ ^) ");
    Console.WriteLine(" (___) ");
	Console.WriteLine();
  }
}
```

### Setting the Console Colors
It is possible to change the colors of the C# console. There is a [limited set](https://docs.microsoft.com/en-us/dotnet/api/system.consolecolor?view=netframework-4.8) of colors, but they can make the console a little bit more fun.

At the top of the body of the `Main` method, add the following code:

```cs
Console.BackgroundColor = ConsoleColor.Cyan;
Console.ForegroundColor = ConsoleColor.DarkBlue;
Console.Clear();
```

This will set the colors, and then clear the existing console so that the colors apply to everything. Make sure the capitalization is consistent!

Try out a few different colors to see what works.

### Challenge: Drawing Multiple Bunnies
Instead of drawing one bunny, draw a few bunnies lined up vertically. Use `Console.WriteLine()` to put an empty line in between them. Try to make all of the bunnies look the same!

## Using Methods
The code starts to get a little more disorganized with each additional bunny. There is a lot of repeated code that does the exact same thing, and it becomes difficult to maintain. Luckily, methods can make this code better!

A **method** is a block of code that runs when it is called. This allows developers to reuse code; they can define the code once, and use it many times.

### Questions
>Q: Where is there already a method in the program?
>A: The `Main` method! This is the entry point for the exeuction of a C# program.

>Q: For this program, what kind of method could help simplify the code?
>A: How about a method to draw a bunny!

### Defining the Method
1. _Under_ the `Main` method (after the `}`), start defining the method with `public static void`
    - These keywords set certain things about the method. They are outside of the scope of this lesson
1. Add the _name_ of the method: `DrawBunny`
1. Add parentheses and curly brackets (`() {}`)
1. Click in between the opening and closing curly brackets and press the `Enter` key
1. In the _body_ of the `DrawBunny` method, add the code to draw a bunny!

```cs
public static void DrawBunny() {
    Console.WriteLine(" () () ");
    Console.WriteLine(" (^ ^) ");
    Console.WriteLine(" (___) ");
    Console.WriteLine();
}
```

### Calling the Method
1. Remove all of the bunny-drawing code from the body of the `Main` method
    - Be sure to keep the console color code though!
1. _Call_ the `DrawBunny` method in the code with `DrawBunny();`
1. Add a few additional method calls under the first one
1. Click the "run" button to run the code and see the bunnies appear!

### Adding Whiskers
One of the best things about methods is that if a developer wants to update code, they only have to do it in one place. For example, to add whiskers to the bunny, it is only necessary to change one line of code instead of several. This change will apply to every method call!

1. In the `DrawBunny` method, find the line that draws the bunny's face
1. Add a greater-than sign (`>`) on the left side of the bunny's face
1. Add a less-than sign (`<`) on the right side of the bunny's face
1. Click the "run" button to run the code again and see each bunny appear with whiskers!

### Challenge: An Additional Bunny Method
Define a _new_ method under the existing method to draw the same bunny, but using an `o` for the eyes! The method definition should look almost exactly the same as the `DrawBunny` definition, but it should have a new name (`DrawBunny2`) and have `o` instead of `^` in the `Console.WriteLine` for the face.

### Code
```cs
using System;

class MainClass {
	public static void Main (string[] args) {
		Console.BackgroundColor = ConsoleColor.Cyan;
		Console.ForegroundColor = ConsoleColor.DarkBlue;
		Console.Clear();
		
		DrawBunny();
		DrawBunny();
		DrawBunny();
	}

	public static void DrawBunny(string eye) {
		Console.WriteLine(" () () ");
		Console.WriteLine(">(^ ^)<");
		Console.WriteLine(" (___) ");
		Console.WriteLine();
	}
}
```

## OPTIONAL: Method Parameters
The two methods, `DrawBunny` and `DrawBunny2`, are very similar. What are the differences?

- The method names
- The character used for the eyes

Instead of writing these two methods that are almost identical, it is possible to use method parameters to make the _one_ method a little more dynamic. **Method parameters** allow developers to pass information to methods when they are called, so they can do different things depending on that information.

For this program, the **eye** is what will change with different method calls. The `eye` could be any piece of text at all, so the code in the body of the `DrawBunnyEye` method should not draw any eyes directly! Instead, it should insert the `eye` into the text dynamically.

1. Under the existing method definitions, define a _new_ method named `DrawBunnyEye`
    - Copy the existing definition for `DrawBunny`, but change the name
1. Add a _parameter_ within the parentheses in the method definition: `string eye`
1. Update the code so that instead of using `.` for the eye, it uses whatever the user passed in (`eye`):  
    ```cs
    Console.WriteLine($">({eye} {eye})<");
    ```
1. In the body of the `Main` method, _call_ the `DrawBunnyEye` method, but put `"^"` inside the parentheses
1. Call the `DrawBunnyEye` method with a couple other `eye` values
1. Remove the other method definitions and calls, as they are no longer necessary
1. Click the "run" button to run the code again, and see the bunnies with all the different eyes!

## Final Code
```cs
using System;

class MainClass {
	public static void Main (string[] args) {
		Console.BackgroundColor = ConsoleColor.Cyan;
		Console.ForegroundColor = ConsoleColor.DarkBlue;
		Console.Clear();
		
		DrawBunnyEye("^");
		DrawBunnyEye("$");
		DrawBunnyEye("0");
	}

	public static void DrawBunnyEye(string eye) {
		Console.WriteLine(" () () ");
		Console.WriteLine($">({eye} {eye})<");
		Console.WriteLine(" (___) ");
		Console.WriteLine();
	}
}
```

## Next Steps
Try to create some different works of text-based art! Find some online by Google searching "ASCII Art" or make up your own! It can be helpful to start in Notepad before trying to write code.

>NOTE: Using the backslash (`\`) character can cause issues when writing text to the screen. To avoid this, use `\\` instead of `\`, and only one `\` will appear.