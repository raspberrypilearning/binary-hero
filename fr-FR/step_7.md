## Plus de blocs personnalisés

La nouvelle section de code est difficile à lire, donc tu vas utiliser plus de blocs personnalisés pour la rendre plus simple.

--- task ---

Fais un autre bloc appelé `effacer la chanson`{:class="block3myblocks"} qui supprime tous les éléments des deux listes. Utilise ce bloc avant d'ajouter des numéros dans les listes.

![note-sprite](images/note-sprite.png)

```blocks3
define effacer la chanson
delete all of [notes v]
delete all of [temps v]
```

Lorsque tu testes ton code, il devrait fonctionner comme avant.

```blocks3
define charger "joyeux anniversaire"
+effacer la chanson ::custom
add [1] to [notes v]
add [5] to [notes v]
```

--- /task ---

--- task ---

Pour que ton code soit encore plus facile à lire, fais un autre bloc qui te permet de spécifier une note à jouer et un temps pour jouer la note.

[[[generic-scratch3-make-block-parameters]]]

--- hints ---
 --- hint ---

Fais un bloc qui prend un numéro en tant que `note`{:class="block3variables"} et un numéro comme `temps`{:class="block3variables"} et `ajoute`{:class="block3variables"} chaque numéro à la liste correcte.

--- /hint --- --- hint ---

Voici à quoi ton code devrait ressembler :

```blocks3
define Ajouter note (note) at (temps :: variables) secs
add (note :: custom-arg) to [notes v]
add (temps :: custom-arg) to [temps v]

define charger "joyeux anniversaire"
effacer la chanson ::custom
+Ajouter note (1) at (5) secs
+Ajouter note (1) at (5.5) secs
+Ajouter note (3) at (6) secs
+Ajouter note (1) at (7) secs
+Ajouter note (6) at (8) secs
+Ajouter note (5) at (9) secs
```

--- /hint ------ /hints ---

--- /task ---