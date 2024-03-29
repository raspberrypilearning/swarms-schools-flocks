## Create your scrolling scene

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Create a new scene and then have it scroll with the mouse motion.
</div>
<div>
![Animation showing background and foreground sprites scrolling.](images/sprite-background-scroll.gif){:width="300px"}
</div>
</div>
 
 --- task ---

Open a [new Scratch project](https://rpf.io/scratch-new){:target="_blank"}. Scratch will open in another browser tab.

[[[working-offline]]]

--- /task ---

Think about what type of scene you will create. You can choose a few sprites now, to give yourself some inspiration. Then choose a backdrop that you think will fit the scene you are imagining.

--- task ---

Choose a fitting backdrop for your scene, one that matches the environment where your animals would live.

[[[generic-scratch3-backdrop-from-library]]]

--- /task ---

You want it so that moving the mouse will allow scrolling behaviour in your game. You can either make the foreground sprites move, or you can turn the backdrop into a sprite and have this move.

--- task ---

Either add additional sprites to your scene, which scroll when the mouse is moved, or convert your backdrop into a sprite and have this scroll when the mouse moves.

--- collapse ---
---
title: Convert a backdrop and make it scroll
---

![A backdrop converted to a sprite and scrolling left and right with the mouse-pointer.](images/scroll-background.gif)

In the **Backdrops** paint editor, select the entire backdrop and then use the **Copy** menu item to copy the entire backdrop.

![The backdrop has been selected and the 'Copy' menu item is shown in the top left.](images/copy-backdrop.png)

Paint a new sprite and paste the backdrop scene into the new sprite so it becomes one of the costumes.

![Paint sprite selected from the 'Create New Sprite' menu.](images/paint-sprite.png)

To add scrolling behaviour to your new sprite, you can use the following scripts. You will need some way to say whether the sprite is moving left or right. In the example, a broadcast is used, but this could be mouse position or key/button presses.

```blocks3
when I receive [left v]
change x by (3)

when I receive [right v]
change x by (-3)

when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
create clone of [myself v]
change x by (460) 
broadcast [scroll v]

when I receive [scroll v]
forever
if <(x position) > (460)> then
set x to (-460)
end
if <(x position) < (-460)> then
set x to (460)
end
```

--- /collapse ---

--- collapse ---
---
title: Make sprites scroll with mouse motion
---

![Animation showing a tree scrolling as the mouse is moved.](images/sprite-scroll.gif)

Add the following code to your foreground sprite to make it scroll left and right as the mouse is moved to either side of the screen. You can adjust the numbers to your liking.

```blocks3
when flag clicked
go to x: (0) y: (-80)
forever
if <(mouse x) > (200)> then
change x by (-10)
end
if <(mouse x) < (-200)> then
change x by (10)
end
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
```

--- /collapse ---

--- /task ---

If you like, you can combine the two techniques.

![Animation showing background and foreground sprites scrolling.](images/sprite-background-scroll.gif)


--- save ---
