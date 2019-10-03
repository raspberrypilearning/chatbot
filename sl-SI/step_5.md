## Sprejemanje odločitev

Svojega klepetalnega robota lahko sprogramiraš, da se bo znal odločiti, kaj naj stori, glede na odgovore, ki jih dobi.

Najprej boš naredil, da bo tvoj robot vprašal vprašanje, na katerega se da odgovoriti z "da" in "ne".

\--- task \---

Spremeni kodo klepeta. Vaš klepetalni robot naj postavi vprašanje "Ali ste v redu, ime", tako da uporabi spremenljivko `ime`{: class = "block3variables"}. Na to naj odgovori "To je dobro slišati!", `če`{: class = "block3control"} je odgovor "da", če pa je odgovor "ne", naj ne reče ničesar.

![Testiranje odziva klepetalnega robota](images/chatbot-if-test1-annotated.png)

![Testiranje odziva klepetalnega robota](images/chatbot-if-test2.png)

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj

+ nastavi [ime v] na (odgovor)
reci (združi [Živijo, ] (ime :: spremenljivke +)) za (2) sekund
+ vprašaj (združi [Ali si v redu, ] (ime)) in počakaj
+ če <(odgovor) = [da]> potem 
  reci [To je dobro slišati!] za (2) sekund
konec
```

Za pravilno preizkusiti novo kodo, jo preizkusite **dvakrat**: enkrat z odgovorom "da", in enkrat z odgovorom "ne".

\--- /task \---

Trenutno tvoj roboto ničesar ne reče ob odgovoru "ne".

\--- task \---

Spremeni kodo, tako da bo klepetalni robot odgovoril "Oh, ne!" če prejme "ne" kot odgovor na vprašanje "Ali si v redu, ime?".

Zamenjaj blok `če, potem`{: class = "block3control"} z blokom `če, potem sicer`{: class = "block3control"} in vključi kodo, da bo robot lahko `rekel "Oh, ne!"`{: class = "block3looks"}.

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj
nastavi [ime v] na (odgovor)
reci (združi [Živjo, ] (ime :: spremenljivke +)) za (2) sekund
vprašaj (združi [Ali si v redu, ] (ime)) in počakaj

+ če <(odgovor) = [da]> potem 
  reci [To je dobro slišati!] za (2) sekund
sicer
+ reci [Oh, ne!] za (2) sekunde
konec
```

\--- /task \---

\--- task \---

Preveri svojo kodo. Glede na to ali je odgovor "da" ali "ne", bi se moral odziv klepetalnega robota razlikovati: Ob odgovoru "da" (odgovor ne razlikuje malih in velikih črk) mora odgovoriti "To je dobro slišati!", **sicer** pa odgovori "Oh, ne!".

![Testiranje odziva klepetalnega robota](images/chatbot-if-test2.png)

![Testiranje odgovora da / ne](images/chatbot-if-else-test.png)

\--- /task \---

Znotraj bloka `če, potem, sicer`{: class = "block3control"} lahko imaš poljubno kodo, ne le kode, ki omogoča, da tvoj robot govori!

Če klikneš na zavihek **Videzi** za vašega klepetalnega robota, boš videl, da ima figura več videzov.

![videzi klepetalnega robota](images/chatbot-costume-view-annotated.png)

\--- task \---

Spremeni kodo klepetalnega robota, tako da bo robot menjal videz, ko vneseš odgovor.

![Testiranje spreminjajočega se videza](images/chatbot-costume-test1.png)

![Testiranje spreminjajočega se videza](images/chatbot-costume-test2.png)

Spremeni kodo znotraj bloka `če, potem, sicer`{: class = "block3control"} v `zamenjaj videz`{: class = "block3looks"}.

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj

nastavi [ime v] na (odgovor)
reci (združi [Živijo, ] (ime :: spremenljivke +)) za (2) sekund
vprašaj (združi [Ali si v redu, ] (ime)) in počakaj
če <(odgovor) = [da]> potem 

+ zamenjaj videz na (nano-c v)  
reci [To je dobro slišati!] za (2) sekund
sicer
+ zamenjaj videz na (nano- d v)
  reci [Oh, ne!] za (2) sekund
konec
```

Preveri in shrani svojo kodo. Obraz tvojega klepetalnega robota bi se sedaj moral spreminjati glede na odgovor.

\--- /task \---

Ali si opazil, da se videz tvojega klepetalnega robota po zamenjavi videza ne spremeni nazaj v začetni videz, temveč ostane spremenjen?

Lahko poskusiš to: zaženi kodo in odgovori z "ne", da se bo obraz tvojega robota spremenil v nesrečen pogled. Nato znova zaženi kodo in opazil boš, da se tvoj klepetalni robot ne spremeni nazaj an srečen obraz, preden te vpraša za ime.

![Videz hrošča](images/chatbot-costume-bug-test.png)

\--- task \---

Da bi odpravil to težavo, dodaj kodi klepetalnega robota `zamenjaj videz`{: class = "block3looks"} takoj za začetnim blokom `ko kliknemo to figuro`{: class = "block3events"}.

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro

+ zamenjaj videz na (nano-a v)
vprašaj [Kako ti je ime?] in počakaj
```

![Testiranje popravljenega videza](images/chatbot-costume-fix-test.png)

\--- /task \---