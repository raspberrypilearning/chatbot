## Hely megváltoztatása

Állítsd be a chatbotot úgy, hogy megváltoztassa a helyét!

![Változó háttér tesztelése](images/chatbot-backdrop-moon.png)

\--- task \---

Tudod úgy módosítani a chatbotodat, hogy megkérdezze: "Akarsz menni a Holdra?", majd módosítsa a hátteret, ha a válasz "igen"?

\--- tippek \---

\--- hint \---

A chatbotnak `meg kell kérdeznie: "El akarsz menni a Holdra?"`{:class="block3sensing"}, és `ha`{:class="block3control"} a `válasz`{:class="block3sensing"} "igen", akkor `kapcsolja át a hátteret a Holdra`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Ezeket a kódblokkokat kell hozzáadnod a chatbot kódjához.

![nano jelmez](images/nano-sprite.png)

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
kérdezd [Akarsz menni a Holdra?] és várj
ha <(válasz) = [igen]> akkor 
  háttér legyen (moon v)
end
```

\--- /hint \---

\--- / tippek \---

\--- /task \---

\--- task \---

Most meg kell győződnöd arról, hogy a chatbot a megfelelő helyen van, amikor rákattintasz, hogy beszélj vele. Add hozzá ezt blokkot a chatbot kódjának tetejéhez:

![nano jelmez](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
háttér legyen (space v)
```

\--- /task \---

\--- task \---

Próbáld ki a programot, és válaszolj "igen"-nel, ha a chatbot megkérdezi, hogy akarsz-e menni a Holdra. Látnod kell, hogy a chatbot helyszíne megváltozik.

\--- /task \---

\--- task \---

A következő kódot is beillesztheted az új `ha`{:class="block3control"} blokkolba, hogy a chatbot ugráljon, ha a válaszod az "igen":

![nano jelmez](images/nano-sprite.png)

```blocks3
ha <(válasz) = [igen]> akkor 
  háttér legyen (moon v)
  ismételd (4) 
    y változzon (10)
    várj (0.1) mp-et
    y változzon (-10)
    várj (0.1) mp-et
  end
end
```

\--- /task \---