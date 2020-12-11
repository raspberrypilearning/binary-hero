## Двоичные числа

Ты будешь использовать разные комбинации нажатия четырех клавиш для воспроизведения разных нот. Каждая из клавиш либо включена (нажата), либо выключена (не нажата). Это значит, что на каждую комбинацию клавиш можно смотреть как на **двоичное число**.

Читая справа налево, клавиши удваивают значение: `1`, `2`, `4` и `8`,. Сложив цифры относящиеся к клавишам, можно определить значение ноты.

![Примеры значений нот](images/note-values.png)

Существует 2<sup>4</sup> = **16 комбинаций** нажатия четырех клавиш. Это означает, что можно сыграть 15 разных нот, так как `0` будет означать отсутствие ноты.

--- task ---

Создай новую переменную с именем `нота`{:class="block3variables"} и перенеси её к четырем остальным спрайтам нот.

![Переменная ноты](images/note-create.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

В `ноте`{:class="block3variables"} будет храниться значение ноты, которую нужно сыграть.

--- task ---

Добавь код к Сцене, который вычисляет значение `ноты`{:class="block3variables"} используя комбинацию нажатых клавиш.

Например, когда `с` и `v` нажаты, значение `ноты`{:class="block3variables"} должно быть `3`.

![Проверка переменной ноты](images/note-test.png)

--- hints ---
 --- hint ---

![сцена](images/stage.png)

`Когда зелёный флаг нажат`{:class="block3events"}, переменной `нота`{:class="block3variables"} должно быть `задано значение 0`{:class="block3variables"}.

+ `если`{:class="block3control"} `нажата клавиша v`{:class="block3sensing"}, `нота`{:class="block3variables"} должна быть `изменена на 1` {:class="block3variables"}
+ `если`{:class="block3control"} `нажата клавиша с`{:class="block3sensing"}, `нота`{:class="block3variables"} должна быть `изменена на 2` {:class="block3variables"}
+ `если`{:class="block3control"} `нажата клавиша x`{:class="block3sensing"}, `нота`{:class="block3variables"} должна быть `изменена на 4`{:class="block3variables"}
+ `если`{:class="block3control"} `нажата клавиша z`{:class="block3sensing"}, `нота`{:class="block3variables"} должна быть `изменена на 8` {:class="block3variables"}

Весь этот код должен повторяться `всегда`{:class="block3control"}.

--- /hint --- --- hint ---

Вот необходимые блоки кода, а ты должен добавить некоторые из них более одного раза:

![сцена](images/stage.png)

```blocks3
forever
end
if < > then
end
key ( v) pressed?

change [нота v] by ( )

set [нота v] to [ ]

when flag clicked
```

--- /hint --- --- hint ---

Так должен выглядеть твой код:

![сцена](images/stage.png)

```blocks3
when flag clicked
forever
set [нота v] to [0]
if <key (v v) pressed? > then
change [нота v] by (1)
end
if <key (c v) pressed? > then
change [нота v] by (2)
end
if <key (x v) pressed? > then
change [нота v] by (4)
end
if <key (z v) pressed? > then
change [нота v] by (8)
end
end
```

--- /hint ------ /hints --- --- /task ---