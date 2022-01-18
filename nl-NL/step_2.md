## Toetsaanslagen

Hoeveel noten kun je met vier toetsen spelen? Het is misschien meer dan je denkt!

--- task ---

Open het 'Binaire held' Scratch startproject.

**Online** open het start project op [scratch.mit.edu/projects/550142911](https://scratch.mit.edu/projects/550142911){:target="_blank"}. Als je een Scratch account hebt, kun je klikken op **Remix** in de rechterbovenhoek om een kopie van het project op te slaan in je account.

**Offline:** open het [startproject](https://rpf.io/p/nl-NL/binary-hero-go){:target="_blank"} in de offline editor. Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

Begin met te laten zien welke toets wordt ingedrukt.

--- task ---

Klik op de sprite genaamd '1' en voeg code toe om het uiterlijk van de sprite te wijzigen als de toets `v` wordt ingedrukt.

![uiterlijk](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (aan v)
else
switch costume to (uit v)
end
```

Wanneer je je code test door op toets <kbd>v</kbd> drukken, zou de sprite moeten oplichten.

![De v toets testen](images/1-test.png)

--- /task ---

--- task ---

Doe hetzelfde voor de andere drie sprites zodat ze oplichten als de toetsen <kbd>z</kbd>, <kbd>x</kbd> of <kbd>c</kbd> worden ingedrukt.

![Alle toetsen ingedrukt](images/all-key-presses.png)

--- /task ---
