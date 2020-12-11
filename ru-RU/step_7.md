## Больше пользовательских блоков

Новую часть кода сложно прочитать, поэтому мы будем использовать больше пользовательских блоков, чтобы упростить ее.

\--- task \---

Создайте еще один блок с имененм `очистить песню`{:class="block3myblocks"}, который удаляет все элементы из обоих списков. Используй этот блок, прежде чем добавлять числа обратно в списки.

![спрайт ноты](images/note-sprite.png)

```blocks3
define clear song
delete (all v) of [notes v]
delete (all v) of [times v]
```

Когда тестируешь код, он должен работать так же, как и раньше.

```blocks3
define load 'happy birthday'
+clear song ::custom
add [1] to [notes v]
add [5] to [notes v]
```

\--- /task \---

\--- task \---

Чтобы код было еще проще читать, сделай еще один блок, который позволит указать ноту и время ее воспроизведения.

[[[generic-scratch3-make-block-parameters]]]

\--- hints \--- \--- hint \---

Сделай блок, который берет число, относящееся к `ноте`{:class="block3variables"} и число, относящееся к `времени`{:class="block3variables"} и `добавляет`{:class="block3variables"} каждое число в правильный список.

\--- /hint \--- \--- hint \---

Так должен выглядеть твой код:

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