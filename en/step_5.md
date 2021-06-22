## Add a predator

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Now you can add a predator that will be able to eat a few of the clones.
</div>
<div>
![a lion and a pterodactyl moving randomly in the scene and consuming bats](images/step_5.gif.png){:width="300px"}
</div>
</div>

You need to decide on the type of predator you want to choose, as this will decide the way it might move.

A land based predator might move randomly back and forth along the ground, but a flying predator might move randomly through the air.

--- task ---

Choose, upload or paint your predator sprite.

--- /task ---

--- task ---

Add scrolling to your predator sprite, so that it appears to move as the background moves. You can `change x by`{:class='block3'motion } values to change the predators speed 

```blocks3
when flag clicked
go to x: (0) y: (-80)
forever
if <(mouse x) > (200)> then
change x by (-3)
end
if <(mouse x) < (-200)> then
change x by (3)
end
```

--- /task ---


--- task ---

Animate your predator so that it moves randomly on the stage, in addition to the scrolling.

--- collapse ---
---
title: Animate a randomly flying sprite
---

The following blocks will cause a sprite to fly randomly around the stage. You can adjust the values to change the speed of the sprite.

```blocks3
when flag clicked
set rotation style [left-right v]
forever
point in direction (pick random (0) to (360))
repeat (10)
wait (0.1) seconds
next costume
move (20) steps
if on edge, bounce
```

--- /collapse ---

--- collapse ---
---
title: Animate a randomly walking sprite
---

The following blocks will make a sprite move randomly along the x axis (horizontally). You will need a variable to store if the sprite is moving left or right.

```blocks3
when flag clicked
set rotation style [left-right v]
forever
set [left-right v] to (pick random (-1) to (1))
if <(left-right) > (0)> then
point in direction (90)
else
point in direction (-90)
repeat (10)
wait (0.1) seconds
next costume
move (20) steps
if on edge, bounce
```

--- /collapse ---

--- /task ---

--- task ---

To finish off, you can make the clones disappear when they come into contact with the predator. If you chose to add a score variable, then maybe the score is reduced each time. If you chose to make the clones increase in size when they eat some food, then maybe they can be reduced in size.

```blocks3
when I start as a clone
forever
if <touching [predator v]> then
change [score v] by [-10] //choose this to reduce the score
change size by [-10] //choose this to reduce the size
delete this clone //choose this to remove the clone
```

--- /task ---
