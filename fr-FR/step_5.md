## Ajouter un prédateur

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Maintenant tu peux ajouter un prédateur qui pourra manger quelques clones.
</div>
<div>
![Animation d'un lion et d'un ptérodactyle se déplaçant aléatoirement dans une scène avec des chauves-souris volant au-dessus d'eux](images/step_5.gif){:width="300px"}
</div>
</div>

Tu dois décider du type de prédateur que tu veux choisir, car cela peut affecter la façon dont il se déplacera.

Un prédateur terrestre peut se déplacer au hasard d'avant en arrière sur le sol, mais un prédateur volant peut se déplacer au hasard dans les airs.

--- task ---

Choisis, télécharge ou peins ton sprite **prédateur**.

--- /task ---

--- task ---

Ajoute un défilement à ton sprite **prédateur**, pour qu'il semble bouger lorsque l'arrière-plan se déplace. Tu peux mettre les valeurs `de x à`{:class='block3motion'} pour changer la vitesse du prédateur.

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

Anime ton prédateur pour qu'il se déplace aléatoirement sur la scène, en plus du défilement.

--- collapse ---
---
title: Animer un sprite volant au hasard
---

Les blocs suivants feront voler un sprite au hasard autour de la scène. Tu peux ajuster les valeurs pour modifier la vitesse du sprite.

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
title: Animer un sprite marchant de manière aléatoire
---

Les blocs suivants feront bouger un sprite de manière aléatoire le long de l'axe x (horizontalement). Tu auras besoin d'une variable pour stocker si le sprite se déplace vers la gauche ou la droite.

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

Pour finir, tu peux faire disparaître les clones lorsqu'ils entrent en contact avec le prédateur. Si tu as choisi d'ajouter une variable de score, le score sera peut-être réduit à chaque fois. Si tu as choisi de faire augmenter la taille des clones quand ils mangent de la nourriture, ils peuvent peut-être être réduits en taille.

```blocks3
when I start as a clone
forever
if <touching [predator v]> then
change [score v] by [-10] //Choisis ceci pour réduire le score
change size by [-10] //Choisis ceci pour réduire la taille
delete this clone //Choisis ceci pour supprimer le clone
```

--- /task ---

