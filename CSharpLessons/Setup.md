# Repl Setup for <span>C#</span>
Start any C# activity by going to `repl.it` and setting up a new C# project.

1. Go to [repl.it](https://repl.it)
1. In the upper right corner, click the "+ new repl" button
1. Scroll down and select "C#" from the Language list
1. Click the "Create Repl" button
1. Make a note of the name of the Repl; it will be automatically saved to that URL, and will be accesible from anywhere!

## Repl Overview
**`repl.it`** is a website that allows developers to _write_ and _run_ code right from a web browser!

![](https://i.imgur.com/7jhKrt9.png)

- **Code Editor** - This is where developers write code
- **Run Button** - Developers click this button to _execute_ the code
- **Run Area** - This is where the developer sees the results of the code

In the new Repl, click the "run" button to see the code _execute_!

### A New Message
Update the message so that instead of saying "Hello World" it says something else!

## TIP - C# Script Structure
In the code, there is a lot of boiler-plate code that sets up the program. These parts of the code may be outside of the scope of this lesson. All that matters for simple scripts is the code between the `{` and `}` where the `Console.WriteLine` is now. This part is called the **body** of the `Main` method. All the rest can be ignored to start.

```cs
using System;

class MainClass {
	public static void Main (string[] args) {
		// IMPORTANT STUFF GOES HERE
	}
}
```

### TIP - Specific Syntax
Make sure every piece of code is **exactly** correct. C# is very particular, and if one letter is wrong, the whole program could crash.

Here are some basic rules that can help deal with these errors:
- Statements should end with semi-colons (`;`)
- Any text to show the user should have an opening AND a closing quotation mark (`""`)
- Make sure capitalization is consistent
- Make sure parentheses open AND close (`()`)