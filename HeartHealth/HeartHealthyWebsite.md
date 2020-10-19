# Heart Healthy Website
In this activity, use HTML and CSS to update a heart healthy website and make it your own!

## Overview of HTML, CSS, and CodePen
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) is a **language** that lets developers to create websites. A web browser takes the HTML code, and displays it as a nice-looking webpage.
- [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) is a **language** that lets developers add style to websites. This includes things like fonts, colors, and more.
- [CodePen](https://codepen.io/trending) is a **website** that lets developers create websites.

## Signing Up for CodePen
In order to create and save a new website project, it will be necessary to make a CodePen account. This is completely free, and it does not require email verification.

1. Go to the [CodePen Sign Up Page](https://codepen.io/accounts/signup/user/free)
1. On the sign up page, lick on the "Sign Up with Email" button under "Or,"  
    ![](https://i.imgur.com/HinQ4Ah.png)
1. Enter a name, username, email, and password in the text boxes below the button  
    ![](https://i.imgur.com/xXgOJ7u.png)
1. Click the "Submit" button  
    ![](https://i.imgur.com/dmSbsSV.png)
1. You now have a CodePen account! On the next page, click the "X" in the upper right of the popup  
    ![](https://i.imgur.com/UbyMYMi.png)

That's all!

## Website Setup
To get started:

1. Go to the existing [Heart-Healthy Website](https://codepen.io/jmaxwell/pen/OJXXBrG?editors=1000)
1. In the bottom right corner, find and click the "Fork" button to create a fork of this project  
    ![](https://i.imgur.com/z0Tx0FM.png)
1. In the upper right, click on the "Change View" button
1. In the menu that appears, click on the "Editor Layout" option on the left:  
    ![](https://i.imgur.com/j7UFrDT.png)
1. Verify that both the HTML code _and_ the website appear on the page!
    - _NOTE: Make sure to zoom in so everything is easy to read_

At this point, it should look like this:

![](https://i.imgur.com/9V1zmgH.png)

### Looking at the HTML
Notice how the code in the HTML creates the text on the website. Everything in HTML goes between _tags_, which tell the website what type of element to display.

- The text between the `<h1>` and `</h1>` tags becomes a large header
- The text between the `<p>` and `</p>` tags becomes normal sized text
- The text within the `<li>` and `</li>` tags are bulleted items in a list

The website looks okay, but there's a lot we can do to make it better. The first thing to do is update the header text with your name! For example, if my name were **Katara**, I could change the header so that it said **Katara's Heart Healthy Website**.

Update the code in the HTML section, _between_ the `<h1>` and `</h1>` tags. It should look something like this:

```html
<h1>Katara's Heart Healthy Website</h1>
```

Make sure the text on the website updates with the new header! Click the "Save" button in the upper right to make sure all changes have been saved. Continue to save throughout the activity!

![](https://i.imgur.com/mjKuMUU.png)

## Adding an Image
Almost every website has at least one image, and we would like our website to have one too! In fact, the code already has the proper tag in place! All we need to do is find an image, and paste the URL into the HTML code.

1. Go to the [Heart Images](HeartImages.md) page, and find a heart that you like
1. Copy the URL listed above the heart by highlighting the text, right clicking, and selecting "Copy"
1. Go back to the CodePen
1. In the HTML section, find the `<img src="" />` tag
1. Click right between the two quotes (`"` and `"`)
1. Paste in the URL by right clicking and selecting "Paste"
1. Verify that the image appears on the website!

The code for the image should look something like this:

```html
<img src="https://i.imgur.com/OEtKLe4.png" />
```

## Updating the List
Currently, the list of heart-healthy foods only has placeholder items. We want it to have some real foods! Update the HTML code so that the website displays a list of foods.

1. Go to the [Heart-Healthy Foods](HeartHealthyFoods.md) page to find a list of some heart healthy foods
1. Select three of your favorite foods from the list
1. Go back to the CodePen
1. In the HTML section, find the `<ul></ul>` tags
    - This is code for the list on the website!
1. Update the text between each `<li>` and `</li>` with one of the heart-healthy foods from the list
1. Verify that the new foods appear in the list on the website!

The code for the list should look something like this:

```html
<ul>
  <li>
    Beans
  </li>
  <li>
    Spinach
  </li>
  <li>
    Dark Chocolate
  </li>
</ul>
```

## Updating the Colors
So far, we have updated the content of the website with HTML, but we haven't done anything with the style. That's where CSS comes in! CSS can change the style of the page, without affecting the content.

1. On the left side of the CodePen, drag up the CSS section from under the HTML  
    ![](https://i.imgur.com/wTgXSj5.png)
1. Take a look at the code in the CSS section, and try to figure out what it does
1. Find the area where it sets the background color: `background: white`
1. Change the "white" to "pink" to change the background color
1. Next, find the area where the CSS sets the text color: `color: black`
1. Change the "black" to "red" to change the text color
1. Verify that the colors have updated on the website!

The CSS code should look something like this:

```css
body {
    font-family: arial;
    font-size: 20px;
    background: pink;
    color: red;
}
```

## Using Custom Colors
Some basic colors are built into the web (like **pink** and **red**), but it is also possible to use custom colors! Each color can be represented as a _hexidecimal color code_, which is a hashtag (`#`) followed by six alphanumeric characters. The easiest way to find a specific color is to use a color picker. Follow the steps below to update the colors on the website.

1. Go to [Google's Color Picker](https://www.google.com/search?q=color+picker)
1. Drag the two sliders around to select a new shade of pink  
    ![](https://i.imgur.com/Q6lxVvu.png)
1. Once a color is selected, highlight the "HEX" code text under the color picker, and copy it
    ![](https://i.imgur.com/ZnYw6fa.png)
1. Go back to the CodePen
1. Remove the "pink" from the CSS, and paste in the new hex code
1. Verify that the new background color appears on the website!
1. Repeat the steps above to change the color of the text to another custom color

The CSS code should look something like this:

```css
body {
    font-family: arial;
    font-size: 20px;
    background: #ffbdbd;
    color: #bf3636;
}
```

## Finishing Up
Our website is looking pretty good now! Certainly a lot better than it started. It should look something like this:

![](https://i.imgur.com/5uzBh7h.png)

Congratulations, you've successfully built a heart healthy website!

## Sharing
To share your website, you can copy the URL from the address bar at the top of the browser:

![](https://i.imgur.com/pKxx7mf.png)

Make sure you save it first!

## Additional Topics
If there is time remaining, there are a lot of additional updates we could make on our website. Some of them can be found here: [Additional Topic Challenges](HtmlCssJsContinued/AdditionalTopicChallenges.md)