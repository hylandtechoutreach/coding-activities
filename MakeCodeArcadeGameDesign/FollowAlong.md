# Follow-Along: Retro Platformer
Learn about MakeCode Arcade and add some code to start building a platformer game!

## MakeCode Arcade Introduction
Play through the [jumpy platformer](https://arcade.makecode.com/71044-22408-12308-23475) for an idea of what is possible with MakeCode Arcade. This editor uses block-based code (or JavaScript) to create retro games. The games can even be ported to physical devices. It may take a long time to build something like the jumpy platformer, but getting started with a simple platformer is not as difficult!

Go to [arcade.makecode.com/#editor](https://arcade.makecode.com/#editor) to start working on a new MakeCode Arcade project. The editor looks like this:

![](Assets/MakeCodeEditor.png)

### Page Sections
- **Game Preview:** This pane on the left is where the developer can test out the game.
- **Block Selection:** This pane in the middle is where the blocks live. They can be dragged to the **Code** section to create the program.
- **Code:** This pane on the right is where the code for the program lives. Drag blocks from the **Block Selection** section into this section to create code.

## Setting a Background Color
For the first block of the game, set the background color.

1. In the **Block Selection** section, click on "Scene" and find the `set background color to` block  
    ![](Assets/SetBgColorTo.png)
1. Click on the `set background color to` block, and drag it into the `on start` block  
    ![](Assets/BlockSnap.png)
1. Click on the blank spot in the background color block, and select a color for the background  
    ![](Assets/SelectBgColor.png)
1. The game preview should automatically update, and the background should be the proper color!

## Creating the Main Character
The first thing the game needs is a main character for the player to control!

1. In the **Block Selection** section, in the "Sprites" category, click and drag the red `set mySprite to` block under the background color block  
    ![](Assets/SetMySprite.png)
1. In the `set mySprite to` block, click the drop-down arrow on `mySprite`, and click "Rename variable..."  
    ![](Assets/RenameVar.png)
1. Set the variable name to "Main Character"
    - _Note: If the main character has a name, this could be their name instead! Just make sure to use the name when referencing the `Main Character` sprite_
1. Click on the blank space next to "sprite" in the `set sprite` block to open the Sprite Editor  
    ![](Assets/SpriteDrawSpace.png)
1. Draw a sprite image for the main character, and then click the green "Done" button in the bottom right
1. The game preview should automatically update, and the main character sprite should appear!

### _Side-Note: Variables_
In computer science, **variables** are containers for data. In MakeCode Arcade, variables can hold things like sprites, images, hit points, the player's score... almost anything!

## Moving the Main Character
The main character should be able to move left and right, as in any other platformer.

1. From the "Controller" category, click and drag a red `move mySprite with buttons +` block under the `set sprite` block  
    ![](Assets/MoveMySprite.png)
1. In the `move` block, click the drop-down arrow on `mySprite`, and select `Main Character`
1. In the game preview, notice that it is possible to move left and right, but also up and down
1. To prevent the main character from moving up and down, click the `+` in the `move` block, and set the `vy` to `0`
    - This sets the _vertical speed_ of the main character sprite to `0`
1. Test out the game in the game preview again, and verify that the main character only moves left and right!

### _Side-Note: The Cartesian Plane - Up, Down, Left, Right_
The MakeCode Arcade screen is a lot like a Cartesian plane. The **x** axis moves left and right (horizontally), and the **y** axis moves up and down.

## Creating a Game Map
Now the main character can move, but they won't have much to do without a map!

1. In the "Scene" category, under the "Tiles" header, click and drag a `set tilemap to` block to right under the `set background color` block  
    ![](Assets/SetTilemap.png)
1. Click the blank spot in the `set tilemap to` block to open the Tilemap Editor

![](Assets/TilemapEditor.png)

1. In the bottom left, set the **Map Size** to `16`x`8`
    - Zoom out if necessary using the magnifying glass icons in the bottom right
1. In the **Tile Selector** section, select a tile for the ground
1. In the **Current Map** section, draw ground covering the bottom part of the map  
    ![](Assets/CurrentMap.png)
1. Select the **Wall Editor** tool  
    ![](Assets/WallEditor.png)
1. Draw over the ground with the wall editor - this will make the ground stop the main character from falling  
    ![](Assets/DrawGroundWall.png)
1. Click the "Done" button, and see the map appear in the game preview!

## Adding Gravity
Now that the main character has somewhere to land, add gravity to the game!

1. In the "Sprites" category, click and drag a `set mySprite x to 0` block under the existing blocks in `on start`  
  ![](Assets/SpriteX.png)
1. Click the drop-down arrow next to `mySprite` and select `Main Character`
1. Click the drop-down arrow next to `x` and select `ay (acceleration y)`
1. Change the `0` to `400`
    - This will make the main character accelerate downward (fall)
1. Notice that in the updated game preview, the main character can move to the right off the screen - the camera does not follow the sprite
1. In the "Scene" category, scroll down to find a `camera follow sprite` block, and click and drag it under the existing blocks in `on start`
1. Click the drop-down arrow next to `mySprite` and select `Main Character`
1. Play the game in the game preview and verify that the main character falls, and the camera follows them!

## Making the Main Character Jump
In almost every platformer, the main character has the ability to jump.

1. In the "Controller" category, click and drag an `on A button pressed` into the **Code** section
1. Click the drop-down arrow next to `A` and select `up`  
    ![](Assets/UpPressed.png)
1. In the "Sprites" category, click and drag a `set mySprite x to 0` block into the `on up button pressed` block
1. Click the drop-down arrow next to `mySprite` and select `Main Character`
1. Click the drop-down arrow next to `x` and select `vy (velocity y)`
1. Change the `0` to `-200`
    - This will make the main character start moving upward (jump)
1. In the game preview, notice that the main character can jump multiple times, which should not be possible

### Single Jump
The main character should only be able to jump when they are on the ground.

1. In the "Logic" category, click and drag an `if true then` block into the `on up button pressed` block
1. In the "Scene" category, scroll down to "Collisions" and click and drag an `is mySprite hitting wall left` into the `true` in the `if` block
1. Click the drop-down arrow next to `mySprite` and select `Main Character`
1. Click the drop-down arrow next to `left` and select `bottom`
1. Click and drag the `set Main Character vy to -200` block into the `if` block
1. Play the game preview and verify that the main character can only jump when they are on the ground!

![](Assets/OnUpIfGround.png)

### _Side-Note: Conditionals_
In computer science, **conditionals** let the program do different things depending on the current situation. In this example, the main character can only jump _if_ they are on the ground. Conditionals are incredibly useful for creating dynamic programs!

## Winning the Game
For this to be an actual game, there should be a way to win!

1. Find the `set tilemap to` block, and click on the tilemap to open the Tilemap Editor  
    ![](Assets/EditTilemap.png)
1. In the Tile Selector section on the left, find a good tile for the winning tile
    - The player will win the game if the main character overlaps with this tile
1. Select the tile, and select the pencil tool  
    ![](Assets/NewTile.png)
1. Place the winning object tile somewhere on the tilemap
1. Click the green "Done" button in the lower right to exit the Tilemap Editor
1. Back in the code, in the "Scene" category, scroll down to Tiles and find the `on sprite of kind Player overlaps at location` block
1. Click and drag the `overlaps` block to a blank spot in the **Code** section
1. Click the drop-down arrow next to `overlaps` and select the winning object tile
1. In the "Game" category, click and drag a `game over` block into the `overlaps` block
1. Click the `LOSE` switch to flip it to `WIN`
1. Play the game in the game preview to verify that reaching the winning object will win the game!

![](Assets/GameOverWin.png)

## Losing the Game
The game will not be very interesting if there is no way to lose. Add an obstacle that will end the game for the player.

1. Find the `set tilemap to` block, and click on the tilemap to open the Tilemap Editor
1. In the Tile Selector section on the left, click on "My Tiles"  
    ![](Assets/MyTiles.png)
1. Click the "+" to create a new tile for an obstacle  
    ![](Assets/CreateNewTile.png)
1. In the Tile Editor, draw an obstacle that will end the game (e.g. spikes, fire, an enemy)
1. Place the obstacle tile in several places on the tilemap
1. Click the green "Done" button in the lower right to exit the Tilemap Editor
1. Back in the code, in the "Scene" category, click and drag another `overlaps` block into the **Code** section
1. Click the drop-down arrow next to `overlaps` and select the obstacle tile
1. In the "Game" category, click and drag a `game over` block into the new `overlaps` block
1. Click the `+` on the `game over` block to reveal additional options
1. Click the drop-down arrow next to `confetti` and select a new game-ending animation (like `melt`)
1. Play the game in the game preview to verify that touching an obstacle will lose the game!

![](Assets/OnLose.png)

## Code
At this point, the project should be done! It should look something like [this](https://makecode.com/_b6V3sP1w5DgL):

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://arcade.makecode.com/#pub:_aLv4XqPHXPT5" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>
