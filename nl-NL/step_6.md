## Bewaar je liedje

Op dit moment worden noten uit de lijsten verwijderd nadat ze zijn gespeeld, dus je hebt nog lege lijsten over:

![Lege lijsten](images/empty-lists.png)

Je gaat nu code toevoegen om liedjes in je project op te slaan, zodat je niet elke keer aan je lijsten hoeft toe te voegen.

![Voeg noten en tijden toe aan lijsten](images/lists-add-annotated.png)

--- task ---

Maak een nieuw blok met de naam `laad 'happy birthday'`{:class="block3myblocks"} dat zowel de `noten`{:class="block3variables"} als `tijden`{:class="block3variables"} lijsten wist, en voegt vervolgens de juiste getallen toe aan beide lijsten. 

[[[generic-scratch3-make-block]]]

--- hints ---
 --- hint ---

Het `laad 'happy birthday'`{:class="block3myblocks"} blok moet `alle`{:class="block3variables"} items verwijderen uit zowel de `noten`{:class="block3variables"} als de `tijden`{:class="block3variables"} lijsten en vervolgens de juiste zes nummers aan de lijst `toevoegen`{:class="block3variables"} waar ze in horen, in de juiste volgorde.

--- /hint --- --- hint ---

Dit zijn de codeblokken die je nodig hebt:

![noten sprite](images/note-sprite.png)

```blocks3
verwijder (alle v) van [noten v]

definieer laad 'happy birthday'

voeg [1] toe aan [noten v]

verwijder (alle v) van [tijden v]
```

--- /hint --- --- hint ---

Dit is hoe je code eruit zou moeten zien:

![noten sprite](images/note-sprite.png)

```blocks3
definieer laad 'happy birthday'
verwijder (alle v) van [noten v]
verwijder (alle v) van [tijden v]
voeg [1] toe aan [noten v]
voeg [5] toe aan [tijden v]
voeg [1] toe aan [noten v]
voeg [5.5] toe aan [tijden v]
voeg [3] toe aan [noten v]
voeg [6] toe aan [tijden v]
voeg [1] toe aan [noten v]
voeg [7] toe aan [tijden v]
voeg [6] toe aan [noten v]
voeg [8] toe aan [tijden v]
voeg [5] toe aan [noten v]
voeg [9] toe aan [tijden v]
```

--- /hint ------ /hints --- --- /task ---

--- task ---

Test je nieuwe blok door het aan het begin van je project uit te voeren.

![noten sprite](images/note-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
+ laad 'happy birthday' ::custom
verdwijn
zet klok op 0
```

Elk van je lijsten zou nu zes nummers moeten bevatten.

![Lijsten met noten en tijden](images/lists-add.png)

--- /task ---