
--- question ---

---
legend: Question 3 sur 3
---
Les blocs suivants sont utilisés sur un sprite **abeille**, pour contrôler ce qui se passe lorsque l'**abeille** touche un sprite  **fleurs**.

```blocks3
quand je commence comme un clone
répéter indéfiniment
si <touching [fleur v]> alors
créer un clone de [moi-même v]
fin
```
Lequel des énoncés suivants décrit le mieux ce qui arrive à **l'abeille**.

--- choices ---

- ( )

Le clone **abeille** est détruit
--- feedback ---
Non, cela nécessiterait un bloc `supprimer ce clone`{:class='block3events'}.
--- /feedback ---

- ( )

Le clone **abeille** se dirigera toujours vers la fleur.
--- feedback ---
Non, ces blocs ne contrôlent aucun `mouvement`{:class='block3motion'}
  --- /feedback ---

- (x)

Lorsque le clone **abeille** touche la fleur, il crée un clone de lui-même.

  --- feedback ---
Oui, les clones peuvent créer des clones d'eux-mêmes.
--- /feedback ---

- ( )

Puis le sprite **abeille** touche la fleur, il crée un clone de lui-même.
--- feedback ---
Non, ces blocs ne contrôlent que le comportement des clones, pas le sprite original.
--- /feedback ---

--- /choices ---

--- /question ---
