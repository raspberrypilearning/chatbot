## Otsuste tegemine

Saate oma vestlusboti programmeerida, et otsustada, mida teha saadud vastuste põhjal.

Esiteks, te teete oma vestlusbotilt küsimuse, millele saab vastata "jah" või "ei".

\--- ülesanne \---

Muutke oma vestluskoodi koodi. Teie chatbot peaks küsima "Kas olete OK nimi", kasutades `nime`{: class = "block3variables"} muutuja. Siis peaks see vastama "See on tore kuulda!" `kui`{: class = "block3control"} see vastus on "jah", kuid ei ütle midagi, kui vastus on "ei".

![Vestlusvestluse vastuse testimine](images/chatbot-if-test1-annotated.png)

![Vestlusvestluse vastuse testimine](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis on sinu nimi?] ja oodake
set [nimi v] (vastus)
(liitu [Hi] (nimi)) (2) sekundi jooksul
+ küsi (liituda [Kas oled OK] (nimi)) ja oodake
+, kui <(vastus) = [yes]> siis 
  öelda [See on tore kuulda!] (2) sekundit
lõpp
```

Uue koodi õigeks testimiseks peaksite seda testima **kaks korda**: üks kord vastusega "jah" ja üks kord vastusega "ei".

\--- / ülesanne \---

Hetkel ei ütle teie vestlusobjekt vastusele "ei" midagi.

\--- ülesanne \---

Muutke oma vestluskoodi koodi nii, et see vastab "Oh ei!" kui ta saab vastuse küsimusele "Kas olete OK", siis "ei".

Vahetage `, siis`{: class = "block3control"} plokk `kui, siis muul`{: class = "block3control"}, ja lisage kood nii, et jututoad saaksid `öelda "Oh ei!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis on sinu nimi?] ja oodake
set [nimi v] (vastus)
(liitu [Hi] (nimi)) (2) sekundi jooksul
küsi (liituda [Kas olete OK] ( nimi)) ja oodake

+, kui <(vastus) = [yes]> siis 
  ütlevad [See on tore kuulda!] (2) sekundit
muidu 
+ öelda [Oh ei!] (2) sekundit
lõpp
```

\--- / ülesanne \---

\--- ülesanne \---

Testige oma koodi. Kui vastate "ei" ja vastate "jah", peaksite saama teistsuguse vastuse: teie vestlusbot peaks vastama "See on tore kuulda!" kui vastate "jah" (mis ei ole tõstutundlik) ja vastake "Oh ei!" kui vastate **midagi muud**.

![Vestlusvestluse vastuse testimine](images/chatbot-if-test2.png)

![Jah / ei vastuse testimine](images/chatbot-if-else-test.png)

\--- / ülesanne \---

`kui muidu`{: class = "block3control"} blokeerida, ei saa sisestada koodi, mitte ainult koodi, et muuta oma jututoad rääkima!

Kui klõpsate vahekaardil chatbot **kostüümi** , näete, et seal on rohkem kui üks kostüüm.

![chatboti kostüümid](images/chatbot-costume-view-annotated.png)

\--- ülesanne \---

Muutke oma chatbot'i koodi nii, et vestlusbot vahetab kostüümid, kui sisestate oma vastuse.

![Muutuva kostüümi testimine](images/chatbot-costume-test1.png)

![Muutuva kostüümi testimine](images/chatbot-costume-test2.png)

Muutke koodi `kui siis, muidu`{: class = "block3control"} blokeerige `lüliti kostüümi`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis on sinu nimi?] ja oodake
set [nimi v] (vastus)
(liitu [Hi] (nimi)) (2) sekundi jooksul
küsi (liituda [Kas olete OK] ( nimi)) ja oodake
kui <(vastus) = [yes]> siis 

+ lülita kostüüm (nano-c v)
  öelda [See on tore kuulda!] (2) sekundit
teist 
+ kostüümi vahetamine (nano- d v)
  öelda [Oh ei!] (2) sekundit
lõppu
```

Testige ja salvestage oma kood. Te peaksite nägema oma vestluspanu nägu vastavalt teie vastusele.

\--- / ülesanne \---

Kas olete märganud, et pärast seda, kui teie chatboti kostüüm on muutunud, jääb see selliseks ja ei muutu tagasi selle algusesse?

Seda saab proovida: käivitage oma kood ja vastake „ei”, nii et teie chatboti nägu muutub õnnetu välimuseks. Seejärel käivitage oma kood uuesti ja märkige, et teie chatbot ei muutu tagasi õnnelikuks, enne kui küsib teie nime.

![Kostüümi viga](images/chatbot-costume-bug-test.png)

\--- ülesanne \---

Selle probleemi lahendamiseks lisage chatboti koodile `lüliti kostüüm`{: class = "block3looks"} alguses `kui sprite klõpsatakse`{: class = "block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas

+ lüliti kostüümi (nano-a v)
küsige [Mis su nimi on?] ja oodake
```

![Kostüümi fikseerimise testimine](images/chatbot-costume-fix-test.png)

\--- / ülesanne \---