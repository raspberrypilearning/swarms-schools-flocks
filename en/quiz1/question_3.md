
--- question ---

---
legend: Question 3 of 3
---
The following blocks are used on a **bee** sprite, to control what happens when the *bee** touches a **flower** sprite.

```blocks3
when I start as a clone
forever
if <touching [flower v]> then
create clone of [myself v]
end
```
Which of the following best describes what happens to the **bee**.

--- choices ---

- ( ) 

The **bee** clone is destroyed
  --- feedback ---
No, that would require a `delete this clone`{:class='block3events'} block.
  --- /feedback ---

- ( ) 

The **bee** clone will always move towards the flower.
  --- feedback ---
No, these blocks do not control any `motion`{:class='block3motion'}
  --- /feedback ---

- (x) 

When the **bee** clone touches the flower, it creates a clone of itself.

  --- feedback ---
Yes, clones can create clones of themselves.
  --- /feedback ---

- ( ) 

Then the **bee** sprite touches the flower, it creates a clone of itself. 
  --- feedback ---
No, these blocks only control the behavior of the clones, not the original sprite.
  --- /feedback ---

--- /choices ---

--- /question ---
