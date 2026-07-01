# 3D Worlds Code-Along
In this activity, use the [aframe-envrionment-component](https://github.com/supermedium/aframe-environment-component) with A-Frame to create a 3D World!

## Getting Started
[Click here to open the starter project.](https://hytop.onrender.com/e/aframe-steam)

Click the "Fork" button in the upper left to create your own copy of the project. From there, you're ready to start editing!

## Magic HTML
A-Frame makes it possible to create three-dimensional structures using [HTML](https://en.wikipedia.org/wiki/HTML) code! HTML is the language of the web, and consists of elements that create everything you see on a website. Elements generally looks like this:

`<element-name>CONTENT</element-name>`

Breaking down that example, the _opening tag_ is this part: `<element-name>`. It starts with `<`, then has the name of the element, then `>`. The _content_ is immediately after the opening tag. The _closing tag_ looks like the opening tag, but with a slash before the element name: `</element-name>`

First, create a basic, _normal_ HTML element. Then, create a couple of A-Frame elements!

### First HTML Element: A Header
Follow these steps to add an HTML element to the page:

1. On the left, open the **index.html** file for editing
1. On a line at the bottom, start typing the _opening tag_ of the `h1` element: `<h1>`
1. Next, add a message: type whatever you'd like!
1. After that, add the _closing tag_ for the `h1` element: `</h1>`
1. Save your project (button in upper left, or `Ctrl`+`s`)

Now, the message should appear on your page! It should look something like this:


```html
<h1>MY WORLD</h1>
```

### First A-Frame Element: A Scene
The next thing to do is add an A-Frame scene. This will look very similar to the `h1` element, with a couple key differences:

- The name of the element is `a-scene` instead of `h1`
- There is no content for the element (yet!)
- Within the opening tag, after the element name, there is an ` environment` attribute

Follow these instructions:

1. Make a new line in the **index.html** file
1. Add the _opening tag_ for the `a-scene` element: `<a-scene>`
1. After the final `e` in `a-scene`, but BEFORE the `>`, make a space
1. There, add the word `environment`
1. Add the _closing tag_ for the `a-scene` element: `</a-scene>`
1. Save the project

Now, you should see a world! it should look pretty empty to start, but it's something! The added code should look something like this:

```html
<a-scene environment></a-scene>
```

### First A-Frame Object: A Sphere
Next, it's time to add an object to the scene: a basic sphere. The `a-sphere` element will be nested INSIDE of the `a-scene` element as its child. It has to be declared BETWEEN the opening `a-scene` tag and the closing `a-scene` tag. We want the sphere to appear in the world, so it has to go inside the scene!

1. Click right between the `<a-sphere>` opening tag and the `</a-sphere>` closing tag
1. Press enter to make a new line
1. There, add the _opening tag_ for the `a-sphere` element: `<a-sphere>`
1. Next, add the _closing tag_ for the `a-sphere` element: `</a-sphere>`
1. Save the project

Now, you should see a sphere appear! The code should look something like this:

```html
<a-scene environment>
  <a-sphere></a-sphere>
</a-scene>
```

That's all for the HTML. Next up, we can start customizing features of the environment using JavaScript!

## JavaScript Variables: Existing
In computer science, variables are containers for data. Variables can hold numbers, text, or true/false values called booleans. Variable names are used in other parts of the code to change how things run dynamically.

Open the **variables.js** file to take a look at some of the existing variables:

```js
let cameraAcceleration = 10;
let cameraLookControls = false;
let cameraFly = false;
let skyType = "color";
```

All of these control how the A-Frame world works. Try changing them around to see what happens! Each value will update some part of the world. Don't worry about the `skyType` variable for now, just keep it as `"color"`. Try setting everything like so:

```js
let cameraAcceleration = 100;
let cameraLookControls = true;
let cameraFly = true;
let skyType = "color";
```

Now, it should be possible to zoom around the world in any direction!

## JavaScript Variables: New
With some of the basic variables set, it is time to start adding some new variables. Declaring a variable in JavaScript looks like this:

```js
let variableName = "variable value";
```

`variableName` is the name of the variable (which must be exactly right, including capitalization). `"variable value"` is the _value_ of the variable (note the `"` and `"` quotation marks - these are important for text values). The `let`, `=`, and `;` are the same for declaring all variables, but the `variableName` and `"variable value"` can change.

For the remainder of this activity, there are a several variables to cover - they all have specific names, and specific possibilities for their values. For each one:

1. Make a new line in the **variables.js** file
1. Start declaring a variable with `let `
1. After a space, add the variable name (e.g., `skyColor`)
1. Next, add an equals sign `=`
1. Then, add the variable value (e.g., `"cyan"` or `.7`)
1. Finally, add a semi-colon `;`

Adding these variable declarations can make your world totally unique!

### Sky Color: `skyColor`
This variable sets the color of the sky.

- Type: text string (needs `"` and `"`)
- Values: colors (named or [hex codes](https://www.google.com/search?q=color+picker))

### Ground Shape: `ground`
This variable sets the shape of the ground.

- Type: text string (needs `"` and `"`)
- Values:
  - `"none"`
  - `"flat"`
  - `"hills"`
  - `"canyon"`
  - `"spikes"`
  - `"noise"`

### Ground Colors: `groundColor` and `groundColor2`
These two variables `groundColor` and `groundColor2` set the colors used for the ground pattern.

- Type: text string (needs `"` and `"`)
- Values: colors (named or [hex codes](https://www.google.com/search?q=color+picker))

### Ground Pattern: `groundTexture`
This variable sets the appearance of the ground, using `groundColor` and `groundColor2`.

- Type: text string (needs `"` and `"`)
- Values:
  - `"none"`
  - `"checkerboard"`
  - `"squares"`
  - `"walkernoise"`

### Fog: `fog`
This variable controls the amount of fog in the world.

- Type: decimal number
- Values: between `0` (no fog) and `1` (full fog) 

### Flat Plane Area: `playArea`
This variable controls the radius of the area where the ground is flat and there are no objects (regardless of `ground` and `dressing` variables).

- Type: decimal number
- Values: between `0` (no area flat) and `2` (all area flat)

### Ground Shape Height: `groundYScale`
This variable controls the maximum height of the ground.

- Type: number
- Values: `0` is flat, `5` is approximately the height of the sphere, higher values are possible

### Scene Decoration Objects: `dressing`
This variable controls the type of objects that are added to the scene.

- Type: text string (needs `"` and `"`)
- Values:
  - `"none"`
  - `"cubes"`
  - `"pyramids"`
  - `"cylinders"`
  - `"towers"`
  - `"mushrooms"`
  - `"trees"`
  - `"apparatus"`
  - `"torii"`

### Scene Decoration Object Size: `dressingScale`
This variable controls the **size** of the objects added with the `dressing` variable.

- Type: number
- Values: `0` is nothing, `5` is approximately the height of the sphere, higher values are possible

### Scene Decoration Object Number: `dressingAmount`
This variable controls the **number** of objects added with the `dressing` variable.

- Type: number
- Values: `0` is none, keep it below `1000` to avoid performance issues

### Scene Decoration Object Color: `dressingColor`
This variable controls the **color** of the objects added with the `dressing` variable.

- Type: text string (needs `"` and `"`)
- Values: colors (named or [hex codes](https://www.google.com/search?q=color+picker))

### Randomness Seed: `seed`
This variable controls the randomness (hills, dressing placement, etc). Try different numbers to see different random worlds.

- Type: number
- Values: anything

### Example Code
Here is one example of a world created by declaring all of these variables!

```js
let skyColor = "cyan";
let ground = "canyon";
let groundColor = "green";
let groundColor2 = "darkgreen";
let groundTexture = "walkernoise";
let fog = .7;
let playArea = .1;
let groundYScale = 2;
let dressing = "trees";
let dressingScale = 10;
let dressingAmount = 100;
let dressingColor = "orange";
let seed = 2;
```

All of the values can change to create different things. 

## Final Code
By the end of the activity, the code should look something like [this](https://hytop.onrender.com/e/aframe-steam0/):

**index.html**

```html
<script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
<script src="https://unpkg.com/aframe-environment-component@1.5.x/dist/aframe-environment-component.min.js"></script>
<script src="variables.js"></script>
<script src="script.js"></script>

<h1>MY WORLD</h1>

<a-scene environment>
  <a-sphere></a-sphere>
</a-scene>
```

**variables.js**

```js
let cameraAcceleration = 100;
let cameraLookControls = true;
let cameraFly = true;
let skyType = "color";

let skyColor = "cyan";
let ground = "canyon";
let groundColor = "green";
let groundColor2 = "darkgreen";
let groundTexture = "walkernoise";
let fog = .7;
let playArea = .1;
let groundYScale = 2;
let dressing = "trees";
let dressingScale = 10;
let dressingAmount = 100;
let dressingColor = "orange";
let seed = 2;
```
