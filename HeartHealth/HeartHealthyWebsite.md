# Heart Healthy Website
In this activity, use HTML and CSS to update a heart healthy website and make it your own!

## Overview of HTML, CSS, and repl.it
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) is a **language** that lets developers to create websites. A web browser takes the HTML code, and displays it as a nice-looking webpage.
- [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS) is a **language** that lets developers add style to websites. This includes things like fonts, colors, and more.
- [repl.it](https://repl.it) is a **website** that lets developers create websites.

## Website Setup
To get started, follow the steps below. In order to make the setup quicker, you can use the following credentials:

- username: **hylandstudent**
- password: **hyland**

1. Go to the existing [Heart-Healthy Website](https://repl.it/@JosephMaxwell/HeartHealthy#index.html)
1. At the top of the page, find and click the "Fork" button to create a fork of this project  
    ![](https://i.imgur.com/IfErZpJ.png)
1. If you already have an account, click the "log in" link  
    ![](https://i.imgur.com/oJ85Q3L.png)
1. From there, enter your account information and click the "Log in" button  
    ![](https://i.imgur.com/z8bjCsB.png)
1. Next, click the "Run" button at the top of the page to build the website from the HTML  
    ![](https://i.imgur.com/5KMRAQO.png)
1. Verify that both the HTML code _and_ the website appear on the page!
    - _NOTE: Make sure to zoom in so everything is easy to read_

At this point, it should look something like this:

![](https://i.imgur.com/aM7Q9Rw.png)

## Looking at the HTML
Notice how the code in the HTML creates the text on the website. Everything in HTML goes between _tags_, which tell the website what type of element to display.

- The text between the `<h1>` and `</h1>` tags becomes a large header
- The text between the `<p>` and `</p>` tags becomes normal sized text
- The text within the `<li>` and `</li>` tags are bulleted items in a list

The website looks okay, but there's a lot we can do to make it better. The first thing to do is update the header text with your name! For example, if my name were **Katara**, I could change the header so that it said **Katara's Heart Healthy Website**.

Update the code in the HTML section, _between_ the `<h1>` and `</h1>` tags. It should look something like this:

```html
<h1>Katara's Heart Healthy Website</h1>
```

Click the "Run" button again, and make sure the text on the website updates with the new header!

## Adding an Image
Almost every website has at least one image, and we would like our website to have one too! In fact, the code already has the proper tag in place! All we need to do is find an image, and paste the URL into the HTML code.

1. Go to the [Heart Images](HeartImages.md) page, and find a heart that you like
1. Copy the URL listed above the heart by highlighting the text, right clicking, and selecting "Copy"
1. Go back to the Repl
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
1. Go back to the Repl
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

1. Take a look at the code within the `<style></style>` tags, and try to figure out what it does
1. Find the area where it sets the background color - `background: white`
1. Change the "white" to "pink" to change the background color
1. Next, find the area where the CSS sets the text color - `color: black`
1. Change the "black" to "red" to change the text color
1. Click the "Run" button again, and verify that the colors have updated on the website!

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
1. Go back to the Repl
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
To share your website, you can copy the URL from the bar at the top of the website:

![](https://i.imgur.com/mShir0v.png)

Paste the link anywhere to share it.

## Additional Topics
If there is time remaining, there are a lot of additional updates we could make on our website. Some of them can be found here: [Additional Topic Challenges](../HtmlCssJsContinued/AdditionalTopicChallenges.md)