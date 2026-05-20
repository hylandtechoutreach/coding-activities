# Mood Swings
[Click here for the starter code.](https://hytop.onrender.com/e/p5-mood-swings) Make sure to **fork** the project to create your own version!

>_Credit: [Happy Coding](https://happycoding.io/tutorials/p5js/input/grouchy-face)_

## Mad Boolean
Currently, the program displays a simple smiley face. Our first step is to anger this face!

At the very top of the **script.js** file, change the code so that the smiley is mad! This is possible with the [**boolean** data type](https://www.w3schools.com/Js/js_booleans.asp).

```js
let isMad = true;
```

## Handling Click
Rather than being a static value, we want to change the `isMad` variable when the user clicks the screen! We can define the `mousePressed` function to accomplish this.

1. At the very bottom of the **script.js** file, make a new line
1. There, define a new function with the word `function`
1. Next, add a space, and the function name: `mousePressed`
1. After that, add the open/close parentheses: `()`
1. After that, add the open/close brackets: `{` and `}`
1. Press `Enter` in between to make a new line
1. There, add an `alert` statement just to make sure it's hooked up!

Save the project, and click the screen - it should pop up with a message!

The added code should look like this:

```js
function mousePressed() {
  alert("TEST");
}
```

## Changing `isMad` On Click
Now, we have to make the `mousePressed` function actually do what we want!

1. Remove the `alert` statement from the `mousePressed` function
1. In its place, set the `isMad` variable to be `false`

Save the project, click the screen, and make sure it changes!

The code should now look like this:

```js
function mousePressed() {
  isMad = false; // or true if it was originally false
}
```

## Toggling `isMad`
Currently, the program will successfully change the mood once and only once - it always sets the `isMad` variable to the same static value! Instead, it should change the `isMad` variable based on its current value.

If the face is currently mad, it should change `isMad` to `false`. If the face is currently happy, it should change `isMad` to `true`. Here is some code to do that:

```js
if (isMad === true) {
  isMad = false;
} else {
  isMad = true;
}
```

However, there is a simpler way! We can use `!` to reverse the value of a boolean. So we just have to set `isMad` to the opposite of what `isMad` currently is! The code looks like this:

```js
isMad = !isMad;
```

Update the code in the `mousePressed` function, save the project, and click the screen repeatedly to see it happen!

## Final Code
At the end of the activity, the code in the **script.js** file should look something like this:

```js
let isMad = false;

function setup() {
  createCanvas(300, 300);
  textAlign(CENTER, CENTER);
  textSize(144);
}

function draw() {
  if (isMad) {
    background(random(64, 255), 0, 0);
    text("😠", width / 2 + random(-10, 10), height / 2 + random(-10, 10));
  } else {
    background(64);
    text("🙂", width / 2, height / 2);
  }
}

function mousePressed() {
  isMad = !isMad;
}
```
