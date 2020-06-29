# JavaScript Alerts Lesson
Use this activity to introduce students to the basics of JavaScript by hooking up HTML buttons to functions that use `alert` commands.

## Starter CodePen
Students should navigate to [bit.ly/alertstarter](https://codepen.io/jmaxwell/pen/JjGJeVy?editors=1010) to get the starter code. Display the link in very large font so they can see it, and make sure they type it in exactly like that (it is case-sensitive).

So far, the page does not contain too much; just a header and an image. The goal of the activity is to add some buttons on the page that will show quotes from Spongebob when clicked!

## Adding a Button in HTML
The first step is to update the HTML so that a button appears on the page.

1. Expand the HTML section in the CodePen
1. At the bottom of the code so far, add a `button` element
    - Opening tag and closing tag: `<button></button>`
1. Make sure an empty button appears on the webpage
    - The button needs some text!
1. Within the opening and closing `button` tags, add text for the button: "Mayo"
1. Verify that the button appears with the text!

```html
<button>Mayo</button>
```

## Defining a Function in JS
Now, define a set of instructions for the button to follow when clicked; this is a **function** in JavaScript.

1. Expand the JS section in the CodePen
1. Here, define a _function_ in JavaScript, starting with the word `function`
1. After `function`, make a space
1. Ask the students what this function should be named
    - A good name for the function would be `sayMayo`, because it will say the "mayo" quote
    - Note that function names can only have letters and numbers, and no spaces!
1. Type in `sayMayo` followed by open and close parentheses and curly brackets
    - `function sayMayo() {}`
1. In between the curly brackets, press enter to make some space
    - This is a lot like in CSS!
    - Inside the brackets part is the _body_ of the function, where the actual commands go
1. In the body, type in the word `alert`, followed by parentheses, and quotes within the parentheses
    - The `alert` will show a message
1. Inside of the quotes, type in the quote from Spongebob: "Is mayonnaise an instrument?"
1. Add a semi-colon at the end of the line
1. Make sure everything is exactly right, otherwise it will not work!

```js
function sayMayo() {
  alert("Is mayonnaise an instrument?");
}
```

## Hooking Up the Button
Now, the HTML button is ready, and the JS function is ready. All that's left is connecting them! Hook up the HTML button to the JS function using the `onclick` attribute.

1. Expand the HTML section in the CodePen
1. Find the `button` element, and click into the opening tag (after `button`, before `>`)
1. Make a space, and type in `onclick`, an equals sign, and quotes
1. Ask the students where they have seen something like this before
    - It is an HTML attribute, just like `src` for images, `href` for links, or `class` for CSS styling
1. Ask students for the name of the function: `sayMayo`
1. Within the quotes, _call_ the `sayMayo` function by typing `sayMayo()`
1. Verify that clicking the button will make the message from the `sayMayo` function pop up!

```html
<button onclick="sayMayo()">Mayo</button>
```

## Creating Another Button
Creating additional buttons will be a lot like adding the first button! Add the `button` element in the HTML, define the function in JS, and finally, hook it up.

1. In the HTML section, make a new line under the existing button
1. Ask the students how to create a new button
1. At the bottom of the code, add another `button` element with the text "Life"
1. Expand the JS section, and make a new line under the closing curly bracket for the function above
1. Ask the students what is needed to make a new function
1. Add the word `function`
    - This is always the first thing needed to define a function
1. Add the name of the function, followed by parentheses (the name of the function in this case is `sayLife`)
1. Add curly brackets after the parentheses, click between them, and press enter
1. Ask the students how to show a message
1. Add the `alert` statement, with parentheses and quotes
1. Add the message within the quotes: "Can I be excused for the rest of my life?"
1. Add a semi-colon at the end of the line
1. Back in the HTML, ask the students how to hook up the `button` element to the function
1. Add the `onclick=""` in the opening tag for the "Life" button
1. Ask the students what to put within the quotes
1. Add in code between the quotes to _call_ the `sayLife` function: `sayLife()`
1. Verify that the new button will show the new quote when clicked!

### HTML
```html
<button onclick="sayLife()">Life</button>
```

### JS
```js
function sayLife() {
    alert("Can I be excused for the rest of my life?");
}
```

## Creating Yet Another Button
For the next button, allow the students to lead the way. The button should say `Ravioli`, and the quote should be `Ravioli, Ravioli, give me the formuoli`.

>Note: If there is not enough time, skip the third button and let the students work individually instead

1. Ask the students how to make a button in HTML that says "Ravioli"
    - In the HTML section after everything else
    - Opening tag
    - Button text
    - Closing tag
    - `<button>Ravioli</button>`
1. Ask the students how to define a function in JavaScript named `sayRavioli`
    - In the JS section after everything else
    - `function`
    - Function name
    - Parentheses
    - Curly brackets
    - `function sayRavioli() {}`
1. Ask the students how to make the function say the quote
    - In the body of the function
    - `alert`
    - Parentheses
    - Quotes within the parentheses
    - Message within the quotes
    - Semi-colon at the end of the line
    - `alert("Ravioli, Ravioli, give me the formuoli");`
1. Ask the students how to hook the function up to the button in the HTML
    - In the opening tag of the button
    - `onclick`
    - Equals sign
    - Quotes
    - Function name within the quotes
    - Parentheses within the quotes
    - `onclick="sayRavioli()"`
1. Verify that the button works!

## Final Code
At the [end of the activity](https://codepen.io/jmaxwell/pen/xxZrJOV), the code should look like this:

### HTML
```html
<h1>Spongebob Quotes</h1>
<p><img src="https://i.imgur.com/J7gL944.png"></p>

<button onclick="sayMayo()">Mayo</button>
<button onclick="sayLife()">Life</button>
<button onclick="sayRavioli()">Ravioli</button>
```

### JS
```js
function mayo() {
  alert("Is mayonnaise an instrument?");
}

function life() {
  alert("Can I be excused for the rest of my life?");
}

function ravioli() {
  alert("Ravioli, ravioli, give me the formuoli");
}
```

## Individual Work
With remaining time after the activity, give the students some time to work individually. Here are some ideas for challenges:

- Add more Spongebob images to the HTML
- Update the page styles in CSS
- Add more buttons to the page with more quotes
- Change Spongebob to another character, and add images and quote buttons from that character instead!

As the students work individually, be available to answer any questions they may have.