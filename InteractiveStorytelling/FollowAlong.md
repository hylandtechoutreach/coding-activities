# Follow-Along: Interactive Storytelling
Follow these instructions to create your own story (like [this](https://hylandtechoutreach.github.io/coding-activities/Archive/TwineLesson/CompleteStory.html)) in [Twine](https://twinery.org)!

## Setup
First, get into Twine and create a new story.

1. Open [Twine](https://twinery.org/2/#/)
1. Click the "Skip" button
1. In the top left, click the "+ New" button
1. Enter a name for your story, like "A Day in the Life"
1. Click the "✓ Create" button to create the story!

## Starting the Story
Now that the story is setup up, it's time to start writing it! Double click on the "Untitled Passage" node to begin editing it. Stories usually begin with the main character waking up. For example:

>Your eyes slowly open. You check the clock, and see that it is 6:00am. Your bed is warm and cozy, but you know it's time to start your day.

1. Click the "Rename" button to change the name from "Untitled Passage" to "The Beginning"
1. In the text box, start typing the story
1. After typing, close the popup (the text will save automatically)
1. At the top of the screen, click the "Test From Here" button to see the story page!

## Adding an Image
Adding an **image** to a story can make it much more dynamic and engaging.

1. Open a new tab in Google Chrome, and go to [Google Images](https://google.com/images)
1. Search and find a picture (e.g., "alarm clock 6:00am" - https://www.ohsu.edu/sites/default/files/2019-06/insomnia-sleep.png)
1. Right click the picture, and select "Copy image address"  
1. Go back to the Twine story page, and double click the "The Beginning" passage
1. At the top of the text, add `<img src="">` on its own line  
	- This is the HTML code for a picture
1. Between the quotation marks (`"` and `"`), paste in the image URL with `Ctrl`+`v`  
	```html
	<img src="https://www.ohsu.edu/sites/default/files/2019-06/insomnia-sleep.png">
	```
1. Click the "Test From Here" button to make sure the image appears!

## Branching
Currently, the story is not very interactive. To make it more fun, use **links** to allow the user to choose a path for the main character.

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
[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) (**C**ascading **S**tyle **S**heets) is a styling language for the web. Almost every website uses CSS to change fonts, colors, layouts, and much more! Twine hosts stories on the web, so it is possible to use CSS to update the styles in a Twine story.

1. Go back to the Twine story page
1. From the top bar, select the "Story" option
1. Under that, click the "# Stylesheet" button
1. Add some CSS to update the `font-size`, `font-family`, text `color`, and `background-color` for the story:  
	```css
	tw-story {
		font-size: 20px;
		font-family: consolas;
		color: lightpink;
		background-color: darkblue;
	}
	```
4. From the top bar, select the "Build" option and click the "Play" button to see the story!

## Tracking Story Information with Variables
Twine also allows developers to keep track of different details throughout the story using **variables**. For example, the story could track how much money the main character has, their health level, their age, the weather, the time of day, or anything else!

### More on Variables
In computer science, **variables** are containers for information that can _change_. Variables have a name (e.g., `money`, `health`, `age`) and a value (e.g., `$5`, `90hp`, `11`). The _value_ of a variable can change throughout the story, but the _name_ will always stay the same. For example, if the main character in a story bought a banana and ate it, the `money` variable might go down to `$4.69`, and the `health` variable might go up to `95hp`.

## Creating the `GPA` variable
For the "A Day in the Life" story, the main character's GPA could change depending on the path the user takes. For example, if the main character skips school, their GPA could go down. If they go to school and work hard, their GPA could go up. Create a **`GPA` variable** to track this information throughout the story.

>If desired, create a different variable to track a different type of information, like the main character's `money`, `HP`, `stress`, or anything else!

1. Double click to open the "The Beginning" passage
1. At the top of the text, add the code `(set: $GPA to 2.5)` so the main character begins the story with a GPA of 2.5. Note the syntax:
	- Parentheses (`( )`)
	- `set: `
	- A dollar sign (`$`)
	- The name of the variable (`GPA`)
	- ` to `
	- The value of the variable (`2.5`)
1. Under the `(set:)` line, add the text `GPA: $GPA`
	- This will display the _value_ of the variable
1. Close out of the passage and click the "Play" button to verify that the GPA appears as expected!

## Updating the `GPA` Variable
Now that the main character's GPA has a starting value, it is possible to **update it** depending on the story branch.

1. In Twine, open up one of the passages where the main character's GPA might go down
1. At the top of the text, add the code `(set: $GPA to $GPA - 0.2)`
	- This will set the `GPA` variable to `.2` less than it was before
1. Close out of that passage, and open a passage where the main character's GPA would go up
1. At the top of the text, add the code `(set: $GPA to $GPA + 0.2)`
	- This will set the `GPA` variable to `.2` more than it was before

## Ending the Day
Eventually, the day in the story will come to an end. When this happens, it would make sense for every story branch to lead to the same place, regardless of how the main character ended up there. At that point, it would also make sense to display the final value for the `GPA` variable.

1. Update all of the current final passages so they link to a new passage: `[[Night falls]]`
1. Double click the "Night falls" passage to edit it
1. Add some text saying "The day has passed" or something similar
1. Add code to display the main character's final `GPA`
	- `GPA: $GPA`
1. Finally, click the "Play" button and play through the story in a few different ways! Try to make the final variable value change on different play-throughs.

## Next Steps
Try to continue the story with some new branches! Write it out on paper first to get an idea of where the story should go. Then, try to update the code to make it into a playable game! Feel free to elaborate on the existing story, or change it completely. Have fun!

### Challenge Ideas
Here are some ideas for things you could do next:

- Add a different image to every passage
- Add several new branches that take the main character on many new adventures
- Do some Google research to learn more about CSS, and update the styles for the story

### Sharing Stories
Follow [these instructions](SharingStories.md) to share your story!
