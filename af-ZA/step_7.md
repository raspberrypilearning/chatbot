## Ligging verander

U kan ook u chatbot program om sy ligging te verander!

![Toets 'n veranderende agtergrond](images/chatbot-backdrop-moon.png)

\--- taak \---

Kan jy jou chatbot programmeer om te vra "Wil jy na die maan gaan" en verander dan die agtergrond wanneer die antwoord "ja" is?

\--- wenke \---

\--- hint \---

Jou chatbot moet `vra "Wil jy na die maan gaan?"`{: class = "block3sensing"} en `as`{: class = "block3control"} jy `antwoord`{: class = "block3sensing"} "ja", moet dit `die agtergrond na die maan skuif`class = "block3looks"}.

\--- / hint \---

\--- hint \---

Hier is die kode blokke wat jy moet byvoeg by jou chatbot kode.

![nano sprite](images/nano-sprite.png)

```blocks3
verander agtergrond na (maan v)

vra [Wil jy na die maan gaan?] en wag

as <(antwoord) = [yes]> dan 

einde
```

\--- / hint \---

\--- hint \---

Dit is hoe jou kode lyk:

```blocks3
vra [Wil jy na die maan gaan?] en wag
as <(antwoord) = [yes]> dan 
  skakel agtergrond na (maan v)
einde
```

\--- / hint \---

\--- / wenke \---

\--- / taak \---

\--- taak \---

Nou moet jy seker maak dat jou chatbot op die regte plek begin wanneer jy daarop kliek om daarmee te praat. Voeg hierdie blokkie by die bokant van jou chatbot-kode:

![nano sprite](images/nano-sprite.png)

```blocks3
wanneer hierdie sprite

gekliek het, verander agtergrond na (spasie v)
```

\--- / taak \---

\--- taak \---

Toets jou program en beantwoord 'ja' wanneer die chatbot vra of jy na die maan wil gaan. Jy moet sien dat die chatbot se ligging verander.

\--- / taak \---

\--- taak \---

Jy kan ook die volgende kode in die nuwe `as`(: class = "block3control"} blokkeer om die chatbot vier keer op en af te laat spring as jy "ja" antwoord:

![nano sprite](images/nano-sprite.png)

```blocks3
as <(antwoord) = [yes]> dan 
  skakel agtergrond na (maan v)

+ herhaal (4) 
    verander y deur (10)
    wag (0.1) sekondes
    verander y deur (-10)
    wag (0.1) sekondes
  einde
einde
```

\--- / taak \---