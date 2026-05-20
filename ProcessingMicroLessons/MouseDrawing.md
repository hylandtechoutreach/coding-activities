# Mouse Drawing
[Click here for the starter code.](https://hytop.onrender.com/e/p5-mouse-draw) Make sure to **fork** the project to create your own version!

This example lets you click and drag to draw on a canvas using an image!

## Part One: Swapping Things
The first step is to make this project your own by changing some key aspects of the code in the **script.js** file:

- Canvas Size (on line `4`)
- Background Color (on line `7`)
- Drawing Image (on line `8`)

Update these things to be whatever you want!

## Part Two: Right Click to Erase
It can be fun to draw, but it's easy for the space to get too busy. Let's add the ability to erase!

1. Make a new line under the `}` of the `if` in the `draw` function (under line `15`)  
  ```js
  function draw() {
    if (mouseButton.left) {
      image(img, mouseX, mouseY, 100, 100);
    }

    // RIGHT HERE
  }
  ```
1. There, add another `if` statement, this time, checking for `mouseButton.right`  
  ```js
  if (mouseButton.right) {

  }
  ```
1. Within the `{` and `}` for that statement, set the `fill` to be the same as the background  
  ```js
  fill(255, 255, 0);
  ```
1. Under that, make sure there is no outline with `noStroke()`  
  ```js
  noStroke();
  ```
1. Finally, under that, make an empty circle at the current mouse position!  
  ```js
  ellipse(mouseX, mouseY, 100, 100);
  ```

Save the project, and it should be possible to erase! The code should look something like this:

```js
let img;

async function setup() {
  let canvas = createCanvas(500, 500);
  canvas.elt.addEventListener("contextmenu", (e) => e.preventDefault());

  background(255, 255, 0);
  img = await loadImage("https://cdn.creazilla.com/cliparts/19265/cartoon-brown-mouse-clipart-xl.png");
  imageMode(CENTER);
}

function draw() {
  if (mouseButton.left) {
    image(img, mouseX, mouseY, 100, 100);
  }

  if (mouseButton.right) {
    fill(255, 255, 0);
    noStroke();
    ellipse(mouseX, mouseY, 100, 100);
  }
}
```
