## Przechowuj swoją piosenkę

W tej chwili notatki są usuwane z list po odtworzeniu, więc masz puste listy:

![Puste listy](images/empty-lists.png)

Teraz dodasz kod do przechowywania piosenek w swoim projekcie, abyś nie musiał za każdym razem dodawać do list.

![Dodaj notatki i czasy do list](images/lists-add-annotated.png)

\--- zadanie \--- Utwórz nowy blok o nazwie `ładuj „wszystkiego najlepszego z okazji urodzin”`{: class = "block3myblocks"}, który usuwa obie `notatki`{: class = "block3variables"} i `razy`{: class = "block3variables"} list, a następnie dodaje poprawne liczby z powrotem do obu list. [[[generic-scratch3-make-block]]] \--- wskazówki \--- \--- wskazówka \--- `ładowanie „wszystkiego najlepszego”`{: class = "block3myblocks"} blok powinien `usunąć wszystkie`{: class = "block3variables "} pozycje z obu `notatek`{: class =" block3variables "} i `razy`{: class =" block3variables "}, a następnie `dodaje`{: class =" block3variables "} poprawnych sześciu liczb do listy należą do, we właściwej kolejności. \--- /wskazówka \--- \--- wskazówka \--- Oto potrzebne bloki kodu: ![notatki-duszek](images/note-sprite.png)

```blocks3
usuń (wszystkie v) z [notatek v]

zdefiniuj ładuj „wszystkiego najlepszego”

dodaj [1] do [notatek v]

usuń (wszystkie v) z [czasów v]
```

\--- /hint \--- \--- hint \--- Twój kod powinien wyglądać tak: ![notatki-duszek](images/note-sprite.png)

```blocks3
zdefiniuj ładowanie „wszystkiego najlepszego”
usuń (wszystkie v) z [notatek v]
usuń (wszystkie v) z [razy v]
dodaj [1] do [notatek v]
dodaj [5] do [razy v]
dodaj [1] do [notatek v]
dodaj [5.5] do [razy v]
dodaj [3] do [notatek v]
dodaj [6] do [razy v]
dodaj [1] do [notatek v]
dodaj [7] do [razy v]
dodaj [6] do [notatek v]
dodaj [8] do [razy v]
dodaj [5] do [notatek v]
dodaj [9] do [razy v]
```

\--- /hint \--- \--- /hints \--- \--- /task \---

\--- zadanie \--- Przetestuj nowy blok, uruchamiając go na początku projektu. ![notatki-duszek](images/note-sprite.png)

```blocks3
po kliknięciu flagi
+ załaduj „wszystkiego najlepszego” :: niestandardowe
ukryj
zeruj licznik czasu
```

Każda z twoich list powinna teraz zawierać sześć liczb.

![Listy notatek i czasów](images/lists-add.png) \--- /task \---