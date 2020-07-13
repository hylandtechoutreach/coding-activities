# Web Development: Additional Topics Challenges
With any remaining time, make updates to the webpage by following these instructions!

## HTML Challenge: Embed a YouTube video
1. Open a new tab and go to [YouTube](https://youtube.com)
1. Search for an appropriate video (e.g., [color red](https://www.youtube.com/watch?v=8YWl7tDGUPA))
1. Under the video, click the "SHARE" button  
    ![](https://i.imgur.com/6rOqJb3.png) 
1. Click "Embed"  
    ![](https://i.imgur.com/OPzkSc2.png)  
1. Click "COPY"  
    ![](https://i.imgur.com/barvOys.png)
1. In the CodePen, paste the code at the bottom of the HTML section
    - Use `Ctrl`+`v` or right-click and select "Paste"
1. Watch the video on your website!

The code should look something like this:

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/7zkX6kfnWbk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## CSS Challenge: Header Text Shadow
1. In the CSS section, under the `}` from the "body" ruleset, make some new lines
1. Create a new ruleset for "h1" by adding `h1` and `{` and `}`
    - This will mean that all styles apply to each `h1` HTML element
    - Note that when adding the opening bracket (`{`), CodePen adds the closing bracket (`}`) automatically
    - With the cursor between the two brackets, press the "Enter" key to properly format the ruleset
1. Within the brackets, add a new declaration: `text-shadow: red -1px 1px`
1. Update the numbers and the color to see how it changes the effect!
1. For more information, check out this article: [https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow)

The code should look something like this:

```css
h1 {
    text-shadow: red -1px 1px;
}
```

## CSS Challenge: Create a Gradient Background or a Background Image
1. In the CSS section, within the `body` ruleset, remove the `background` value
1. Replace the value with a `linear-gradient` containing two colors (see code below)
1. Change the values to see how it changes the gradient!

```css
body {
    /* ... */
    background: linear-gradient(#9198e5, #e66465);
    /* ... */
}
```

>Note: Go [cssgradient.io](https://cssgradient.io/) to customize the gradient!

It is also possible to give the page a background image:

1. Find an image online
1. Copy the image address
1. Update the `background` declaration in the CSS with a `url` containing the image address in quotes

```css
body {
    /* ... */
    background: url("https://cdn141.picsart.com/301292961077211.png?r1024x1024");
    /* ... */
}
```

## CSS Challenge: Change Text Color on Hover
1. In the CSS section, create a new ruleset for `li`
    - The styles in this ruleset will only affect `li` elements
1. Add the `color` property with a value of `orange`
    - Notice that the text color changed
1. Update the selector so that instead of `li`, it is `li:hover`
    - This means the styles will only apply when the user hovers over the `li` elements
1. Update the values to change the effect! 

```css
li:hover {
  color: orange;
}
```

## JavaScript Challenge: Add an Alert Button
Add a button to the webpage that will display a message when someone clicks it.

### HTML
1. In the HTML section, add a new element: `button`
    - Add the opening tag: `<button>`
    - Add some text for the button
    - Add the closing tag: `</button>`
1. Make sure the button appears on the page with the proper text
1. Inside the opening tag for the button, after the word `button` before the `>`, add a space
1. After the space, add an `onclick` attribute set equal to `run()`
    - Add `onclick`
    - Add an equals sign
    - Add quotation marks
    - Between the quotation marks, add `run()`
    - This `onclick` will trigger JavaScript code to run when the button is clicked!

```html
<button onclick="run()">Click Me!</button>
```

### JavaScript
The button needs a _function_ to call, which will contain some code commands. Basically, defining a function will tell the button what to do when it is clicked.

1. Expand the JS section
1. Type the word `function`
1. Make a space, and type in `run()`
    - This **must** match the value inside of the `onclick` in the HTML
1. Type in a left curly bracket
    - The right curly bracket should be added automatically, like in CSS
1. Press enter to go between the curly brackets on a new line
1. Type in `alert`
    - This command will display a message
1. After `alert`, type in a left parenthesis: `(`
    - This should automatically add a right parenthesis, and the cursor should be in between the two parentheses
1. Between the parentheses, type in a double quote: `"`
    - Another double quote should be added automatically
1. Between the quotes, type in a message to show
1. Add a semi-colon at the end of the line
1. Try to click the button after the page re-loads, and make sure a message appears!

```js
function run() {
    alert("Hello!");
}
```