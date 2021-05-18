## Guarda tu canción

Hasta el momento, las notas se eliminan desde las listas después de ser reproducidas, así que quedas con listas vacías:

![Listas vacías](images/empty-lists.png)

Ahora vas a agregar código para guardar las canciones en tu proyecto, para que solo tengas que agregarlas una vez a tus listas.

![Añadir notas y tiempos a las listas](images/lists-add-annotated.png)

\--- task \---

Crea un nuevo bloque que se llame `carga «feliz cumpleaños»`{:class="block3myblocks"} que borre las listas `notas`{:class="block3variables"} y `tiempos`{:class="block3variables"}, y luego añade los números correctos a ambas listas. [[[generic-scratch3-make-block]]]

\--- hints \--- \--- hint \---

El bloque `cargar «feliz cumpleaños»`{:class="block3myblocks"} debería `eliminar todos`{:class="block3variables"} los elementos de las listas `notas`{:class="block3variables"} y `tiempos`{:class="block3variables"} y, a continuación, `añadir`{:class="block3variables"} los seis números correctos de la lista en la que pertenecen, en el orden correcto.

\--- /hint \--- \--- hint \---

Aquí están los bloques de código que necesitas:

![objetos nota](images/note-sprite.png)

```blocks3
delete all of [notes v]

define load 'happy birthday'

add [1] to [notes v]

delete all of [times v]
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![objetos nota](images/note-sprite.png)

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

Prueba tu nuevo bloque ejecutándolo al inicio de tu proyecto.

![objetos nota](images/note-sprite.png)

```blocks3
when flag clicked
+load 'happy birthday' ::custom
hide
reset timer
```

Ahora, cada una de tus listas debe contener seis números.

![Listas de notas y tiempos](images/lists-add.png)

\--- /task \---