## Touches pressées

Combien de notes peux-tu jouer avec quatre touches ? Cela pourrait être plus que tu ne le penses !

--- task ---

Ouvre le projet de démarrage Scratch « Virtuose du binaire ».

**En ligne :** ouvre le projet de démarrage sur [scratch.mit.edu/projects/550776893](https://scratch.mit.edu/projects/550776893){:target="_blank"}. Si tu as un compte Scratch, tu peux cliquer sur **Remix** dans le coin supérieur droit pour enregistrer une copie du projet.

**Hors ligne :** ouvre le [projet de démarrage](http://rpf.io/p/fr-FR/binary-hero-go){:target="_blank"} de l'éditeur hors ligne. Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver sur [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

Commence par montrer quelle touche est pressée.

--- task ---

Clique sur le sprite appelé "1", et ajoute du code pour changer le costume du sprite si la touche `v` est pressée.

![costume](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (allumé v)
else
switch costume to (éteint v)
end
```

Lorsque tu testes ton code en appuyant sur la touche <kbd>v</kbd> , le sprite devrait s'allumer.

![Test de la touche v](images/1-test.png)

--- /task ---

--- task ---

Fais la même chose pour les trois autres sprites afin qu'ils s'allument si les touches <kbd>z</kbd>, <kbd>x</kbd>, ou <kbd>c</kbd> sont pressées.

![Toutes les touches sont pressées](images/all-key-presses.png)

--- /task ---