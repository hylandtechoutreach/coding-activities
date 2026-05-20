# Code-Along: 2D Scene in Processing
Follow these steps to build a simple two-dimensional scene in **p5.js**.

[**Click here to open the empty starter project.**](https://hytop.onrender.com/e/p5-start-scene) Make sure to click the **Fork** button to make your own copy.

## Getting Started
Since the **script.js** file is pretty empty, there are a few things to add before it's possible to create anything interesting.

### The `setup` Function
First, add some code to the `setup` function. This code will run once, when the program first loads. This is where we can set the size of our scene!

```js
function setup() {
  createCanvas(300, 200);
}
```

Make sure that the new line is inside the `{` and `}` so it's in the _body_ of the function.

With the `setup` function defined, try running the program. It's still empty, but the canvas is the right size!

### The `draw` Function
Next, we need to define the `draw` function. This code will run every frame - in our case, that doesn't really matter, but it is good to know. This is where we can start drawing! First, let's set the background color of our scene.

```js
function draw() {
    background("cyan");
}
```

Make sure that the new line is inside the `{` and `}` so it's in the _body_ of the function.

Save the file to see the sky!

## Sun, and Ground
Next, start to create a world within this canvas. We'll create a circle (an `ellipse`) that represents a celestial body, and a rectangle (a `rect`) that represents the ground.

### Sun
In the `draw` function, under `background` (but still above `}`), add some new code:

```js
stroke("black");
fill("yellow");
ellipse(300, 0, 50, 50);
```

1. Use `stroke` to give the drawing an outline color
1. Use `fill` to give the drawing a fill color
1. Use `ellipse` to draw the circle!

With this code, the circle should appear in the upper right! To move it, we can change the numbers:

1. `x` (currently `150`) - horizontal location
2. `y` (currently `100`) - vertical location
3. `width` (currently `10`) - horizontal size
4. `height` (currently `10`) - vertical size

Save the file, and it should look like there's a sun!

### Ground
Now it's time to add some ground. In the `draw` function, under `ellipse` (but still above `}`), add some new code:

```js
fill("lime");
rect(-1, 175, 301, 25);
```

With this code, the green ground should appear at the bottom! To change it:

1. `x` (currently `-1`) - upper left corner horizontal position
2. `y` (currently `175`) - upper left corner vertical position
3. `width` (currently `301`) - horizontal size
4. `height` (currently `25`) - vertical size


#### Aside: Processing Canvas
[Click here to read more](https://processing.org/tutorials/coordinatesystemandshapes)

### Basic Scene Code
At this point, there should be a nice basic scene. The code should look something like this:

```js
function setup() {
    createCanvas(300, 200);
}

function draw() {
    background("cyan");
    stroke("black");
    fill("yellow");
    ellipse(300, 0, 50, 50);
    fill("lime");
    rect(-1, 175, 301, 25);
}
```

## Drawing Trees
The scene has a nice background, but there's not much there. Luckily, there is a separate function to draw trees.

### Placing the Tree
Trees can be drawn using the `drawTree` function (defined in the **drawLib.js** file). Add a line to the bottom of the `draw` function (above `}`):

```js
drawTree(20, 170, 80);
```

Save the file, and see a tree appear!

### Adding More Trees
Next, add some more trees to the scene. Each tree is added with the `drawTree` function, just like this:

```js
drawTree(20, 170, 80);
```

Copy and paste that line within the body of the `draw` function definition, and change the numbers:

1. Horizontal position (e.g., `20`)
1. Vertical position (e.g., `170`)
1. Height (e.g., `80`)

Do that a few times, then run the program to see a whole forest begin to appear!

## _BONUS: Clouds_
On your own, see if you can figure out how to draw clouds in the scene!

## Conclusion
By the end of this activity, the added code in the **script.js** file should look something like this:

```js
function setup() {
  createCanvas(300, 200);
}

function draw() {
  background("cyan");
  stroke("black");
  fill("yellow");
  ellipse(300, 0, 50, 50);
  
  fill("lime");
  rect(-1, 175, 301, 25);

  drawTree(20, 170, 80);
  drawTree(90, 177, 70);
  drawTree(120, 177, 70);
  drawTree(250, 163, 59);
  drawTree(194, 172, 90);
}
```
