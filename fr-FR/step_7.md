## Plus de blocs personnalisés

La nouvelle section de code est difficile à lire, donc tu vas utiliser plus de blocs personnalisés pour la rendre plus simple.

\--- task \---

Fais un autre bloc appelé `effacer la chanson`{:class="block3myblocks"} qui supprime tous les éléments des deux listes. Utilise ce bloc avant d'ajouter des numéros dans les listes.

![note-sprite](images/note-sprite.png)

```blocks3
define clear song
delete (all v) of [notes v]
delete (all v) of [times v]
```

Lorsque tu testes ton code, il devrait fonctionner comme avant.

```blocks3
define load 'happy birthday'
+clear song ::custom
add [1] to [notes v]
add [5] to [notes v]
```

\--- /task \---

\--- task \---

Pour que ton code soit encore plus facile à lire, fais un autre bloc qui te permet de spécifier une note à jouer et un temps pour jouer la note.

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

Fais un bloc qui prend un numéro en tant que `note`{:class="block3variables"} et un numéro comme `temps`{:class="block3variables"} et `ajoute`{:class="block3variables"} chaque numéro à la liste correcte.

\--- /hint \--- \--- hint \---

Voici à quoi ton code devrait ressembler :

```blocks3
define Add note (note) at (time) secs
add (note :: custom-arg) to [notes v]
add (time :: custom-arg) to [times v]

define load 'happy birthday'
clear song ::custom
+Add note (1) at (5) secs
+Add note (1) at (5.5) secs
+Add note (3) at (6) secs
+Add note (1) at (7) secs
+Add note (6) at (8) secs
+Add note (5) at (9) secs
```

\--- /hint \--- \--- /hints \---

\--- /task \---