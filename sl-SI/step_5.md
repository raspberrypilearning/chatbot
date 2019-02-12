## Odločanje

S programom za klepet lahko programirate, da se odločite, kaj storiti na podlagi odgovorov, ki jih prejme.

Prvič, naredili boste, da bo vaš chatbot postavil vprašanje, na katerega je mogoče odgovoriti z "da" ali "ne".

\--- naloga \---

Spremenite kodo klepeta. Vaš chatbot naj postavi vprašanje "Ali ste v redu ime" z uporabo spremenljivke `name`{: class = "block3variables"}. Potem mora odgovoriti: "To je čudovito slišati!" `če`{: class = "block3control"} odgovor, ki ga prejme, je "da", vendar ne reci ničesar, če je odgovor "ne".

![Testiranje chatbota odgovora](images/chatbot-if-test1-annotated.png)

![Testiranje chatbota odgovora](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj
postavi [ime v] na (odgovor)
reci (pridruži se [Hi] (ime)) za (2) sekunde
+ vprašaj (pridruži se [Ali si v redu] (ime)) in počakajte
+, če <(odgovor) = [yes]> nato 
  recite [to je super slišati!] za (2) sekunde
konec
```

Za pravilno preizkusiti novo kodo, jo preizkusite **dvakrat**: enkrat z odgovorom "da", in enkrat z odgovorom "ne".

\--- / naloga \---

Trenutno vaš chatbot ne pove ničesar o odgovoru "ne".

\--- naloga \---

Spremenite kodo klepetalnice, tako da bo odgovoril "Oh ne!" če prejme "ne" kot odgovor na "Ali ste v redu ime".

Zamenjajte blok `if, nato`{: class = "block3control"} z blokado `if, then else`{: class = "block3control"} in vključite kodo, tako da bo chatbot lahko `rekel "Oh ne!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj
nastavljen [ime v] na (odgovor)
reci (pridruži se [Hi] (ime)) za (2) sekunde
vprašaj (pridruži se [Ali si v redu] ( ime)) in počakajte

+, če <(odgovor) = [yes]> nato 
  recite [to je super slišati!] za (2) sekunde
drugo 
+ recite [Oh ne!] za (2) sekunde
konec
```

\--- / naloga \---

\--- naloga \---

Preverite svojo kodo. Ko odgovorite "ne" in ko odgovorite z "da", morate dobiti drugačen odziv: vaš klepet mora odgovoriti s "To je čudovito slišati!" ko odgovorite z "da" (ki ni občutljiv na velike in male črke), in odgovorite z "Oh ne!" ko boste odgovorili **karkoli drugega**.

![Testiranje chatbota odgovora](images/chatbot-if-test2.png)

![Testiranje odgovora da / ne](images/chatbot-if-else-test.png)

\--- / naloga \---

Vnesete lahko katerokoli kodo znotraj bloka `, potem, drugje`{: class = "block3control"}, ne le kode, da bi vaš chatbot govoril!

Če kliknete kartico **kostumi** vašem klepetalnici, boste videli, da obstaja več kostumov.

![kostumi za klepet](images/chatbot-costume-view-annotated.png)

\--- naloga \---

Spremenite kodo klepetalnice, tako da bo klepet klepetalnice klical, ko vnesete odgovor.

![Testiranje spreminjajočega kostuma](images/chatbot-costume-test1.png)

![Testiranje spreminjajočega kostuma](images/chatbot-costume-test2.png)

Spremenite kodo znotraj `če, potem, drugje`{: class = "block3control"} bloka na `stikalo kostum`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj
nastavljen [ime v] na (odgovor)
reci (pridruži se [Hi] (ime)) za (2) sekunde
vprašaj (pridruži se [Ali si v redu] ( ime)) in počakajte
če <(odgovor) = [yes]> nato 

+ preklopite kostum na (nano-c v)
  recite [to je super slišati!] za (2) sekunde
drugo 
+ preklopite kostum na (nano- d v)
  izgovorite [Oh no!] za (2) sekunde
koncu
```

Preverite in shranite kodo. Videti morate, da se bo obraz vašega klepeta spremenil glede na vaš odgovor.

\--- / naloga \---

Ali ste opazili, da se po tem, ko se je kostum vaše klepetalnice spremenil, to zgodi in se ne spremeni nazaj na to, kar je bilo na začetku?

Lahko poskusite to: zaženite kodo in odgovorite "ne", da se bo obraz vašega klepeta spremenil v nesrečen pogled. Nato znova zaženite kodo in opazite, da se vaš chatbot ne spremeni nazaj v iskalno zadovoljstvo, preden vpraša vaše ime.

![Žuželka za kostum](images/chatbot-costume-bug-test.png)

\--- naloga \---

Da bi rešili ta problem, dodati kode chatbot za `stikalo kostum`{: class = "block3looks"} na začetku `, ko je Sprite kliknili`{: class = "block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta sprite kliknil

+ preklopi kostum na (nano-a v)
vprašaj [kako ti je ime?] in počakaj
```

![Testiranje popravila kostuma](images/chatbot-costume-fix-test.png)

\--- / naloga \---