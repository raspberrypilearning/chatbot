## Tehdä päätöksiä

Voit ohjelmoida chatbotin päättää, mitä tehdä vastausten perusteella.

Ensinnäkin aiot tehdä chatbotista kysymyksen, johon voidaan vastata "kyllä" tai "ei".

\--- tehtävä \---

Muuta chatbotin koodia. Chatbotin pitäisi kysyä kysymyksestä "Oletko OK nimi" käyttämällä `nimeä`{: class = "block3variables"} muuttujaa. Sitten sen pitäisi vastata "On hienoa kuulla!" `jos`{: class = "block3control"} sen saama vastaus on "kyllä", mutta ei sano mitään, jos vastaus on "ei".

![Chatbot-vastauksen testaaminen](images/chatbot-if-test1-annotated.png)

![Chatbot-vastauksen testaaminen](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota
asettaa [nimi v] (vastaus)
sanomaan (liity [Hi] (nimi)) (2) sekunnin ajan
+ kysy (liity [Oletko OK] (nimi)) ja odota
+, jos <(vastaus) = [yes]> sitten 
  sanoa [Se on hienoa kuulla!] (2) sekuntia
loppuun
```

Jos haluat testata uuden koodin oikein, testaa se **kahdesti**: kerran vastauksella "kyllä" ja kerran vastauksella "ei".

\--- / tehtävä \---

Tällä hetkellä chatbot ei sano mitään vastaukseen "ei".

\--- tehtävä \---

Muuta chatbotin koodia niin, että se vastaa "Voi ei!" jos se vastaanottaa "ei" vastauksena "Oletko OK nimi".

Korvata `jos, niin`{: class = "block3control"} lohko, jossa on `, jos, niin, muuten`{: class = "block3control"} lohko, ja sisältää koodin, joten chatbot voi `sanoa "Voi ei!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota
setti [nimi v] (vastaus)
sanoa (liity [Hi] (nimi)) (2) sekuntia
kysy (liity [Oletko OK] ( nimi)) ja odota

+, jos <(vastaus) = [yes]> sitten 
  sanoa [Se on hienoa kuulla!] (2) sekuntia
muuta 
+ sanoa [Voi ei!] (2) sekuntia
loppuun
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa koodi. Sinun pitäisi saada erilainen vastaus, kun vastaat "ei" ja kun vastaat "kyllä": chatbotin pitäisi vastata "On hienoa kuulla!" kun vastaat "kyllä" (mikä ei ole kirjainkohtainen) ja vastaa "Voi ei!" kun vastaat **mitään muuta**.

![Chatbot-vastauksen testaaminen](images/chatbot-if-test2.png)

![Kyllä / ei vastauksen testaus](images/chatbot-if-else-test.png)

\--- / tehtävä \---

Voit laittaa minkä tahansa koodin `jos sitten`{: class = "block3control"} estää, ei vain koodia, jotta chatbot puhuu!

Jos napsautat chatbot's **Costumes** -välilehteä, näet, että on olemassa useampi kuin yksi puku.

![chatbot-puvut](images/chatbot-costume-view-annotated.png)

\--- tehtävä \---

Muuta chatbotin koodia niin, että chatbot vaihtaa puvut, kun kirjoitat vastauksesi.

![Muuttuvan puvun testaus](images/chatbot-costume-test1.png)

![Muuttuvan puvun testaus](images/chatbot-costume-test2.png)

Muuta koodia `sisällä, jos sitten`{: class = "block3control"} lohko `kytkinpuku`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota
setti [nimi v] (vastaus)
sanoa (liity [Hi] (nimi)) (2) sekuntia
kysy (liity [Oletko OK] ( nimi)) ja odota
jos <(vastaus) = [yes]> sitten 

+ kytke puku (nano-c v)
  sanoa [Se on hienoa kuulla!] (2) sekuntia
muuta 
+ vaihtaa puku (nano- d v)
  sanoa [Voi ei!] (2) sekuntia
loppuun
```

Testaa ja tallenna koodi. Sinun pitäisi nähdä chatbotin kasvot muuttuvat vastauksesi mukaan.

\--- / tehtävä \---

Oletteko huomanneet, että kun chatbot-puku on muuttunut, se pysyy sellaisena ja ei muutu takaisin siihen, mitä se oli alussa?

Voit kokeilla tätä: suorita koodi ja vastaa "ei" niin, että chatbotin kasvot muuttuvat onnettomaksi. Suorita sitten koodi uudelleen ja huomaa, että chatbot ei muutu takaisin etsimään onnellista ennen kuin se pyytää nimeäsi.

![Puku bug](images/chatbot-costume-bug-test.png)

\--- tehtävä \---

Voit korjata tämän ongelman lisäämällä chatbotin koodiin `kytkinpuku`{: class = "block3looks"} alussa `kun sprite napsautetaan`{: class = "block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti

+ vaihtaa pukua (nano-a v)
kysy [Mikä on nimesi?] ja odota
```

![Pukukorjauksen testaus](images/chatbot-costume-fix-test.png)

\--- / tehtävä \---