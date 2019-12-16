## Zachowaj wynik

Popraw swoją grę, przyznając graczom punkty za zagranie właściwej nuty.

\--- zadanie \--- Utwórz nową zmienną o nazwie `score`{: class = "block3variables"} i umieść ją na górze stołu montażowego.

![Dodaj wynik](images/add-score.png) \--- /task \---

\--- zadanie \--- Dodaj do `wyniku`{: class = "block3variables"} za każdym razem, gdy gracz zagra prawidłową nutę we właściwym czasie. Pamiętaj, aby ustawić `punktów`{: class = "block3variables"} na `0`{: class = "block3variables"} na początku gry.

Wskazówki \--- \--- \--- wskazówkę \--- `Przed każdym klon usunięte`{: klasa = "block3control"}, to należy sprawdzić, `, jeśli`{: klasa = "block3control"} z `Uwaga`{: class = "block3variables"} ma wartość `równą`{: class = "block3operators"} `kostium numer`{: class = "block3looks"}, w takim przypadku wynik powinien zostać zmieniony ``{ : class = "block3variables"}. \--- /wskazówka \--- \--- wskazówka \--- Oto potrzebne bloki kodu: ![Uwaga](images/note-sprite.png)

```blocks3
[] = []
(kostium [liczba v])
(uwaga)
zmień [wynik v] o (1)

jeśli <> to

kończy
```

\--- /hint \--- \--- hint \--- Twój kod powinien wyglądać tak: ![Uwaga](images/note-sprite.png)

```blocks3
kiedy zaczynam jako klon
przejdź do x: (20) y: (160)
pokaż
szybowanie (2) s do x: (20) y: (- 130)
+ if <(uwaga :: zmienne) = (kostium [numer v])> a następnie
zmień [wynik v] o (1)

usuń ten klon
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- zadanie \--- Nadaj komunikat o nazwie „poprawny”, gdy odtwarzana jest właściwa nuta. ![Uwaga](images/note-sprite.png)

```blocks3
kiedy zaczynam jako klon
przejdź do x: (20) y: (160)
pokaż
szybowanie (2) sek. do x: (20) y: (- 130)
jeśli <(uwaga :: zmienne) = ( kostium [numer v])> a następnie
zmień [wynik v] o (1)
+ transmisja (poprawne v)
koniec
usuń ten klon
```

\--- /task \---

\--- zadanie \--- ![Prawidłowe tło sceny](images/correct-costume.png)

Dodaj kod do stołu montażowego, aby krótko zmienić tło, gdy gracz zagra prawidłową nutę. Projekt zawiera już drugie tło do tego.

![scena](images/stage.png)

```blocks3
po kliknięciu flagi
przełącz tło na (normalne v)

gdy otrzymam [poprawne v]
przełącz tło na (prawidłowe v)
poczekaj (0,3) sekundy
przełącz tło na (normalne v)
```

\--- /task \---