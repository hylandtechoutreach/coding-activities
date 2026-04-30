# Animation Lesson Part 1 - Snap!
Snap is a programming environment where developers can drag and drop blocks of code to create applications. Go to https://snap.berkeley.edu/snapsource/dev/snap.html to begin!

## Page Sections
![](https://i.imgur.com/jcmHn2a.png)

- **Blocks:** This pane on the left is where the Snap blocks live. They can be dragged to the **Scripts** section to create code.
- **Scripts:** This central part is where the code for the program lives. Drag blocks from the **Blocks** section into this section to create code.
- **Stage:** On the top right, this is where the program will execute. This is how users interact with the developed applications.
- **Sprites:** On the bottom right, this is where all of the _sprites_ appear. A sprite is a character or object within a Snap application that can interact with the user.

## Basic Sprite Movement
1. At the top of the **Blocks** section, click _Control_ to view the Control blocks
1. Find the ![](https://i.imgur.com/hVrmVxa.png) block, and drag it to the **Scripts** area  
1. At the top of the **Blocks** section, click _Motion_ to view the Motion blocks
1. Find the "change x by {10}" block, and _snap_ it under the "when" block in the **Scripts** area:  
    ![](https://i.imgur.com/Y3QWa5B.png)
1. On the "when" block, click the dropdown where it says "space" and change it to "right arrow"
1. On the **Stage**, see the sprite move to the right while pressing the right arrow key!

Create similar movement scripts for _left_, _up_, and _down_. Note that the "change x by..." block will move the sprite _horizontally_ (left and right), and the "change y by..." block will move the sprite _vertically_ (up and down).

## Left and Right
1. Within the "if" blocks for left and right movement, add ![](https://i.imgur.com/Ij5razi.png) blocks so that the sprite faces the proper direction
    - Use the dropdown to set the direction
1. Above the **Sprites** area, click the two-sided arrow to make the sprite only face left or right, not upside down:  
    ![](https://i.imgur.com/eedpGWz.png)

## Smoother Movements
With the existing code, the sprite does not move very smoothly. Update the code so that it constantly checks if a keys are pressed instead of simply responding to keypresses.

1. Drag all of the code scripts out of the stage so they disappear
1. Drag over a ![](https://i.imgur.com/sUQuf19.png) block from the _Control_ section
    - This will cause the following blocks to execute when the user clicks the green flag
1. Under the "When" block, drag over a ![](https://i.imgur.com/f0mf813.png) block from the _Control_ section
    - This will cause the blocks within to execute repeatedly forever
1. Within the "forever" block, drag a ![](https://i.imgur.com/N29G17D.png) block
1. In the empty space next to the "if", drag a ![](https://i.imgur.com/MetLsie.png) block from the _Sensing_ section
1. Within the "key pressed" block, click the dropdown where it says "space" and change it to "left arrow"
    - This will cause the blocks within the "if" to execute only **if** the left arrow key is pressed
1. Within the "if" block, drag a ![](https://i.imgur.com/UmyNtt7.png) block from the _Motion_ section
    - Change the value to "-3"
1. Above the "change" block, add a ![](https://i.imgur.com/Ij5razi.png) block so that the sprite faces the proper direction
    - Use the dropdown to set the direction
1. Above the **Sprites** area, click the two-sided arrow to make the sprite only face left or right, not upside down:  
    ![](https://i.imgur.com/eedpGWz.png)
1. Click the green flag, and see the sprite move on the **Stage** while pressing the right arrow key!

![](https://i.imgur.com/887dbhu.png)

>Note: If the sprite goes off the screen, right click it in the **Sprites** section and select "show"  
>![](https://i.imgur.com/XFL2qrG.png)

Update the movement scripts for _right_, _up_, and _down_ as well. Make sure to point in the proper direction when moving to the right!

## Changing the Background
In Snap!, it is possible to change the background to an image.

1. Open a new tab in Google Chrome, and go to [Google images](https://images.google.com/)
1. Find a suitable background image that is the proper size
    - The default size for a Snap! stage is 480x360
1. Right click the image, and save it to the desktop
1. Go back to Snap!, and in the **Sprites** area, click on the Stage
1. Click on the "Backgrounds" tab
1. Drag the new background image into the Backgrounds area!

## Animation with Costumes
In Snap!, it is possible to give **costumes** to sprites. Developers can create animations by switching a sprite's costumes quickly.

### Setting up the Costumes
1. In the top menu, click the File icon and select "Costumes..." from the list:  
    ![](https://i.imgur.com/qqLjmeH.png)
1. In the costume selection pop-up, scroll down and double click on "avery walking a", "avery walking b", "avery walking c", and "avery walking d":  
    ![](https://i.imgur.com/PgUSI4f.png)
1. Verify that each costume appears in the sprite's **Costumes** area:  
    ![](https://i.imgur.com/Y3zyQzT.png)

### Animating the Sprite
The costumes should change when the sprite is walking. This happens when either the right key OR the left key is pressed.

1. Drag over another ![](https://i.imgur.com/sUQuf19.png) block
1. Under the "When" block, drag over another ![](https://i.imgur.com/f0mf813.png) block
1. Within the "forever" block, drag a ![](https://i.imgur.com/N29G17D.png) block
1. From the _Operators_ section, drag a ![](https://i.imgur.com/ZfNwmLB.png) block into the **Scripts** area
    - This block allows developers to check if one thing or another are _true_
1. Drag a ![](https://i.imgur.com/MetLsie.png) block into the first space in the "or" block
1. Drag another ![](https://i.imgur.com/MetLsie.png) block into the second space in the "or" block
1. Set the dropdown for the "key pressed" blocks to be "left" and "right"
1. Within the "if" block, drag a ![](https://i.imgur.com/J2TuJpO.png) from the _Looks_ section
    - This will switch the costume of the sprite!
1. Test out the code and see the animation happen when moving the sprite left or right!

### Slower Animation Speed
Add a ![](https://i.imgur.com/7Hkpiyh.png) block under the "next costume" block so the costumes do not change constantly. Update the value in the "wait" block to change the animation speed.

## Final Snap! Code
![](https://i.imgur.com/IKqp8cu.png)

![](https://i.imgur.com/887dbhu.png)

![](https://i.imgur.com/Ncjsa3W.png)

![](https://i.imgur.com/wuGy8hi.png)

![](https://i.imgur.com/dauS4zN.png)

## Next Steps
- [Part 2 - Piskel Demo](Part2Piskel.md)
