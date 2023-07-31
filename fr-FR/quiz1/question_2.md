
--- question ---

---
legend: Question 2 sur 3
---

Lequel des blocs de code suivants ferait en sorte qu'un clone se déplace continuellement dans une direction aléatoire pendant une durée aléatoire ?

--- choices ---

- (x)

```blocks3
quand je commence comme un clone
répéter indéfiniment
glisser en (nombre aléatoire entre (1) et (2)) secondes à x: (nombre aléatoire entre (-40) et (40)) y: (nombre aléatoire entre (-40) et (40))
```

  --- feedback --- Oui, le temps ainsi que les positions `x`{:class='block3motion'} et `y`{:class='block3motion'} sont tous choisis à l'aide d'un bloc `nombre aléatoire`{:class='block3operators'}. --- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (3) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback --- Non, le temps est réglé sur `3` secondes, bien que les positions `x`{:class='block3motion'} et `y`{:class='block3motion'} soient choisies au hasard --- /feedback ---

- ( )
```blocks3
when I start as a clone
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback --- Non, cela rendra le mouvement initial aléatoire, mais ne se produira qu'une seule fois, et non `répéter indéfiniment`{:class='block3control'}
  --- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (pick random (2) to (2)) secs to x: (pick random (40) to (40)) y: (pick random (40) to (40))
```
  --- feedback --- Non, bien que des blocs aléatoires aient été utilisés, les plages de début et de fin du `nombre aléatoire`{:class='block3operators'} sont les mêmes, donc un seul nombre peut être choisi. --- /feedback ---

--- /choices ---

--- /question ---
