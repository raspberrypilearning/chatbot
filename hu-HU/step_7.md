## Hely megváltoztatása

Állítsd be a chatbotot úgy, hogy megváltoztassa a helyét!

![Változó hátteret tesztel](images/chatbot-backdrop-moon.png)

\--- task \---

Tudod úgy módosítani a chatbotodat, hogy megkérdezze: "Akarsz menni a Holdra?", majd módosítsa a hátteret, ha a válasz "igen"?

\--- tippek \---

\--- hint \---

A chatbotnak `meg kell kérdeznie: "El akarsz menni a Holdra?"`{:class="block3sensing"}, és `ha`{:class="block3control"} a `válasz`{:class="block3sensing"} "igen", akkor `kapcsolja át a hátteret a Holdra`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Ezeket a kódblokkokat kell hozzáadnod a chatbot kódjához.

![nano sprite](images/nano-sprite.png)

```blocks3
háttér legyen (moon v)

kérdezd [Akarsz menni a Holdra?] és várj

ha <(válasz) = [igen]> akkor
end
```

\--- /hint \---

\--- hint \---

A kódnak így kell kinéznie:

```blocks3
kérdezd meg [Szeretnéd a Holdra menni?] és várjunk
> ha <(válasz) = [yes]> majd 
  kapcsolót hátra (hold v)
vége
```

\--- /hint \---

\--- / tippek \---

\--- /task \---

\--- task \---

Most meg kell győződnie arról, hogy a chatbot a megfelelő helyen kezdődik, amikor rákattint, hogy beszéljen vele. A blokk hozzáadása a chatbot kódjának tetejére:

![nano sprite](images/nano-sprite.png)

```blocks3
amikor ez a sprite

+ + kapcsoló hátteret (tér v)
```

\--- /task \---

\--- task \---

Tesztelje a programot, és válaszoljon "igen" -re, ha a chatbot megkérdezi, hogy akar-e menni a Holdra. Látnia kell, hogy a chatbot helyszíne megváltozik.

\--- /task \---

\--- task \---

A következő kódot is beillesztheti az új `ha`{: class = "block3control"} blokkolja a chatbot négyszer ugrását, ha válaszol az "igen":

![nano sprite](images/nano-sprite.png)

```blocks3
ha <(válasz) = [yes]> majd 
  kapcsoló háttere (hold v)

+ ismétlés (4) 
    változtatás y -val (10)
    várakozás (0,1) másodperc
    változtatás y -val (-10)
    várakozás (0,1) másodperc
  vég
vége
```

\--- /task \---