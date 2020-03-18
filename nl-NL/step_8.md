## Houd een score bij

Verbeter je spel door de speler punten te geven voor het spelen van de juiste noot.

\--- task \---

Maak een nieuwe variabele met de naam `score`{:class="block3variables"} en zet deze boven in je speelveld.

![Een score toevoegen](images/add-score.png)

\--- /task \---

\--- task \---

Tel bij `score`{:class="block3variables"} op wanneer de speler de juiste noot op het juiste tijdstip speelt. Vergeet niet om `score`{:class="block3variables"} in te stellen op `0`{:class="block3variables"} aan het begin van het spel.

\--- hints \--- \--- hint \---

`Voordat elke kloon wordt verwijderd`{:class="block3control"}, moet deze controleren dat `als`{:class="block3control"} de `noot`{:class="block3variables"} `gelijk is aan`{:class="block3operators"} het `uiterlijk nummer`{:class="block3looks"}, dan moet de score `gewijzigd`{:class="block3variables"} worden.

\--- /hint \--- \--- hint \---

Dit zijn de codeblokken die je nodig hebt:

![noot](images/note-sprite.png)

```blocks3
[] = []
(uiterlijk [nummer v])
(noot)
verander [score v] met (1)

als <> dan
anders
einde
```

\--- /hint \--- \--- hint \---

Dit is hoe je code eruit zou moeten zien:

![noot](images/note-sprite.png)

```blocks3
wanneer ik begin als kloon
ga naar x: (20) y: (160)
verschijn
schuif in (2) sec. naar x: (20) y: (- 130)
+ als <(noot :: variables) = (uiterlijk [nummer v])> dan
verander [score v] met (1)
einde
verwijder deze kloon
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Verzend een signaal met de naam 'correct' wanneer de juiste noot wordt gespeeld.

![noot](images/note-sprite.png)

```blocks3
wanneer ik begin als kloon
ga naar x: (20) y: (160)
verschijn
schuif in (2) sec. naar x: (20) y: (- 130)
als <(noot :: variables) = (uiterlijk [nummer v])> dan
verander [score v] met (1)
+ zend signaal (correct v)
einde
verwijder deze kloon
```

\--- /task \---

\--- task \---

![Juiste achtergrond speelveld](images/correct-costume.png)

Voeg code toe aan je speelveld om de achtergrond kort te veranderen wanneer de speler de juiste noot speelt. Het project bevat hiervoor al een tweede achtergrond.

![speelveld](images/stage.png)

```blocks3
wanneer op de groene vlag wordt geklikt
verander achtergrond naar (normal v)

wanneer ik signaal [correct v] ontvang
verander achtergrond naar (correct v)
wacht (0.3) sec.
verander achtergrond naar (normal v)
```

\--- /task \---