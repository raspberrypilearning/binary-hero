## Bewaar je liedje

Op dit moment worden noten uit de lijsten verwijderd nadat ze zijn gespeeld, je lijsten zijn nu dus leeg:

![Lege lijsten](images/empty-lists.png)

Je gaat nu code toevoegen om liedjes in je project op te slaan, zodat je niet elke keer de lijsten hoeft te vullen.

![Voeg noten en tijden toe aan lijsten](images/lists-add-annotated.png)

\--- task \---

Make a new block called `load 'happy birthday'`{:class="block3myblocks"} that clears both the `notes`{:class="block3variables"} and `times`{:class="block3variables"} lists, and then adds the correct numbers back into both lists.

[[[generic-scratch3-make-block]]]

\--- hints \--- \--- hint \---

The `load 'happy birthday'`{:class="block3myblocks"} block should `delete all`{:class="block3variables"} items from both the `notes`{:class="block3variables"} and `times`{:class="block3variables"} lists and then `add`{:class="block3variables"} the correct six numbers to the list they belong in, in the correct order.

\--- /hint \--- \--- hint \---

Here are the code blocks you need:

![notes-sprite](images/note-sprite.png)

```blocks3
delete all of [notes v]

define load 'happy birthday'

add [1] to [notes v]

delete all of [times v]
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![notes-sprite](images/note-sprite.png)

```blocks3
define load 'happy birthday'
delete all of [notes v]
delete all of [times v]
add [1] to [notes v]
add [5] to [times v]
add [1] to [notes v]
add [5.5] to [times v]
add [3] to [notes v]
add [6] to [times v]
add [1] to [notes v]
add [7] to [times v]
add [6] to [notes v]
add [8] to [times v]
add [5] to [notes v]
add [9] to [times v]
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Test your new block by running it at the start of your project.

![notes-sprite](images/note-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
+ laad 'happy birthday' ::custom
verdwijn
zet klok op 0
```

Each of your lists should now contain six numbers.

![Lists of notes and times](images/lists-add.png)

\--- /task \---