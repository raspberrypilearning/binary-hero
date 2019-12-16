## Graj w notatki

Odtwarzaj nuty po naciśnięciu klawiszy.

\--- task \---

Dodaj rozszerzenie Music do swojego projektu.

[[[generic-scratch3-add-music-extension]]]

\--- /task \---

\--- zadanie \--- Broadcast komunikat „uwaga zmiana” ilekroć **każdy z czterech kluczy** jest wciśnięty. ![duszek 1](images/1.png)

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

\--- zadanie \--- Dodaj kod do stołu montażowego, aby zagrać nutę po naciśnięciu kombinacji klawiszy.

Twoje notatki powinny zaczynać się w środku C, czyli w notatce 60.

```blocks3
zagraj nutę (60) dla (1) uderzeń
```

\--- wskazówki \--- \--- wskazówka \--- ![1 duszek](images/stage.png)

Kiedy twój stopień `odbierze`{: class = "block3events"} transmisja „zmień nutę”, powinien `zatrzymać wszystkie dźwięki`{: class = "block3sound"} przed `odtworzeniem nuty`{: class = "block3sound"} na podstawie wartości zmiennej`note`{: class = "block3variables"}.

+ Gdy zmienna `nuta`{: class = "block3variables"} ma wartość `1`{: class = "block3variables"}, uwaga 60 powinna być odtwarzana
+ Gdy zmienna `przypis`{: class = "block3variables"} ma wartość `2`{: class = "block3variables"}, uwaga 61 powinna zostać odtworzona
+ Gdy zmienna `nuta`{: class = "block3variables"} ma wartość `3`{: class = "block3variables"}, uwaga 62 powinna być odtwarzana
+ itp...

\--- /hint \--- \--- hint \--- Oto potrzebne bloki kodu: ![scena](images/stage.png)

```blocks3
odtwórz nutę (60) dla (1) bije
gdy otrzymam [zmiana nuty v]
() + ()
(nuta)
zatrzymaj wszystkie dźwięki
```

\--- /hint \--- \--- hint \--- Twój kod powinien wyglądać tak: ![scena](images/stage.png)

```blocks3
kiedy otrzymuję [zmiana nut v]
zatrzymaj wszystkie dźwięki
odtwarzaj nutę ((59) + (uwaga :: zmienne)) dla (1) uderzeń
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\---task\--- Wypróbuj swój kod. Czy słyszysz, że nuta jest odtwarzana wielokrotnie po przytrzymaniu klawisza?

\--- no-print \---

<video width="400" controls>
  <source src="images/play-note-bug.mp4" type="video/mp4">
  Twoja przeglądarka nie obsługuje wideo HTML5.
</video>

\--- /no-print \---

\--- /task \---

\--- zadanie \--- Dodać kod, aby sprajty klawiszowe **all** odtwarzały nutę **tylko raz** gdy klawisz jest wciśnięty?

![1 duszek](images/1.png)

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