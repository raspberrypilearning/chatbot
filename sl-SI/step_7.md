## Spreminjanje lokacije

Lahko tudi programirate svoj chatbot, da spremenite njegovo lokacijo!

![Testiranje spreminjanja ozadja](images/chatbot-backdrop-moon.png)

\--- naloga \---

Ali lahko programirate svoj chatbot in vprašate "Ali želite iti na luno" in nato spremeniti ozadje, ko je odgovor "da"?

\--- namigi \---

\--- namig \---

Vaš chatbot mora `vprašati "Ali želite iti na luno?"`{: class = "block3sensing"}, in `če`{: class = "block3control"} vas `odgovor`{: class = "block3sensing"} "da", mora `preklopiti ozadje na luno`{: class = "block3looks"}.

\--- /namig \---

\--- namig \---

Tukaj so kodni bloki, ki jih morate dodati vaši chatbot kodi.

![nano sprite](images/nano-sprite.png)

```blocks3
preklopi ozadje na (mesec v)

vprašaj [Ali želiš iti na luno?] in počakaj

če <(odgovor) = [yes]> nato 

konec
```

\--- /namig \---

\--- namig \---

Takšna mora biti vaša koda:

```blocks3
vprašaj [Ali hočeš iti na luno?] in počakaj
če <(odgovor) = [yes]> nato 
  stikalo ozadja na (luna v)
konec
```

\--- /namig \---

\--- / namigi \---

\--- / naloga \---

\--- naloga \---

Zdaj morate poskrbeti, da se bo vaš chatbot začel na pravi lokaciji, ko boste kliknili nanj in se pogovorili z njim. Dodajte ta blok na vrh kode za klepet:

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo

+ preklopi ozadje na (presledek v)
```

\--- / naloga \---

\--- naloga \---

Preizkusite program in odgovorite "da", ko chatbot vpraša, ali želite iti na luno. Videti morate, da se lokacija klepetalnice spremeni.

\--- / naloga \---

\--- naloga \---

Naslednjo kodo lahko dodate tudi v novi blok `če`:

![nano sprite](images/nano-sprite.png)

```blocks3
če <(odgovor) = [yes]> nato 
  stikalo ozadje na (luna v)

+ ponavljanje (4) 
    spremeni y z (10)
    čakaj (0.1) sek
    spremeni y ((-10)
    čakaj (0.1) sekund
  konec
konec
```

\--- / naloga \---