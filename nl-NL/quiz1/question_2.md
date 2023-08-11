
--- question ---

---
legend: Vraag 2 van 3
---

Welke van de volgende blokken code zouden een kloon voortdurend in een willekeurige richting laten bewegen over een willekeurige tijd?

--- choices ---

- (x)

```blocks3
wanneer ik als kloon start
herhaal
schuif in (willekeurig getal tussen (1) en (2)) sec. tot x: (willekeurig getal tussen (-40) en (40)) y: (willekeurig getal tussen (-40) en (40))
```

  --- feedback ---
Ja, zowel de tijd als `x`{:class='block3motion'} en `y`{:class='block3motion'} posities worden allemaal gekozen met behulp van een `willekeurig getal tussen`{:class='block3operators'} blok.
--- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (3) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
Nee, de tijd is ingesteld op `3` seconden, hoewel de `x`{:class='block3motion'} en `y`{:class='block3motion'} posities willekeurig worden gekozen
--- /feedback ---

- ( )
```blocks3
when I start as a clone
glide (pick random (1) to (2)) secs to x: (pick random (-40) to (40)) y: (pick random (-40) to (40))
```
  --- feedback ---
Nee, dit zorgt ervoor dat de initiële beweging willekeurig is, maar slechts één keer zal gebeuren, er ontbreekt een lus `herhaal`{:class='block3control'}
  --- /feedback ---

- ( )
```blocks3
when I start as a clone
forever
glide (pick random (2) to (2)) secs to x: (pick random (40) to (40)) y: (pick random (40) to (40))
```
  --- feedback ---
Nee, hoewel de juiste blokken zijn gebruikt, zijn de begin- en eindwaarden van het `willekeurig getal tussen`{:class='block3operators'} hetzelfde, dus er kan maar één nummer worden gekozen.
--- /feedback ---

--- /choices ---

--- /question ---
