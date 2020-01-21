## Więcej niestandardowych bloków

Najnowsza sekcja kodu jest trudna do odczytania, więc będziesz używać więcej niestandardowych bloków, aby uprościć.

\--- task \---

Make another block called `clear song`{:class="block3myblocks"} that deletes all items from both lists. Use this block before adding numbers back intothe lists.

![note-sprite](images/note-sprite.png)

```blocks3
zdefiniuj czysty utwór
usuń (wszystkie v) z [uwagi v]
usuń (wszystkie v) z [razy v]
```

When you test your code, it should work just as it did before.

```blocks3
zdefiniuj ładowanie „wszystkiego najlepszego”
+ wyczyść piosenkę :: niestandardowe
dodaj [1] do [notatek v]
dodaj [5] do [notatek v]
```

\--- /task \---

\--- task \---

So that your code is even easier to read, make another block that allows you to specify a note to be played and a time to play the note at.

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

Make a block that takes a number as `note`{:class="block3variables"} and a number as `time`{:class="block3variables"} and `adds`{:class="block3variables"} each number to the correct list.

\--- /hint \--- \--- hint \---

This is what your code should look like:

```blocks3
zdefiniuj Dodaj notatkę (uwaga) w (czasie) sek.
dodaj (uwaga :: custom-arg) do [notatek v]
dodaj (czas :: niestandardowy-argument) do [czasów v]

zdefiniuj ładunek „wszystkiego najlepszego”
wyczyść piosenka :: niestandardowe
+ Dodaj notatkę (1) w (5) sek.
+ Dodaj notatkę (1) w (5.5) sek.
+ Dodaj notatkę (3) w (6) sek.
+ Dodaj notatkę (1) w (7) ) sek.
+ Dodaj notatkę (6) o (8) sek.
+ Dodaj notatkę (5) o (9) sek.
```

\--- /hint \--- \--- /hints \---

\--- /task \---