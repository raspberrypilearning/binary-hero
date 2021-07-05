## Jouer des notes

Jouer des notes lorsque les touches sont pressées.

--- task ---

Ajoute l'extension « Musique » à ton projet.

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Diffuser un message de changement de note chaque fois que **l'une des quatre touches** est pressée.

![sprite 1](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (allumé v)
+broadcast (changer de note v)
else
switch costume to (éteint v)
end
```

--- /task ---

--- task ---

Ajoute du code à la scène pour jouer une note lorsqu'une combinaison de touches est pressée.

Tes notes devraient commencer au C moyen, ce qui est la note 60.

```blocks3
play note (60) for (1) beats
```

--- hints ---
 --- hint ---

![1 sprite](images/stage.png)

Lorsque ta scène `reçoit`{:class="block3events"} la diffusion "changer de note", il devrait `arrêter tous les sons`{:class="block3sound"} avant de `jouer une note`{:class="block3sound"} en fonction de la valeur de la variable `note`{:class="block3variables"}.

+ Lorsque la variable `note`{:class="block3variables"} est `1`{:class="block3variables"}, la note 60 devrait jouer
+ Lorsque la variable `note`{:class="block3variables"} est `2`{:class="block3variables"}, la note 61 devrait jouer
+ Lorsque la variable `note`{:class="block3variables"} est `3`{:class="block3variables"}, la note 62 devrait jouer
+ etc...

--- /hint --- --- hint ---

Voici les blocs de code dont tu as besoin :

![scène](images/stage.png)

```blocks3
play note (60) for (1) beats
when I receive [changer de note v]
() + ()
(note)
stop all sounds
```

--- /hint --- --- hint ---

Voici à quoi ton code devrait ressembler :

![scène](images/stage.png)

```blocks3
when I receive [changer de note v]
stop all sounds
play note ((59) + (note :: variables)) for (1) beats
```

--- /hint ------ /hints --- --- /task ---

--- task ---

Teste ton code. Entends-tu qu'une note est répétée lorsque tu maintiens une touche enfoncée ?

--- no-print ---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Ton navigateur ne supporte pas la vidéo HTML5.
</video>

--- /no-print ---

--- /task ---

--- task ---

Ajoute du code pour que **tous** les sprites de touche ne jouent une note **qu'une fois** quand une touche est enfoncée.

![1 sprite](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (allumé v)
broadcast (changer de note v)
+wait until <not <key (v v) pressed?>
else
switch costume to (éteint v)
end
```

--- /task ---