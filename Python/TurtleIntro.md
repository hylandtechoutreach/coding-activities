# Python Coding Activity - Turtle Graphics
![](https://i.imgur.com/zVWdA5m.png) <- (not this kind of turtle)

In this activity, write a **Python** application and play around with some two-dimensional graphics. It will provide a glimpse into the power of programming and show how fun it can be to write code!

## Python
[Python](https://en.wikipedia.org/wiki/Python_(programming_language)) is a popular programming language used by developers all over the world. It is a _general-purpose_ language, which means that developers can use it to write **scripts** that do almost anything: create websites, analyze large data sets, control robots, design video games... the list goes on and on!

### trinket
trinket is a website that allows a developer to write and run code in a web browser. It works in any browser, on any device! This makes it easy to practice coding and show off any programs that are created. During this activity, trinket will be used to build some cool Python programs.

### First Python Program - Hello World
The first program a developer normally writes when learning a new programming language is a "Hello World" program. The goal of these programs is to display a message of "Hello World" to the user. In Python, that program is fairly simple. Follow the steps below to create a Python "Hello World" program:

1. Navigate to https://trinket.io/python/93409853b0 to start building the program
1. Open the hamburger menu in the upper left, and select "Fullscreen" so it is easier to use
1. In the `main.py` file, type the Python command to print a message to the screen:   
    ```python
    print("Hello World")
    ```
1. Click the "Run" button to _run_ the program!

When a developer "runs" their program, they are telling the computer to execute all the code they wrote, and perform the commands they specified. **Commands** are like instructions in a recipe; they tell the computer what to do. Running the "Hello World" program in Python will print the message on the console screen.

#### Challenge: Change the Message
Update the simple "Hello World" program so that instead of saying "Hello World" it says something else!

## Python Library - Turtle Graphics Introduction
Python has a multitude of **libraries** that allow developers to use pre-existing code to build their own applications. One such library is for [turtle graphics](https://en.wikipedia.org/wiki/Turtle_graphics), which are vector graphics that use a cursor (or "turtle") to create images on a Cartesian plane.

### First Turtle Program
Remove any code from the `main.py` file so it is totally blank. Then, on the first line of the file, add the following command:  
```python
from turtle import *
```

This command tells the computer to bring in all the code from the `turtle` library so it is usable in the program! The next step is to create the turtle. First, add a blank line underneath the first line. Then, on the third and fourth lines of the file, add the following commands:
```python
koopa = Turtle()
koopa.shape("arrow")
```

These lines create a turtle and set its shape. In this case, the turtle is `koopa`, but the turtle could have any name. Click the "Run" button to see the "turtle" appear on the page!

#### Challenge: Change the shape to "turtle"
Update the code so that instead of setting the shape to `"arrow"`, it sets the shape to `"turtle"`. Run the program again to see the shape shift!

### Adding color
Black and white is boring, so we can add some color to the program! On the next line of the `main.py` file, add the following command:  
```python
koopa.color("green")
```

This command will turn the turtle green! Next, we can change the background color. Add a blank line, and then add the following commands:
```python
paper = koopa.getscreen()
paper.bgcolor("black")
```

These commands get the screen and set its background color to black. Run the program again to see the new colors on the page!

#### Challenge: Change the colors
Update the code so that instead of green and black, the turtle and the background have different colors. For example, the turtle could be blue, and the background could be pink!

## Turtle Graphics - Moving the Turtle
One of the most useful turtle abilities is the ability to move across the screen and draw like a pen! Create a blank line in the `main.py` file, and then add the following command on the next line:
```python
koopa.forward(50)
```

When the program runs, the turtle moves across the screen! Specifically, it moves **forward** `50` pixels in the direction it is currently facing (90 degrees).

It is also possible to turn the turtle. Add the following command on the next line:
```python
koopa.right(90)
```

This command turns the turtle `90` degrees to the **right**. Previously the direction of the turtle was 90 degrees (pointing to the right), so after turning 90 degrees to the right, the turtle should face down (180 degrees).

Run the program to see the turtle move to the right, then turn to face down!

### Drawing a square
Add the following commands to the file, under the existing commands:
```python
koopa.forward(50)
koopa.right(90)
koopa.forward(50)
koopa.right(90)
koopa.forward(50)
koopa.right(90)
```

Run the program to see what this code does. It should draw a square! How does that work? On a piece of paper, or on a whiteboard, try to draw the same square as the turtle:

1. Draw the top side from left to right
1. Turn the writing utensil and draw the right side from top to bottom
1. Turn the writing utensil and draw the bottom side from left to right
1. Turn the writing utensil and draw the left side from bottom to top

So, the turtle moves `50` pixels to the right, turns `90` degrees to face down, moves `50` pixels down, turns `90` degrees to face left, moves `50` pixels to the left, turns `90` degrees to face up, moves `50` pixels up, and finally, turns `90` pixels to face right once again!

#### Challenge: Make the square bigger
Currently, the square will be `50` pixels tall and `50` pixels wide. Try to change some of the numbers so that instead, the square is `100` pixels tall and `100` pixels wide!

## Turtle Graphics - Multiple Turtles
So far, the program has used one sole turtle to carry out all of the commands. However, it is also possible to create more than one turtle, and each turtle can do different things! We can create a new turtle, and have it draw a **triangle**!

### Creating the turtle
Creating the _new_ turtle will be very similar to creating the original turtle. The only difference will be the name of the turtle (turtles are not allowed to have the same name in Python). Copy the commands used to create the `koopa` turtle, and update them to create a turtle named `shelly`. Add the following commands at the bottom of the `main.py` file:
```python
shelly = Turtle()
shelly.shape("turtle")
shelly.color("white")
```

Run the program to see the new white turtle appear at the end!

### Drawing the triangle
Shelly should draw three lines of equal length `100`, turning `120` degrees between each line. Add the following commands at the bottom of the `main.py` file:
```python
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
```

Run the program to see Shelly draw the triangle!

#### Challenge: Tilted triangle
Currently, the triangle is tilted so that instead of being flat on the bottom, it is flat on the top. Add an additional command _before_ Shelly starts drawing so that the triangle is rotated and becomes flat on the bottom.

>HINT: Use `shelly.right` and an appropriate number for the angle!

### Changing the starting point
In the current program, Shelly draws all over the existing shape. Instead, the program should move Shelly to another position _before_ drawing anything.

_Before_ the commands that make Shelly draw, add the following command:
```python
shelly.setpos(-100, 100)
```

Run the program to see what happens. Shelly moves, but there is another issue now!

### Removing the extra pen marks
When shelly moves to the starting point, the pen draws an extra line! Instead of doing this, the program should lift up the pen before this movement.

When working with turtles, it is possible to control whether the pen is "up" or "down" (like real life drawing). _Before_ the `shelly.setpos` command, add the following command:
```python
shelly.penup()
```

This will allow Shelly to move without drawing anything! Run the program to see what happens.

### Putting the pen back down
Oh no! After lifting up the pen, Shelly no longer draws the triangle! Fix this by adding the following command _after_ the `shelly.setpos` command:
```python
shelly.pendown()
```

This way, Shelly will pick up the pen when moving to the starting point, and then put it back down before moving in the triangular fashion. Run the program again to see it work properly!

#### Challenge: New starting point
Instead of starting Shelly at a position of `(-100, 100)`, move the starting point to be right above the square!

## Loops
Loops are a very powerful programming tool. They allow developers to repeat blocks of code automatically, without having to write the commands over and over again. One of the major benefits is that if the developer needs to change something, they only have to change it in one place!

In the turtle code, there are a couple of blocks of code that could be improved with loops. Where do those repetitive commands occur?

### Drawing the square
```python
koopa.forward(100)
koopa.right(90)
koopa.forward(100)
koopa.right(90)
koopa.forward(100)
koopa.right(90)
koopa.forward(100)
koopa.right(90)
```

The two lines, `koopa.forward` and `koopa.right`, are repeated four times here. It takes up extra space in the file, and in order to update the program, each individual line would require update. For example, to make the square bigger, each `100` would have to change. Imagine if, instead of four times, the developer had to change four _hundred_ lines! Or, if the program needed to dynamically update the number of times to repeat the code, that would be impossible without loops.

### Looping the square
Use a `for` loop to automatically repeat the `forward` and `right` lines. Replace the square-drawing code with the following set of commands:
```python
for x in range(4):
    koopa.forward(100)
    koopa.right(90)
```

This will make the two lines repeat `4` times!

Note that the two lines are _indented_; this is how the loop knows which commands should repeat. The `for x in range()` part is the same for any number of repetitions; the `4` specifies that the loop should repeat four times.

### Looping the triangle
Apply the same looping technique for Shelly and the triangle. Replace the repeated lines of code with a new loop:
```python
for x in range(3):
    shelly.forward(100)
    shelly.right(120)
```

With the use of loops, the file is much shorter, and easier to maintain. Loops are one of the most important parts of programming!

## Additional Challenges
Play around with the turtles to create something cool! Feel free to start from the challenges below, or do something completely different. Also, check out the other turtle abilities!

### Diamond
At the bottom of the `main.py` file, write commands to complete the steps below:

1. Create a new turtle
1. Move them to a good starting point on the screen
    - Remember to make them pick up the pen first!
1. Make them draw a diamond
    - Note: A diamond is simply a tilted square!

### Many-pointed star
At the bottom of the `main.py` file, write commands for a new turtle to draw a star with many points! It should look something like this:

![many-pointed star](https://i.imgur.com/uJR2FZO.png)

#### Help
Use the square as a template:
```python
for x in range(4)
    koopa.forward(100)
    koopa.right(90)
```

Change the `4`, `100`, and `90` values so that the turtle moves in the correct way. Try out different numbers until it looks right!

### Other Shapes
Create new turtles that draw each of the following shapes:
- Pentagon
- Hexagon
- Septagon
- Parallelogram
- Trapezoid

### Complete drawing
Use a turtle to draw a whole picture, like a house or a flower or anything else that comes to mind!

## Other turtle abilities
Turtles have many additional abilities! Try to incorporate some of these new commands into the existing turtle code.

### Turtle talk
Turtles have the ability to display messages on the screen. Add the following command in the `main.py` file:
```python
koopa.write("I am a turtle")
```

Run the program to see the message appear next to the turtle! 

### Turtle pen size
Turtles can change the size of the lines they draw. In the `main.py` file, _above_ the commands that make the turtle draw, add the following command:
```python
koopa.pensize(4)
```

Run the program to see the line thickness change! Try out some other values to see how they look.

### Turtle speed
There is a command that will change the speed of a turtle. In the `main.py` file, _above_ the commands that make the turtle move, add the following command:
```python
koopa.speed(8)
```

Run the program to see the speed change! Try out some other values to see how they look.

### Hiding the turtle
There is a command that will make the turtle invisible. This can be very useful when drawing. In the `main.py` file, add the following command:
```python
koopa.hideturtle()
```

Run the program to see the turtle disappear!

It is also possible to **show** the turtle after it has hidden, using the following command:
```python
koopa.showturtle()
```

### Turtle circles
There is a command that will make the turtle draw a circle. In the `main.py` file, add the following command:
```python
koopa.circle(50)
```

Run the program to see the circle! It is also possible to change the size of the circle by using numbers other than `50`.

### Pen fills
There is a command that will make the pen drawing fill with the color of the turtle (like a paint bucket tool). In the `main.py` file, add the following commands:
```python
koopa.begin_fill()
koopa.circle(80)
koopa.end_fill()
```

This will fill in the circle the turtle draws! It can be used with any shape by running the `begin_fill` command before drawing and the `end_fill` command after.
