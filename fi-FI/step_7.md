## Sijainnin muuttaminen

Voit myös ohjelmoida chatbotin muuttamaan sen sijaintia!

![Muuttuvan taustan testaus](images/chatbot-backdrop-moon.png)

\--- tehtävä \---

Voitteko ohjelmoida chatbotin kysyä "Haluatko mennä kuuhun" ja muuttaa taustaa, kun vastaus on "kyllä"?

\--- vinkkejä \---

\--- vihje \---

Oman chatbot pitäisi `kysyä "Haluatko mennä kuuhun?"`{: class = "block3sensing"}, ja `, jos`{: class = "block3control"}, jos `vastauksen`{: class = "block3sensing"} "kyllä", se on `vaihtaa taustan kuun`{: class = "block3looks"}.

\--- / vihje \---

\--- vihje \---

Tässä on koodilohkot, jotka sinun täytyy lisätä chatbot-koodiin.

![nano sprite](images/nano-sprite.png)

```blocks3
kytke taustakuva (kuu v)

kysy [Haluatko mennä kuuhun?] ja odota

jos <(vastaus) = [yes]> ja 

loppua
```

\--- / vihje \---

\--- vihje \---

Tämän pitäisi näyttää koodissa:

```blocks3
kysy [Haluatko mennä kuuhun?] ja odota
jos <(vastaus) = [yes]> ja 
  kytkin taaksepäin (kuu v)
loppuun
```

\--- / vihje \---

\--- / vinkkejä \---

\--- / tehtävä \---

\--- tehtävä \---

Nyt sinun täytyy varmistaa, että chatbot alkaa oikeassa paikassa, kun napsautat sitä keskustelemaan sen kanssa. Lisää tämä lohko chatbot-koodisi yläosaan:

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti

+ vaihtaa taustakuvaksi (tila v)
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa ohjelmasi ja vastaa "kyllä", kun chatbot kysyy, haluatko mennä kuuhun. Sinun pitäisi nähdä, että chatbotin sijainti muuttuu.

\--- / tehtävä \---

\--- tehtävä \---

Voit myös lisätä seuraavan koodin uuden `jos`{: class = "block3control"} estää chatbotin hyppäämään ylös ja alas neljä kertaa, jos vastaat "kyllä":

![nano sprite](images/nano-sprite.png)

```blocks3
jos <(vastaus) = [yes]> ja 
  kytkin taaksepäin (kuu v)

+ toisto (4) 
    muutos y: llä (10)
    odota (0,1) sekuntia
    muutos y: llä (-10)
    odota (0,1) sekuntia
  pään
pää
```

\--- / tehtävä \---