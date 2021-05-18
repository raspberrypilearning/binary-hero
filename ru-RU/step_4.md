## Воспроизведи ноты

Воспроизведи ноты, когда клавиши нажаты.

\--- task \---

Добавь расширение Музыка в твой проект.

[[[generic-scratch3-add-music-extension]]]

\--- /task \---

\--- task \---

Передавай сообщение «смена ноты» всякий раз, когда **любая из четырех клавиш** нажата.

![спрайт 1](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
+broadcast (note change v)
else
switch costume to (off v)
end
```

\--- /task \---

\--- task \---

Добавь код к Сцене для воспроизведения ноты при нажатии комбинации клавиш.

Ноты должны начинаться со средней C, а это нота 60.

```blocks3
play note (60) for (1) beats
```

\--- hints \--- \--- hint \---

![1 спрайт](images/stage.png)

Когда сцена `получает`{:class="block3events"} сообщение 'смена ноты', она должна `остановить все звуки`{:class="block3sound"} до `воспроизведения ноты`{:class="block3sound"} на основе значения переменной `нота`{:class="block3variables"}.

+ Когда значение переменной `нота`{:class="block3variables"} будет `1`{:class="block3variables"}, должна играть нота 60
+ Когда значение переменной `нота`{:class="block3variables"} станет `2`{:class="block3variables"}, должна играть нота 61
+ Когда значение переменной `нота`{:class="block3variables"} станет `3`{:class="block3variables"}, должна играть нота 62
+ и т. д...

\--- /hint \--- \--- hint \---

Вот блоки кода, которые тебе нужны:

![сцена](images/stage.png)

```blocks3
play note (60) for (1) beats
when I receive [note change v]
() + ()
(note)
stop all sounds
```

\--- /hint \--- \--- hint \---

Так должен выглядеть твой код:

![сцена](images/stage.png)

```blocks3
when I receive [note change v]
stop all sounds
play note ((59) + (note :: variables)) for (1) beats
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Проверь свой код. Слышишь, как повторяется нота, когда ты удерживаешь клавишу?

\--- no-print \---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Your browser does not support HTML5 video.
</video>

\--- /no-print \---

\--- /task \---

\--- task \---

Add code so that the **all** the key sprites only play a note **once** when a key is held down.

![1 спрайт](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
broadcast (note change v)
+wait until <not <key (v v) pressed?>
else
switch costume to (off v)
end
```

\--- /task \---