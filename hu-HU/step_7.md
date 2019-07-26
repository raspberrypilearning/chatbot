## Hely megváltoztatása

Beállíthatja a chatbotot is, hogy megváltoztassa a helyét!

![Változó hátteret tesztel](images/chatbot-backdrop-moon.png)

\--- task \---

Beállíthatod a chatbotodat, hogy megkérdezd: "Akarsz menni a Holdra", majd módosítsd a hátteret, amikor a válasz "igen"?

\--- tippek \---

\--- hint \---

Az Ön chatbotjának `kell kérdeznie: "El akarsz menni a Holdra?"`{: class = "block3sensing"}, és `ha`{: class = "block3control"} te `válasz`{: class = "block3sensing"} "igen", akkor `kapcsolja át a hátteret a holdra`{: class = "block3looks"}.

\--- /hint \---

\--- hint \---

Íme a kódblokkok, amelyeket hozzá kell adnod a chatbot kódodhoz.

![nano sprite](images/nano-sprite.png)

```blocks3
kapcsolja a hátteret (hold v)

kérje [Szeretne menni a Holdra?] és várjon

ha <(válasz) = [yes]> majd 

vége
```

\--- /hint \---

\--- hint \---

Ez az, amit a kódodnak kell kinéznie:

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