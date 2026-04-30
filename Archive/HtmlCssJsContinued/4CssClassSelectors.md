# CSS Class Selectors Lesson
Use this activity to introduce students to class selectors in CSS.

## Starter CodePen
Students should navigate to [bit.ly/selectorstart](https://codepen.io/jmaxwell/pen/mdVwzWP?editors=1100) to get the starter code. Display the link in very large font so they can see it, and make sure they type it in exactly like that (it is case-sensitive).

Explain that so far, the HTML contains several elements that tell the story of The Tortoise and the Hare. The goal of the activity is to style this page in CSS using **class selectors**! **Class selectors** allow developers to style specific elements, instead of styling all elements of a given type.

Tell the students that if they complete the activity with time to spare, they can participate in a Kahoot quiz.

## SKIP: Updating the `body` Styles
>Note: In the interest of time, these styles will already exist in the CodePen. Take a moment to explain them, but do not walk through adding them.

First, make some basic style updates to the whole page.

1. Expand the CSS section and click into it to start typing
1. Ask the students how to make a ruleset that will style all the content on the page
1. Add `body {}` to the CSS section
1. Ask the students how to set the background color to light yellow
1. Within the `body` ruleset, add `background: lightyellow;`
1. Ask the students how to set the font
1. Under the `background` declaration, set the `font-family` property to `garamond`
1. Make sure the page has a light yellow background and a fancy new font!

```css
body {
  background: lightyellow;
  font-family: garamond;
}
```

## SKIP: Updating the `img` Styles
>Note: In the interest of time, these styles will already exist in the CodePen. Take a moment to explain them, but do not walk through adding them.

Next, make a couple of updates to the image on the page.

1. Under the `body` ruleset, make some new lines
1. Ask the students how to make a ruleset to style the `img` element
1. Add `img {}` to the CSS section
1. Use the `float` property to make the image "float" to the `left`
    - `float: left`
1. Check the page to see that the image has floated left, causing the text to stack horizontally on the right!
1. Notice that now the text is right next to the image, which is too close
1. Under the `float` property, add a `margin` declaration
1. Show the students that it is possible to add _only_ a horizontal margin with `margin: 0 10px`
1. Make sure the text has moved away from the image a little bit!

```css
img {
  float: left;
  margin: 0 10px;
}
```

## Updating the Final Paragraph
Now it's time to start using some CSS classes! This way, it is possible to update the style of _only_ the final `p` element to make it stand out a little bit.

1. Expand the HTML section and find the final `p` paragraph element
1. Right after the `p`, before the greater-than sign, make a space and add `class`, then an equals sign, then quotes, then `final`
1. Ask the students if this looks familiar - it's a lot like adding `src` to an image or `href` to a link!
1. Expand the CSS section and go to the bottom of the text
1. Make a new ruleset with a selector of `.final` - this is a class selector!
1. Explain that every style in that ruleset will _only_ apply to HTML elements that have a `class` of `first`
1. In the `.first` ruleset, add a `coloe` declaration
1. Set the value of the `color` property to be `purple`
1. On the page, verify that the final paragraph is purple, but none of the other ones changed!
1. In the `.first` ruleset, add another declaration for `font-weight`
1. Set the value of the `font-weight` property to `bold`
1. Verify that the final paragraph is bold and purple!

```css
.final {
  color: purple;
  font-weight: bold;
}
```

## Updating the First Paragraph
Next, use the same method to update the styles of _only_ the first `p` element of the page.

1. Expand the HTML section and find the first `p` paragraph element
1. Right after the `p`, before the greater-than sign, ask the students how to add the class
1. Make a space and add `class="first"`
1. Expand the CSS section and go to the bottom of the text
1. Make a new ruleset with a selector of `.first` - this is another class selector!
1. In the `.first` ruleset, add a `font-style` declaration
1. Set the value of the `font-style` property to be `italic`
1. On the page, verify that the first paragraph is in italics!

```css
.first {
  font-style: italic;
}
```

## Final Code
At the [end of the activity](https://codepen.io/jmaxwell/pen/mdVwGNy), the code should look like this:

### HTML
```html
<h1>The Tortoise And The Hare</h1>

<img src="https://i.imgur.com/T6qJeaP.jpg">

<p class="first">A Hare was making fun of the Tortoise one day for being so slow.</p>

<p>The Hare was much amused at the idea of running a race with the Tortoise, but for the fun of the thing he agreed. So the Fox, who had consented to act as judge, marked the distance and started the runners off.</p>

<p>"Do you ever get anywhere?" he asked with a mocking laugh.</p>

<p>"Yes," replied the Tortoise, "and I get there sooner than you think. I'll run you a race and prove it."</p>

<p>The Hare was soon far out of sight, and to make the Tortoise feel very deeply how ridiculous it was for him to try a race with a Hare, he lay down beside the course to take a nap until the Tortoise should catch up.</p>

<p>The Tortoise meanwhile kept going slowly but steadily, and, after a time, passed the place where the Hare was sleeping. But the Hare slept on very peacefully; and when at last he did wake up, the Tortoise was near the goal. The Hare now ran his swiftest, but he could not overtake the Tortoise in time.</p>

<p class="final">Slow and steady wins the race.</p>
```

### CSS
```css
body {
  background: lightyellow;
  font-family: garamond;
}

img {
  float: left;
  margin: 0 10px;
}

.first {
  font-style: italic;
}

.final {
  font-weight: bold;
  color: purple;
}
```

## Kahoot Quiz
If there is a decent chunk of time left after the activity (15 minutes or so), there is a Kahoot that covers the content from the HTML & CSS lessons so far.

- [View](https://create.kahoot.it/share/a199e4fd-56ab-4f5b-b94e-e3e8169e4956)
- [Play](https://play.kahoot.it/v2/?quizId=a199e4fd-56ab-4f5b-b94e-e3e8169e4956)

## Individual Work
With any remaining time, give the students some time to work individually. Here are some ideas for challenges:

- Shrink the image by setting the `height` property in the `img` ruleset
- Create a new `h1` ruleset and center the header with the `text-align` property
- Change the font size of the final message to be larger using the `font-size` property
- Use a new class to change the `color` of the second paragraph to `red`
    - Add the `class` attribute in the HTML (`class="red"`)
    - Create a new `.red` ruleset in the CSS, and set the `color` to `red` within it

As the students work individually, be available to answer any questions they may have.

