
--- question ---

---
legend: Ερώτηση 2 από 3
---

Ποιο από τα παρακάτω μπλοκ κώδικα θα έκανε έναν κλώνο να κινείται συνεχώς σε τυχαία κατεύθυνση για ένα τυχαίο χρονικό διάστημα;

--- choices ---

- (x)

```blocks3
when I start as a clone
forever
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```

  --- feedback ---
Ναι, ο χρόνος καθώς και οι θέσεις `x`{:class='block3motion'} και `y`{:class='block3motion'} επιλέγονται χρησιμοποιώντας ένα μπλοκ `επίλεξε τυχαίο`{:class='block3operators'}.
--- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (3) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
Όχι, ο χρόνος έχει οριστεί σε `3` δευτερόλεπτα, παρόλο που οι θέσεις `x`{:class='block3motion'} και `y`{:class='block3motion'} επιλέγονται τυχαία
--- /feedback ---

- ( )
```blocks3
when I start as a clone
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
Όχι, αυτό θα προκαλέσει τυχαία αρχική κίνηση, αλλά θα συμβεί μόνο μία φορά και όχι `για πάντα`{:class='block3control'}
  --- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (pick random (2) to (2)) secs to x: (pick random (40) to (40)) y: (pick random (40) to (40))
```
  --- feedback ---
Όχι, αν και έχουν χρησιμοποιηθεί τυχαία μπλοκ, οι τιμές έναρξης και λήξης του `επίλεξε τυχαίο`{:class='block3operators'} είναι ίδιες, με συνέπεια να επιλέγεται μόνο ένας αριθμός.
--- /feedback ---

--- /choices ---

--- /question ---
