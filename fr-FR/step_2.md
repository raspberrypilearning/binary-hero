## Touches pressées

Combien de notes peux-tu jouer avec quatre touches ? Cela pourrait être plus que tu ne le penses !

\--- task \---

Ouvre le projet de démarrage Scratch « Virtuose du binaire ».

**Online:** open the starter project at [rpf.io/binary-hero-on](https://rpf.io/binary-hero-on){:target="_blank"}. Si tu as un compte Scratch, tu peux cliquer sur **Remix** dans le coin supérieur droit pour enregistrer une copie du projet.

**Offline:** open the [starter project](https://rpf.io/p/en/binary-hero-go){:target="_blank"}in the offline editor. If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

Commence par montrer quelle touche est pressée.

\--- task \---

Clique sur le sprite appelé "1", et ajoute du code pour changer le costume du sprite si la touche `v` est pressée.

![costume](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
else
switch costume to (off v)
end
```

Lorsque tu testes ton code en appuyant sur la touche <kbd>v</kbd> , le sprite devrait s'allumer.

![Test de la touche v](images/1-test.png)

\--- /task \---

\--- task \---

Fais la même chose pour les trois autres sprites afin qu'ils s'allument si les touches <kbd>z</kbd>, <kbd>x</kbd>, ou <kbd>c</kbd> sont pressées.

![Toutes les touches sont pressées](images/all-key-presses.png)

\--- /task \---