# HTML and CSS Lesson
An activity to introduce HTML and CSS in 45-60m

## Explain HTML
Start by showing an example webpage (e.g., https://en.wikipedia.org/wiki/SpongeBob_SquarePants) in Google Chrome. Talk to the students about their experience with the web. Then, right click on the page and view the source to show the HTML that builds the page.

### What is HTML
- HTML tells an internet browser what to show on a website
    - Ask students to name internet browsers (chrome, firefox, etc.)
- HTML elements are the building blocks of a webpage
- Browsers use HTML elements to display webpages

## Create a Webpage
Students should follow along to create their own webpages!

### Basic HTML
1. Open a new CodePen: https://codepen.io/pen/ 
    - This allows developers to write HTML code and see it _render_ immediately
    - Display the URL in a large font so the students can see it and navigate there
2. Change the view so the code appears on the left and the webpage appears on the right
3. Minimize the JS section
4. In the HTML section, add an `h1` header element saying "My Awesome Website"
    - Explain that this is used for page titles, and there are also smaller header elements (`h2`-`h6`)
5. Add a `p` paragraph element with a greeting
    - Explain that this is used for regular text on the page

```html
<h1>My Awesome Website</h1>
<p>Hi, I'm me.  Welcome to my awesome website.</p>
```

### Lists
1. Add an `h2` for "My Hobbies" beneath the `p`
1. Add a `ul` that will contain a list of hobbies beneath the `h2`
    - Pause to ask students if they can guess what the `ul` will be
1. Add `li` elements as children of the `ul`
    - Ask them if they can guess what `li` means
1. Show them that there are both unordered _and_ ordered lists in HTML (`ol`)

```html
<h2>My Hobbies</h2>
<ul>
    <li>Reading</li>
    <li>Writing</li>
    <li>Petting Cats</li>
</ul>
```

## Styles with CSS
The current webpage looks fairly boring. Explain that developers use CSS to make their webpages look fun and exciting. HTML is like the skeleton, just the structure of the webpage, and CSS is like the clothes that it wears, giving it style.

1. In the CSS section, add a ruleset to select `body`
1. Add some declarations to update the text color, background color, and font of the page

```css
body {
    color: pink;
    background: black;
    font-family: Consolas;
}
```

### Color Picker
Some basic colors are built into the web, but it is also possible to use custom colors. Explain that each pixel on a computer screen has a color that comes from three values: Red, Blue, and Green (RGB). The final pixel color is the mix of each of those colors at different levels. For more information about the RGB color model, check out the [Wikipedia page](https://en.wikipedia.org/wiki/RGB_color_model). These RGB values can be represented in Hexidecimal, where two digits represent one number between 0 and 255. Combining those three numbers (one for red, one for blue, and one for green) into a six digit _hex code_ allows developers to easily reference colors.

1. Open a new tab in Google Chrome
1. Search for "color picker" in the search bar
1. Drag the pointer to select a desired color
1. Copy the hex value (starting with `#`)
1. Paste the hex value where a color name would go in the CSS!

```css
body {
    color: #f54594;
    background: #4a0021;
    font-family: Consolas;
}
```

## Adding an image
1. In the HTML section, add an `h2` saying "A Cool Image"
2. Beneath the `h2`, add an `img` element to the page
    - This will not do anything
    - Ask the students what is needed to create an image (the image)
3. Search for an image of a cat using Google Images in Chrome
4. Right click and select "Copy image address"
    - Do not copy the image itself, that will not work!
5. Add a `src` attribute to the `img` element, and paste in the URL for the image
6. Finally, in the CSS section, select the `img` element and set the `height` so that it fits on the page

```html
<h2>A Cool Image</h2>
<img src="https://images.unsplash.com/photo-1482066490729-6f26115b60dc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&w=1000&q=80">
```

```css
img {
    height: 200px;
}
```

## Final
https://codepen.io/jmaxwell/pen/NVjrpQ?editors=1100

## Saving
If the students would like to save their webpages, they can click the "Save" button. They will have to create an account, but it is totally free. After they save their Pen, the can copy the URL from the address bar and revisit it to see their website! Make sure they have enough time to create accounts before the end of the session. After that, they can continue to save any changes they make by clicking the "Save" button.

## Additional Topics
If there is time remaining, students can make updates to their website. If there is interest, show them some other things they can do with HTML and CSS. There are some challenges that can be completed as a class or by students individually: [Additional Topic Challenges](HtmlCssJsContinued/AdditionalTopicChallenges.md)