## Más bloques personalizados

La nueva sección del código es difícil de leer, así que usarás más bloques personalizados para simplificarlo.

\--- task \---

Haz otro bloque que se llame `borrar canción`{:class="block3myblocks"} que elimine todos los objetos de ambas listas. Usa este bloque antes de volver a agregar números en las listas.

![objetos nota](images/note-sprite.png)

```blocks3
define clear song
delete all of [notes v]
delete all of [times v]
```

Cuando pruebes tu código, debería funcionar como antes.

```blocks3
define load 'happy birthday'
+clear song ::custom
add [1] to [notes v]
add [5] to [notes v]
```

\--- /task \---

\--- task \---

So that your code is even easier to read, make another block that allows you to specify a note to be played and a time to play the note at.

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

Make a block that takes a number as `note`{:class="block3variables"} and a number as `time`{:class="block3variables"} and `adds`{:class="block3variables"} each number to the correct list.

\--- /hint \--- \--- hint \---

Así es como debería verse tu código:

```blocks3
define Add note (note) at (time) secs
add (note :: custom-arg) to [notes v]
add (time :: custom-arg) to [times v]

define load 'happy birthday'
clear song ::custom
+Add note (1) at (5) secs
+Add note (1) at (5.5) secs
+Add note (3) at (6) secs
+Add note (1) at (7) secs
+Add note (6) at (8) secs
+Add note (5) at (9) secs
```

\--- /hint \--- \--- /hints \---

\--- /task \---