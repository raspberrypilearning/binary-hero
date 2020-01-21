## Graj w notatki

Odtwarzaj nuty po naciśnięciu klawiszy.

\--- task \---

Dodaj rozszerzenie Music do swojego projektu.

[[[generic-scratch3-add-music-extension]]]

\--- /task \---

\--- task \---

Broadcast a 'note change' message whenever **any of the four keys** is pressed.

![sprite 1](images/1.png)

```blocks3
kiedy flaga kliknęła
zawsze
jeśli wciśnięto < klawisze (vv)?> następnie
przełącz kostium na (on v)
+ transmisja (zmiana notatki v)
inaczej
przełącz kostium na (off v)
koniec
```

\--- /task \---

\--- task \---

Add code to the Stage to play a note when a combination of keys is pressed.

Your notes should start at middle C, which is note 60.

```blocks3
zagraj nutę (60) dla (1) uderzeń
```

\--- hints \--- \--- hint \---

![1 sprite](images/stage.png)

When your stage `receives`{:class="block3events"} the 'change note' broadcast, it should `stop all sounds`{:class="block3sound"} before `playing a note`{:class="block3sound"} based on the value of the`note`{:class="block3variables"} variable.

+ Gdy zmienna `nuta`{: class = "block3variables"} ma wartość `1`{: class = "block3variables"}, uwaga 60 powinna być odtwarzana
+ Gdy zmienna `przypis`{: class = "block3variables"} ma wartość `2`{: class = "block3variables"}, uwaga 61 powinna zostać odtworzona
+ Gdy zmienna `nuta`{: class = "block3variables"} ma wartość `3`{: class = "block3variables"}, uwaga 62 powinna być odtwarzana
+ itp...

\--- /hint \--- \--- hint \---

Here are the code blocks you need:

![stage](images/stage.png)

```blocks3
odtwórz nutę (60) dla (1) bije
gdy otrzymam [zmiana nuty v]
() + ()
(nuta)
zatrzymaj wszystkie dźwięki
```

\--- /hint \--- \--- hint \---

This is what your code should look like:

![stage](images/stage.png)

```blocks3
kiedy otrzymuję [zmiana nut v]
zatrzymaj wszystkie dźwięki
odtwarzaj nutę ((59) + (uwaga :: zmienne)) dla (1) uderzeń
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- task \---

Test your code. Can you hear that a note is repeatedly played when you hold down a key?

\--- no-print \---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Twoja przeglądarka nie obsługuje wideo HTML5.
</video>

\--- /no-print \---

\--- /task \---

\--- task \---

Add code so that the **all** the key sprites only play a note **once** when a key is held down?

![1 sprite](images/1.png)

```blocks3
kiedy flaga kliknęła
zawsze
jeśli wciśnięto < klawisze (vv)?> następnie
przełącz kostium na (on v)
transmisji (zmiana notatki v)
+ poczekaj, aż <not <key (v v) pressed?>
inaczej
przełącz kostium na (off v)
koniec
```

\--- /task \---