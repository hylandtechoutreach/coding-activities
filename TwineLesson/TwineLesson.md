# Twine
An activity to introduce [Twine](http://twinery.org/2/#!/welcome) in 45-60m. Twine is an open-source tool for telling interactive, nonlinear stories. The goal of this lesson is to build a simple interactive fiction story using Twine. It uses CSS for styling, and introduces variables as a way to keep track of information throughout a story.

>**Instructor Note**: It may be beneficial to allow the students drive the story writing process. Take suggestions from them for the content of the story, the branches, the characters, etc. Make sure their suggestions are conducive to a story with at least one variable, and multiple branches reaching the same node.

### Example
<a href="CompleteStory.html" target="_blank">Complete Story</a>

## Getting Started
### Setup
1. Go to [twinery.org](http://twinery.org/)
1. In the upper right corner, click the "Use it online" link  
    ![](https://i.imgur.com/Y30eOGr.png)
1. On the next screen, click the "Skip" link  
    ![](https://i.imgur.com/u8m12uI.png)
1. On the right side of the screen, click the "+ Story" button  
    ![](https://i.imgur.com/Degn7nB.png)
1. Enter a name for the story, and click the "+ Add" button  
    ![](https://i.imgur.com/0WfuXjl.png)
1. In the lower left corner, click the story name menu and select "Change Story Format"  
    ![](https://i.imgur.com/B06p281.png)
1. Select the "SugarCube 23.0.0" option, and then close out of the menu  
    ![](https://i.imgur.com/LV50DLk.png)

### Starting the Story
Now that the story is setup up, it's time to start writing it! Double click on the "Untitled Passage" node to begin editing it. Stories usually begin with the main character waking up. For example:
> Your eyes slowly open. You check the clock, and see that it is 6:00am. Your bed is warm and cozy, but you know it's time to start your day.

1. Change the name from "Untitled Passage" to "The Beginning"
1. In the text box, remove the text and start typing the story
1. After typing, close the popup (the text will save automatically)
1. In the lower right corner of the screen, click the "Play" button to see the story so far!

### Adding an Image
In Twine, it is possible to add images to stories.

1. Open a new tab in Google Chrome, and go to [Google Images](https://images.google.com/)
1. Search and find a picture (e.g., "alarm clock 6:00am" - https://www.ohsu.edu/sites/default/files/2019-06/insomnia-sleep.png)
1. Right click the picture, and select "Copy image address"  
	![](https://i.imgur.com/yLXXvwC.png)
1. Go back to the Twine story page, and double click the "The Beginning" passage
1. At the top of the text, add `[img[]]` on its own line
1. Between the empty square brackets (`[` and `]`), paste in the image URL with `Ctrl`+`v`  
	```
	[img[https://www.ohsu.edu/sites/default/files/2019-06/insomnia-sleep.png]]
	```
1. Click the "Play" button to make sure the image appears!

### Branching
Currently, the story is not very interactive. To make it more fun, use links to allow the user to choose a path for the main character.

1. Double click the "The Beginning" passage to edit it again
1. Make a few new lines under the existing text
1. To create a _link_, add another line of text, surrounded by `[[` and `]]`
	- For example, `[[Wake up]]`
1. To create another option for the user, add another link beneath the existing link
	- For example, `[[Stay in bed]]`
1. Close out of the "The Beginning" passage, and notice that two new passages were automatically created
1. Double click the first branch, and fill in some text
	- Ex: `You wake up and get out of bed, ready to face the day!`
1. Double click the second branch, and fill in some different text
	- Ex: `You continue to sleep happily.`
1. Click "Play" again to see how the links work in the story!

#### Challenge: Branching the Branch
Choose one of the paths, and add another pair of branches to continue the story. Use links `[[like this]]` to create the branching passages.

## Styling the Story with CSS
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) (**C**ascading **S**tyle **S**heets) is a styling language for the web. Almost every website uses CSS to change fonts, colors, layouts, and much more!

### CSS in a Web Browser
It is possible to demonstrate the use of CSS in Google Chrome using [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools). This toolset allows developers to update CSS for a webpage right from the browser!

1. Open a new tab in Google Chrome, and go to a Wikipedia page
	- Ex: [Choose Your Own Adventure](https://en.wikipedia.org/wiki/Choose_Your_Own_Adventure)
1. Press the `F12` key to open Chrome DevTools
	- This allows developers to see all of the HTML and CSS that creates the webpage
1. Find the "Styles" section, and click the `+` button to create a new style rule  
	![](https://i.imgur.com/lWZeJDR.png)
1. For the style _selector_, enter `body`
	- This means that the styles will apply to everything on page
1. Click in between the curly brackets (`{` and `}`)
1. Type in `font-size: 20px`, and press the `Enter` key
	- This should make the text on the page bigger
1. Click between the curly brackets again, and type in `font-family: cursive`
	- This should change the font of the text on the page

```css
body {
	font-size: 20px;
	font-family: cursive;
}
```

These are only a couple of the styles in CSS. There are many more to explore!

### CSS in Twine
Twine hosts stories on the web, so it is possible to use CSS to update the styles for those pages too!

1. Go back to the Twine story page in Chrome
1. In the lower left corner, click the story name menu and select "Edit Story Stylesheet"
1. Add some CSS to update the `font-size`, `font-family`, text `color`, and `background-color` for the story:  
	```css
	body {
		font-size: 20px;
		font-family: consolas;
		color: lightpink;
		background-color: darkblue;
	}
	```
1. Close out of the stylesheet, and click "Play" to see the styles in the story!

### Choosing Custom Colors for CSS
Some color names like "lightpink" and "darkblue" are built into the web already, but it is also possible to choose custom colors using RGB values! The [RGB color model](https://en.wikipedia.org/wiki/RGB_color_model) is an additive color model in which red, green and blue light are added together in various ways to reproduce a broad array of colors. Basically, it is possible to create any digital color with a combination of red, green, and blue!

Each color (R, G, and B) can take a number from 0 to 255. This represents the amount of the color in the mix. For example, a color with a Red value of 255, a Green value of 0, and a Blue value of 0 would be red.

The combinations are almost endless! Google has a [built-in color picker](https://www.google.com/search?q=color+picker) that developers and designers can utilize to find the perfect color. It displays RGB colors in the HEX format like so:

```
#7b95a8
```

To use that color in CSS, copy the number (including the `#`) and paste it into the CSS where a color would go! Try out some different colors for the page to find the best ones.

## Tracking Story Information with Variables
Twine also allows developers to keep track of different details throughout the story using variables. For example, the story could track how much money the main character has, their health level, their age, the weather, the time of day, or anything else!

### More on Variables
In computer science, **variables** are containers for information that can _change_. Variables have a name (e.g., `money`, `health`, `age`) and a value (e.g., `$5`, `90hp`, `11`). The _value_ of a variable can change throughout the story, but the _name_ will always stay the same. For example, if the main character in a story bought a banana and ate it, the `money` variable might go down to `$4.69`, and the `health` variable might go up to `95hp`.

### Creating the `GPA` variable
For the "A Day in the Life" story, the main character's GPA could change depending on the path the user takes. For example, if the main character skips school, their GPA could go down. If they go to school and work hard, their GPA could go up. Create a `GPA` variable to track this information throughout the story.

>If desired, create a different variable to track a different type of information, like the main character's `money`, `HP`, `stress`, or anything else!

1. Double click to open the "The Beginning" passage
1. At the top of the text, add the code `<<set $GPA to 2.5>>` so the main character begins the story with a GPA of 2.5. Note the syntax:
	- Less-than and greater-than signs (`<< >>`)
	- `set`
	- A dollar sign (`$`)
	- The name of the variable (`GPA`)
	- `to`
	- The value of the variable (`2.5`)
1. Under the `<<set>>` line, add the text `GPA: $GPA`
	- This will display the _value_ of the variable
1. Close out of the passage and click the "Play" button to verify that the GPA appears as expected!

### Updating the `GPA` Variable
Now that the main character's GPA has a starting value, it is possible to update it depending on the story branch.

1. In Twine, open up one of the passages where the main character's GPA might go down
1. At the top of the text, add the code `<<set $GPA to $GPA - 0.2>>`
	- This will set the `GPA` variable to `.2` less than it was before
1. Close out of that passage, and open a passage where the main character's GPA would go up
1. At the top of the text, add the code `<<set $GPA to $GPA + 0.2>>`
	- This will set the `GPA` variable to `.2` more than it was before

### Ending the Day
Eventually, the day in the story will come to an end. When this happens, it would make sense for every story branch to lead to the same place, regardless of how the main character ended up there. At that point, it would also make sense to display the final value for the `GPA` variable.

1. Update all of the current final passages so they link to a new passage: `[[Night falls]]`
1. Double click the "Night falls" passage to edit it
1. Add some text saying "The day has passed" or something similar
1. Add code to display the main character's final `GPA`
	- `GPA: $GPA`
1. Finally, click the "Play" button and play through the story in a few different ways! Try to make the final variable value change on different play-throughs.

## Next Steps
Try to continue the story with some new branches! Write it out on paper or in Notepad first to get an idea of where the story should go. Then, try to update the code to make it into a playable game! Feel free to elaborate on the existing story, or change it completely. Have fun!

### Challenge Ideas
- Add a different image to every passage
- Add a new variable to keep track of something else throughout the story
- Add several new branches that take the main character on many new adventures
- Do some Google research to learn more about CSS, and update the styles for the story