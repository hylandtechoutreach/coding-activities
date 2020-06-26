# CSS Box Model Lesson
Use this activity to introduce students to the basic box model:

![](https://i.imgur.com/C5LUqrU.png)

## Review Kahoot
Start with a Kahoot quiz covering some of the concepts the students should have seen already. This will give them a refresher on some of the syntax and should lead into the activity.

- [View](https://create.kahoot.it/details/basic-html-css-activities-quiz/4160a857-ccdf-4e7d-8d5b-f0c6b230e19d)
- [Play](https://play.kahoot.it/v2/?quizId=4160a857-ccdf-4e7d-8d5b-f0c6b230e19d)

## Starter CodePen
Students should navigate to [bit.ly/boxmodelstart](https://codepen.io/jmaxwell/pen/wvMeQNZ?editors=0100) to get the starter code. Display the link in very large font so they can see it, and make sure they type it in exactly like that (it is case-sensitive).

Explain that so far, the HTML contains several `img` elements with pictures of cats. The goal of the activity will be to use CSS to frame the images so they display nicely on the page!

## Selecting All `img` Elements
The first thing to do is create a ruleset in CSS that will style all the images in the HTML.

1. Expand the CSS section in the CodePen
    - Make sure students are typing in the correct area!
1. Ask the students how to _select_ `img` elements
    - Use `img`, the element selector
1. Ask students what to use to create the ruleset
    - Use `{}` (curly brackets)
1. Create the ruleset, and press Enter between the brackets to make space
1. Note that this will not do anything yet - there are no declarations in the ruleset!

### Code
```css
img {

}
```

## Setting the Height of All Images
Next, to make the page a little neater, set each image to be the same height.

1. Within the `img` ruleset, add the _property_ to set the height
    - Students can guess what it is: `height`
1. Ask students what comes next in a CSS declaration
    - `:` (colon)
1. Ask students what the _value_ should be
    - `300px` (a number, followed by "px")
1. Ask students what comes next, to end the declaration
    - `;` (semi-colon)
1. The height of the images should change on the page!

### Code
```css
img {
    height: 300px;
}
```

## Box Model Overview
Show the students the box model diagram from [this page](https://www.w3schools.com/css/css_boxmodel.asp). Explain that each HTML element has space around it that can be updated with padding, borders, and margins.

## Adding a Border to All Images
Frame each picture using the CSS `border` property.

1. Within the `img` ruleset, make a new line under the `height` declaration
1. Create a new declaration to set the `border` property
1. Explain that the `border` property has three parts: thickness, style, and color
    - There are spaces between each of these values
1. Add the value for `border` so that the border is three pixels thick, solid, and black
    - `border: 3px solid black`
1. Tell the students they can experiment with other values for the border, including styles:
    - `dotted`
    - `dashed`
    - `solid`
    - `double`
    - `groove`
    - `ridge`
    - `inset`
    - `outset`
1. Make sure to add the semi-colon at the end of the line
1. Check the page to see the border!

### Code
```css
img {
    height: 300px;
    border: 3px solid black;
}
```

## Adding Padding Between the Images and Borders
Next, add some space _within_ the border around the image with the `padding` property.

1. Within the `img` ruleset, make a new line under the `border` declaration
1. Create a new declaration to set the `padding` property
    - Ask the students what comes after the property name (a colon)
1. Explain that the `padding` property will add space around HTML content inside of the border
1. Ask the students to guess what measurement the padding will use: `px` (pixels)
1. Add the value for the `padding` so that the padding adds five pixels of space
    - `padding: 5px`
1. Make sure to add the semi-colon at the end of the line
1. Check the page to see the added space!

### Code
```css
img {
    height: 300px;
    border: 3px solid black;
    padding: 5px;
}
```

## Adding Margins Around the Images
Next, add some space _outside_ the border for the image with the `margin` property.

1. Within the `img` ruleset, make a new line under the `padding` declaration
1. Create a new declaration to set the `margin` property
    - Ask the students what comes after the property name (a colon)
1. Explain that the `margin` property will add space around HTML content outside of the border
1. Ask the students to guess what measurement the margin will use: `px` (pixels)
1. Add the value for the `margin` so that it adds twenty pixels of space
    - `margin: 20px`
1. Make sure to add the semi-colon at the end of the line
1. Check the page to see the added space!

### Code
```css
img {
    height: 300px;
    border: 3px solid black;
    padding: 5px;
    margin: 20px;
}
```

## Individual Work
At this point, give the students some time to work individually. Here are some ideas for challenges:

- Add a header at the top of the HTML
- Add a new image in the HTML
- Set the `width` of the images instead of the `height` to see how it looks
- Change the border thickness, style, and color

As the students work on those, be available to answer any questions they may have.

## Extra Concepts
Once the basic activity has been completed, there are a few additional advanced features to share with the students. Go over these if there is enough time remaining. There should be at least 15 minutes to cover these topics.

### Changing the Border on Hover
It is possible to change styles on a page when the user hovers over an element. Use this concept to update the border style!

1. Make some new lines in the CSS section _under_ the closing bracket of the `img` ruleset
1. Create a _new_ ruleset with `img:hover` that will select the `img` elements when they are hovered over
1. Within the new ruleset, make a new `border` declaration
1. Ask the students how to set the border to be three pixels thick, dotted, and green
1. Make sure to add the semi-colon at the end of the line
1. On the page, hover over the images and make sure the border turns dotted and green!

#### Code
```css
img:hover {
    border: 3px dotted green;
}
```

### Rotating the Images on Hover
It is also possible to _rotate_ HTML elements using the `transform` property. Use this property to slightly turn the images when they are hovered over!

1. Make a new line under the `border` declaration in the `img:hover` ruleset (above the closing curly bracket)
1. Make a new declaration for `transform`
1. Ask the students what comes after the property name (a colon)
1. Explain that the value for the `transform` property is a little different - there are a lot of options
1. Set the value to rotate the image five degrees
    - `transform: rotate(5deg)`
1. Make sure to use the parentheses properly - it should look exactly that way
1. Add a semi-colon at the end of the line
1. On the page, hover over the images and make sure they rotate!

#### Code
```css
img:hover {
    border: 3px dotted green;
    transform: rotate(5deg);
}
```

### Setting the Transition Speed
Right now, when hovering over an image, it transitions immediately. This can be a little jarring, so use the `transition` property to set the speed of the transition!

1. Find the `img` ruleset in the CSS section, and make a new line at the bottom (above the closing bracket)
1. Set the `transition` property to a value of `300ms`
1. On the page, hover over the images and make sure they transition slowly!

#### Code
```css
img {
  height: 300px;
  border: 3px solid black;
  padding: 5px;
  margin: 20px;
  transition: 300ms;
}
```

## Final Code
At the [end of the activity](https://codepen.io/jmaxwell/pen/xxZryNG), the CSS section should have the following code:

```css
img {
  height: 300px;
  border: 3px solid black;
  padding: 5px;
  margin: 20px;
  transition: 300ms;
}

img:hover {
  transform: rotate(5deg);
  border: 3px dotted green;
}
```