# Add POWER-UP Code-Along
Once you have [customized the game](FillInTheVariablesCodeAlong.md), it's time to add a new feature: a **POWER-UP**. For this example, we will make the player run faster when they eat the POWER-UP.

## Adding a "Consumable"
The game is pre-built to allow for "Consumables" to be added to the map. "Consumables" (as defined in the **zobject.consumable.js** file) are designed to disappear and cause some effect when the player touches them.

1. Open the **script.js** file
1. Put your cursor on line `8` (way down at the bottom)  
  - _We will be adding more lines of code above this line_
2. Add this line of code to create a new `Consumable` object:  
  ```js
  game.addConsumable();
  ```
1. Save the project
1. Look at the game preview
1. You should notice a small white ball!
1. Eat the ball
1. You should notice the ball disappears!

So we have a consumable! But we can change quite a few things to make sure it makes sense in the game.

## Changing the North Position
We can set the `north` position of our new consumable. We will do this using _variables_ that are passed into `addConsumable`!

First, make the new variable `north`:

1. Put your cursor at the top of the **script.js** file (above the `game.addConsumable()` line)
1. Start a new variable definition by typing `let`
1. Then, type a variable name: `north`
1. After that, add an equals sign `=`
1. Next, add a number for the `north` position: `2`
1. At the end of the line, add a semi-colon `;`

Next, pass the variable to `addConsumable`:

1. Find the `game.addConsumable` line
1. Put your cursor right between the parentheses (`(` and `)`)
1. Type the variable name, `north`
1. Save the project
1. Look at the preview
1. Notice the little ball should have moved!

The code in the **script.js** file should look something like this:

```js
let north = 2;

game.addConsumable(north);
```

## Changing the East and Vertical Position
To change the `east` and `vertical` positions of the POWER-UP, follow very similar steps:

1. Create the new variables (`east` and `vertical`)
1. Set their values to things that make sense (like `10` and `4`)
1. In the `game.addConsumable` line, add `east` and `vertical`, all separated by commas
1. Save the project
1. Look at the preview
1. Notice the little ball should have moved!

At this point, the code in the **script.js** file should look something like this:

```js
let north = 2;
let east = 10;
let vertical = 4;

game.addConsumable(north, east, vertical);
```

## Making the POWER-UP Actually Power Up
Now for the fun and difficult part - making the POWER-UP actually functional! To do this, we will actually be defining a **function** in JavaScript. A **function** is a piece of code that does something on command. Just like with the previous variables, we will be making a new variable to store this command, and then we will pass it to the `game.addConsumable` line.

### VARIABLE SETUP
First, get the variable setup:

1. Make a new line in the **script.js** file, still above the `game.addConsumable` line
1. Create a new variable named `eatPowerUp`  
  1. `let` keyword
  1. Variable name (`eatPowerUp`)
  1. Equals sign (`=`)
  1. Value (?????????)

```js
let eatPowerUp = 
```

### FUNCTION SKELETON
Now, it's time to define the function skeleton:

1. After the equals sign, instead of a number, type the word `function`
1. After the word `function`, add left and right parentheses: `()`
1. In between the parentheses, add left and right curly brackets: `{}`
1. Put your cursor between the curly brackets and press **Enter** to make a new line

```js
let eatPowerUp = function() {

}
```

Whatever code is between those curly brackets will run whenever the player consumes the POWER-UP!

### FUNCTION FUNCTIONALITY
We can **set** one of our variables in there to change the gameplay. Setting a variable is a lot like defining one, but we don't need the `let` keyword.

Let's set our `PLAYER_SPEED` to `20`:

```js
let eatPowerUp = function() {
  PLAYER_SPEED = 20;
}
```

### FUNCTION PASSING
Finally, we need to pass the new `eatPowerUp` function to our `game.addConsumable`.

1. Find the `game.addConsumable` line
1. Put your cursor in between the parentheses, right at the end (after `vertical`, before `)`)
1. Add a comma `,` and the function name `eatPowerUp`

```js
game.addConsumable(north, east, vertical, eatPowerUp);
```

Save the project, eat the POWER-UP, and see what happens!

### CODE NOW
The code in the **script.js** file should now look something like this:

```js
let north = 2;
let east = 10;
let vertical = 4;

let eatPowerUp = function() {
    PLAYER_SPEED = 20;
}

game.addConsumable(north, east, vertical, eatPowerUp);
```

## Changing Size, Color, and Shape
The last thing to do is customize our POWER-UP with its own size, color, and shape. Setting these POWER-UP properties will be very similar to setting `north`, `east`, and `vertical`. It is very important that they are added in the proper order, AND have the proper formatting (watch commas `,` and quotation marks `""`).

1. Above the `game.addConsumable` line, define the `size` variable, and set it to `10`
1. Under that, define the `color` variable and set it to `"cyan"`  
  - Note the `""` quotation marks!
1. Under that, define the `shape` variable and set it to `"box"`  
  - The only options now are `"sphere"`, `"box"`, and `"torus"`
1. Add `size`, `color`, and `shape` between the parentheses on the `game.addConsumable` line
1. Save the project
1. Look at the preview
1. See the new size, shape, and color!

## Conclusion
At the end of this code-along, the code in the **script.js** file should look something like this:

```js
let north = 2;
let east = 10;
let vertical = 4;

let eatPowerUp = function() {
    PLAYER_SPEED = 20;
}

let size = 10;
let color = "cyan";
let shape = "box";

game.addConsumable(north, east, vertical, eatPowerUp, size, color, shape);
```

## Next Steps
There are so many additional things you can try to make your game even better!

1. Add a new power-up, or change the current one to do something interesting
1. Add more platforms, coins, or enemies
1. Continue changing the variables

The possibilities are endless!
