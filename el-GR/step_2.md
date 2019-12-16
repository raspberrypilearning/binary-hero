## Key presses

How many notes can you play with four keys? It might be more than you think!

\--- task \--- Open the 'Binary hero' Scratch starter project.

**Online:** άνοιξε το αρχικό έργο στο [rpf.io/binary-hero-on](http://rpf.io/binary-hero-on){:target="_blank"}. Αν διαθέτεις λογαριασμό Scratch, μπορείς να πατήσεις το **Remix** στην πάνω-δεξιά γωνία για να αποθηκεύσεις ένα αντίγραφο του έργου.

**Offline:** open the [starter project](http://rpf.io/p/en/binary-hero-go){:target="_blank"}in the offline editor. Αν χρειαστεί να κατεβάσεις και να εγκαταστήσεις τον offline editor για το Scratch, μπορείς να το βρεις στο [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}. \--- /task \---

Start by showing which key is being pressed.

\--- task \--- Click on the sprite called '1', and add code to change the sprite's costume if the `v` key is pressed.

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

When you test your code by pressing the <kbd>v</kbd> key, the sprite should light up.

![Testing the v key](images/1-test.png) \--- /task \---

\--- task \--- Do the same for the other three sprites so that they light up if the <kbd>z</kbd>, <kbd>x</kbd>, or <kbd>c</kbd> keys are pressed.

![All keys pressed](images/all-key-presses.png) \--- /task \---