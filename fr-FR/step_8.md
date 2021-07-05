## Garder un score

Améliore ton jeu en donnant aux joueurs des points à chaque bonne note jouée.

\--- task \---

Crée une nouvelle variable appelée `score`{:class="block3variables"}, et place-la en haut de ta scène.

![Ajouter un score](images/add-score.png)

\--- /task \---

\--- task \---

Ajoute au `score`{:class="block3variables"} chaque fois que le joueur joue la bonne note au bon moment. N'oublie pas de définir le `score`{:class="block3variables"} à `0`{:class="block3variables"} au début du jeu.

\--- hints \--- \--- hint \---

`Avant que chaque clone soit supprimé`{:class="block3control"}, il devrait vérifier pour voir `si`{:class="block3control"} la `note`{:class="block3variables"} est `égale au`{:class="block3operators"} `numéro de costume`{:class="block3looks"}, et dans ce cas, le score devrait être `modifié`{:class="block3variables"}.

\--- /hint \--- \--- hint \---

Voici les blocs de code dont tu as besoin :

![note](images/note-sprite.png)

```blocks3
[ ] = [ ]
(costume [number v])
(note)
change [score v] by (1)

if <> then
else
end
```

\--- /hint \--- \--- hint \---

Voici à quoi ton code devrait ressembler:

![note](images/note-sprite.png)

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
+if <(note :: variables) = (costume [number v])> then
change [score v] by (1)
end
delete this clone
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Diffuse un message appelé « correct » lorsque la bonne note est jouée.

![note](images/note-sprite.png)

```blocks3
when I start as a clone
go to x: (20) y: (160)
show
glide (2) secs to x: (20) y:(-130)
if <(note :: variables) = (costume [number v])> then
change [score v] by (1)
+broadcast (correct v)
end
delete this clone
```

\--- /task \---

\--- task \---

![Arrière-plan de la bonne scène](images/correct-costume.png)

Ajoute du code à ta scène pour changer brièvement l'arrière-plan lorsque le joueur joue la bonne note. Le projet contient déjà un deuxième arrière-plan pour cela.

![scène](images/stage.png)

```blocks3
when flag clicked
switch backdrop to (normal v)

when I receive [correct v]
switch backdrop to (correct v)
wait (0.3) seconds
switch backdrop to (normal v)
```

\--- /task \---