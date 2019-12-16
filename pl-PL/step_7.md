## Więcej niestandardowych bloków

Najnowsza sekcja kodu jest trudna do odczytania, więc będziesz używać więcej niestandardowych bloków, aby uprościć.

\--- zadanie \--- Utwórz kolejny blok o nazwie `wyczyść piosenkę`{: class = "block3myblocks"}, który usuwa wszystkie elementy z obu list. Użyj tego bloku przed dodaniem liczb z powrotem do list.

![notatka-duszek](images/note-sprite.png)

```blocks3
zdefiniuj czysty utwór
usuń (wszystkie v) z [uwagi v]
usuń (wszystkie v) z [razy v]
```

Podczas testowania kodu powinien on działać tak jak wcześniej.

```blocks3
zdefiniuj ładowanie „wszystkiego najlepszego”
+ wyczyść piosenkę :: niestandardowe
dodaj [1] do [notatek v]
dodaj [5] do [notatek v]
```

\--- /task \---

\--- zadanie \--- Aby twój kod był jeszcze łatwiejszy do odczytania, stwórz kolejny blok, który pozwoli ci określić nutę do odtworzenia i godzinę na odtworzenie nuty.

[[[generic-scratch3-make-block-parameters]]]

\--- wskazówki \--- \--- wskazówka \--- Zrób blok, który przyjmuje liczbę `jako notatkę`{: class = "block3variables"} i liczbę jako `razy`{: class = "block3variables"} a `dodaje`{: class = "block3variables"} każdą liczbę do poprawnej listy. \--- / hint \--- \--- hint \--- Tak powinien wyglądać Twój kod:

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