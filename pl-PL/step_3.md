## Liczby binarne

Użyjesz różnych kombinacji naciskania czterech klawiszy, aby grać różne nuty. Każdy z klawiszy jest włączony (wciśnięty) lub wyłączony (nie wciśnięty). Oznacza to, że każdą kombinację kluczy można traktować jako liczbę binarną ****.

Przechodzenie z prawej do lewej klawisze mają podwójną wartość: `1`, `2`, `4`i `8`. Dodając liczby powyżej naciśniętych klawiszy, możesz obliczyć wartość nuty.

![Zwróć uwagę na przykłady wartości](images/note-values.png)

Istnieją 2<sup>4</sup> = **16 kombinacji** naciśnięcia czterech klawiszy. Oznacza to, że możesz grać 15 różnych dźwięków, ponieważ `0` oznacza, że żadna nuta nie jest odtwarzana.

\--- zadanie \--- Utwórz nową zmienną o nazwie `notatka`{: class = "block3variables"} i przeciągnij ją obok czterech duszków.

![Uwaga zmienna](images/note-create.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

`Uwaga`{: class = "block3variables"} zapisze wartość nuty, którą należy odtworzyć.

\--- zadanie \--- Dodaj kod do stołu montażowego, aby użyć kombinacji naciśniętych klawiszy do obliczenia wartości `uwagi`{: class = "block3variables"}.

Na przykład po naciśnięciu `c` i `v` wartość `nuty`{: class = "block3variables"} powinna wynosić `3`.

![Testowanie zmiennej notatki](images/note-test.png)

\--- wskazówki \--- \--- wskazówka \--- ![stage](images/stage.png) Po kliknięciu flagi ``{: class = "block3events"}, zmienna `note`{: class = "block3variables"} powinna wynosić `ustaw`{: class = "block3variables"} na `0`{: class = "block3variables"}.

+ `jeśli`{: class = "block3control"} naciśniesz klawisz `v`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić o `o 1`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `c`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić o `o 2`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `x`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić `o 4`{: class = „block3variables”}
+ `jeśli`{: class = "block3control"} naciśniesz klawisz `z`{: class = "block3sensing"}, `nutę`{: class = "block3variables"} należy zmienić `o 8`{: class = „block3variables”}

Cały ten kod należy powtórzyć `zawsze`{: class = "block3control"}. \--- / wskazówka \--- \--- wskazówka \--- Oto bloki kodu, których potrzebujesz i musisz dodać niektóre z nich więcej niż jeden raz: ![scena](images/stage.png)

```blocks3
na zawsze
koniec
jeśli < > to
koniec
klawisz (v) wciśnięty?

zmień [uwaga v] o ()

ustaw [uwaga v] na []

po kliknięciu flagi
```

\--- /hint \--- \--- hint \--- Twój kod powinien wyglądać tak: ![scena](images/stage.png)

```blocks3
kiedy flaga kliknęła
zawsze
ustaw [uwaga v] na [0]
jeśli wciśnięto klawisz <(vv)? > a następnie
zmiana [uwaga v] o (1)
koniec
jeśli naciśnięty został klawisz <(cv)? > a następnie
zmiana [uwaga v] o (2)
koniec
jeśli naciśnięto klawisz <(xv)? > a następnie
zmiana [uwaga v] o (4)
koniec
jeśli naciśnięto klawisz <(zv)? > a następnie
zmiana [uwaga v] o (8)
koniec
koniec
```

\--- /hint \--- \--- /hints \--- \--- /task \---