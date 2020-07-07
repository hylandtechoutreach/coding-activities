# <span>C#</span>: Choose Your Own Adventure
An activity to introduce C# in 45-60m. **C#** is an object-oriented programming language, often used to make desktop applications. This lesson covers input/output from the console, variables, and conditional statements. The goal of the lesson is to build a simple [Choose Your Own Adventure](https://en.wikipedia.org/wiki/Choose_Your_Own_Adventure) game using the C# console.

## Setup
Follow the [Setup](Setup.md) guide to get ready to build an introductory program with `repl.it`!

## User Input
The Choose Your Own Adventure game should allow the user to decide how the story plays out. To do that, the program must ask a question, and remember the user's answer. 

1. Add another `Console.WriteLine` statement under the first one, and make it say "You wake up. What do you do?"
	- Make sure everything is capitalized correctly
	- Make sure there are parentheses (`()`) and quotes (`""`)
	- Make sure there is a semi-colon (`;`) at the end of the statement
1. Under the `Console.WriteLine` statement, add another statement to _read_ the user's answer:  
	```cs
	string answer = Console.ReadLine();
	```

Now `answer` is a variable that holds the answer from the user. A **variable** is a name that points to a value in the code. A variable can hold anything, and the program can even change what it holds. For now, the `answer` variable allows the program to remember the user's _answer_ to the question.

1. Make another new line under the `string answer` statement, and add a `Console.WriteLine`
1. Make the statement say "You said "
1. After the "You said " ending quote, add `+ answer` so that the answer is added to the end of the message:  
	```cs
	Console.WriteLine("You said " + answer);
	```
1. Run the program, and test that the user's answer to the question is said back!

## Branching
Now, the program should change the story based on the user's answer. This is possible with `if` statements. These work just like in English; for example, "**if** it is raining, I will stay indoors." For the story, the program can create different outcomes in this way.

1. Create a new line under the last `Console.WriteLine` statement
1. Add an `if` statement to check whether the `answer` is equal to the text "Go back to sleep":  
	```cs
	if (answer == "Go back to sleep")
	```
1. Add curly brackets (`{` and `}`) to open up the **body** of the `if` statement
	- All of the code in between those brackets will only run _if_ the check is true!
1. Create a new line after the opening bracket (`{`)
1. On the new line, add a `Console.WriteLine` saying "You sleep happily."
1. Run the code, and check that the next line appears when entering "Go back to sleep"

### Code
```cs
if (answer == "Go back to sleep") {
	Console.WriteLine("You sleep happily.");
}
```

## Another Answer
Now the program can respond to one answer, but what about another one? Use another `if` statement to check if the user entered a different answer.

1. After the closing curly bracket (`}`) for the `if`, make a new line and add a new `if` statement
1. In the parentheses, check if `answer` is equal to the text "Get up"
1. Add opening and closing curly brackets after the parentheses
1. Within the curly brackets, add a `Console.WriteLine` to say "You get out of bed."
1. Run the code, and check that the proper line appears when entering "Get up"

### Code
```cs
if (answer == "Get up") {
	Console.WriteLine("You get out of bed.");
}
```

## Continuing the Story
After the user gets out of bed, the program can again ask how to proceed. Everything within the curly brackets of the second `if` will run only _if_ the user said to get up. So, it is possible to ask another question within that branch!

1. Under the "You get out of bed" line, add another `Console.WriteLine` asking the user what they would like to do next
1. Use `Console.ReadLine` again to take in the user's answer, and store it in a variable named `answer2`
1. If the user says to go to school, write a message saying "You learn a lot at school!"
1. Otherwise, if the user says to go to the movies, write a message saying "You get in trouble :("
1. Run the code, and test that the different branches work as expected!

## Final Code
```cs
using System;

class MainClass {
    public static void Main (string[] args) {
        Console.WriteLine("Welcome to my game!");
        Console.WriteLine("You wake up. What do you do?");
        string answer = Console.ReadLine();

        if (answer == "Go back to sleep") {
            Console.WriteLine("You sleep happily.");
        }

        if (answer == "Get up") {
            Console.WriteLine("You get out of bed.");
            Console.WriteLine("What do you do next?");
            string answer2 = Console.ReadLine();

            if (answer2 == "Go to school") {
                Console.WriteLine("You learn a lot at school!");
            }

            if (answer2 == "Go to the movies") {
                Console.WriteLine("You get in trouble :(");
            }
        }
    }
}
```

## Next Steps
Try to continue the story with some new branches! Write it out on paper or in Notepad first to get an idea of where the story should go. Then, try to update the code to make it into a playable game! Feel free to elaborate on the existing story, or change it completely. Have fun!