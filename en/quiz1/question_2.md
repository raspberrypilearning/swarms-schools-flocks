
--- question ---

---
legend: Question 2 of 3
---

Which of the following blocks of code would make a clone continually move in a random direction over a random amount of time?

--- choices ---

- (x) 

```blocks3
when I start as a clone
forever
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```

  --- feedback ---
Yes, the time as well as the `x`{:class='block3motion'} and `y`{:class='block3motion'} positions are all chosen using a `pick random`{:class='block3operators'} block.
  --- /feedback ---

- ( ) 
```blocks3
when I start as a clone
forever
glide (3) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
No, the time is set to `3` seconds, although the `x`{:class='block3motion'} and `y`{:class='block3motion'} positions are chosen randomly
  --- /feedback ---

- ( ) 
```blocks3
when I start as a clone
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
No, this will cause the initial motion to be random, but will only happen once, and not `forever`{:class='block3control'}
  --- /feedback ---

- ( ) 
```blocks3
when I start as a clone
forever
glide (pick random (2) to (2)) secs to x: (pick random (40) to (40)) y: (pick random (40) to (40))
```
  --- feedback ---
No, although random blocks have been used, the start and end ranges of the `pick random`{:class='block3operators'} are the same, so only one number can be picked.
  --- /feedback ---

--- /choices ---

--- /question ---
