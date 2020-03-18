## Meer aangepaste blokken

Het nieuwste gedeelte van de code is moeilijk te lezen, dus je gaat meer aangepaste blokken gebruiken om het eenvoudiger te maken.

\--- task \---

Maak nog een blok met de naam `wis liedje`{:class="block3myblocks"} dat alle items uit beide lijsten verwijdert. Gebruik dit blok voordat je weer getallen toevoegt aan de lijsten.

![noten sprite](images/note-sprite.png)

```blocks3
definieer wis liedje
verwijder (alle v) of [noten v]
verwijder (alle v) of [tijden v]
```

Wanneer je de code test, zou deze net zo moeten werken als voorheen.

```blocks3
definieer laad 'happy birthday'
+ wis liedje ::custom
voeg [1] toe aan [noten v]
voeg [5] toe aan [noten v]
```

\--- /task \---

\--- task \---

Om ervoor te zorgen dat je code nog makkelijker te lezen is, maak je nog een blok waarmee je een te spelen noot kunt specificeren en een tijdstip om de noot te spelen.

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

Maak een blok met een getal als `noot`{:class="block3variables"} en een getal als `tijd`{:class="block3variables"} en `voeg`{:class="block3variables"} elk getal toe aan de juiste lijst.

\--- /hint \--- \--- hint \---

Dit is hoe je code eruit zou moeten zien:

```blocks3
definieer voeg noot (noot) toe op (tijd) sec.
voeg (noot :: custom-arg) toe aan [noten v]
voeg (tijd :: custom-arg) toe aan [tijden v]

definieer laad 'happy birthday'
wis liedje ::custom
+ Voeg noot (1) toe op (5) sec.
+ Voeg noot (1) toe op (5.5) sec.
+ Voeg noot (3) toe op (6) sec.
+ Voeg noot (1) toe op (7) sec.
+ Voeg noot (6) toe op (8) sec.
+ Voeg noot (5) toe op (9) sec.
```

\--- /hint \--- \--- /hints \---

\--- /task \---