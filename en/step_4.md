## Feed your clones

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Now it's time to feed your animal clones; the player needs to guide them to a food source so they can collect it.
</div>
<div>
![Bats flying towards the mouse-pointer and collecting butterflies.](images/step_4.gif){:width="300px"}
</div>
</div>



--- task ---

Choose, upload, or draw a sprite to represent the food your animals will eat.

--- /task ---

--- task ---

Make the food appear on the screen. It could appear in a random position and at random times. It might move randomly around the screen. Maybe your animals' food does not move around, but it should scroll with the rest of the scenery.

--- collapse ---
---
title: Make a sprite appear in a random position for a random time
---

Adjust the `random`{:class='block3operators'} ranges to change how often the sprite disappears and reappears.

```blocks3
when flag clicked
forever
hide
wait (pick random (1) to (10)) seconds
show
go to (random position v)
wait (pick random (1) to (10)) seconds
```

--- /collapse ---

--- collapse ---
---
title: Move a sprite randomly around the screen
---

Adjust the `random`{:class='block3operators'} range to change how quickly the sprite moves around the screen.

```blocks3
when flag clicked
forever
glide (pick random (1) to (2)) secs to (random position v)
```

--- /collapse ---

--- collapse ---
---
title: Make sprites scroll with mouse motion
---

Add the following code to your sprite to make it scroll left and right as the mouse is moved to either side of the screen.

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

**Test**: You need to test your code to make sure the scrolling speed is not too fast or too slow. Also make sure that the sprite leaves and reenters the screen correctly, as the values will be different depending on the size of your sprite.

--- /collapse ---

--- /task ---

Now that your animals have something to eat, you can guide them with your mouse-pointer to their food. The question is, what should happen when they reach the food?

--- task ---

Add code so that your animals can eat their food. Eating the food should make it disappear; here are some ideas for what happens next and how it could help your animals.

1. Generate more clones
1. Increase the size of your clones
1. Increase a score

--- collapse ---
---
title: Eat the food
---

A small addition to your code will make the food disappear when it is touched by a clone.

On your **animal** sprite, add blocks so that when a clone touches the **food** sprite, it broadcasts a message.

```blocks3
when I start as a clone
forever
if <touching [animal v]> then
broadcast (eaten v)
end
```

Then, on the **food** sprite, hide it when it receives the broadcast.

```blocks3
when I receive [eaten v]
hide
```

--- /collapse ---

--- collapse ---
---
title: Grow a clone, make a new clone, or increase a score
---

This code will allow the clones to increase in size each time they eat some food.

```blocks3
when I start as a clone
forever
if <touching [animal v]> then
broadcast (eaten v)
change size by (20)
end
```

This will generate a new clone each time they eat some food.

```blocks3
when I start as a clone
forever
if <touching [animal v]> then
broadcast (eaten v)
create clone of [myself v]
end
```

This will increase a score when some food has been eaten.

```blocks3
when flag clicked
set [score v] to (0)

when I start as a clone
forever
if <touching [animal v]> then
broadcast (eaten v)
change [score v] by (10)
end
```
--- /collapse ---

--- /task ---

