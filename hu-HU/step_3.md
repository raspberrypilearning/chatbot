## Beszélő chatbot

Most, hogy van egy személyiséggel rendelkező chatbotod, készítünk egy programot, hogy beszélni tudjon veled.

\--- task \---

Kattints a chatbot szereplőre, és add hozzá ezt a kódot, hogy `ha rákattint az`{:class="block3events"}, `megkérdezi a nevedet`{:class="block3sensing"}, majd `azt mondja: "Milyen kedves név!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ha ez a szellem a kattintott
kérni [Mi a neved?], és várjon
mondják [Milyen kedves név!] A (2) másodpercig
```

\--- /task \---

\--- task \---

A kód teszteléséhez kattints a chatbotodra. Amikor a chatbot megkérdezi a nevét, írd be a színpad alján látható mezőbe, majd kattints a kék jelre, vagy nyomd meg a <kbd>Enter</kbd>-t.

![Chatbot válasz tesztelése](images/chatbot-ask-test1.png)

![Chatbot válasz tesztelése](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Most, a chatbot azt mondja, hogy "Milyen kedves név!" minden alkalommal, amikor válaszolsz a kérdésére. A chatbot válaszát személyesebbé teheted azzal, hogy a válasza minden alkalommal más legyen, amikor beírsz egy új nevet.

Változtasd meg a chatbot szereplő kódját úgy, hogy `összefűzze`{:class="block3operators"} a "Szia"-t a "Mi a neved?" kérdésre adott `válasz`{:class="block3sensing"}oddal, a kód így fog kinéz:

![nano sprite](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
kérdezd [Mi a neved?] és várj
mondd: ([Szia ] és (válasz) összefűzve :: +) (2) másodpercig
```

![Testreszabott válasz tesztelése](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

A választ egy **változó**ban tárolva, azt bárhol felhasználhatod a projektben.

Hozz létre egy úgy változót, a neve legyen: `név`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Most változtasd meg a chatbot szereplő kódját úgy, hogy a `név`{:class="block3variables"} változót állítsa a `válasz`{:class="block3sensing"}ra:

![nano sprite](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
kérdezd [Mi a neved?] és várj
[név v] legyen (válasz)
mondd: ([Szia ] és (név :: + variables) összefűzve) (2) másodpercig
```

A kódnak úgy kell működnie, mint korábban: a chatbotnak köszönéskor használnia kell a beírt nevet.

![Testreszabott válasz tesztelése](images/chatbot-answer-test.png)

\--- /task \---

Teszteld a programot megint. Figyeld meg, hogy a beírt válasz a `név`{:class="block3variables"} változóban tárolódik, és megjelenik a színpad bal felső sarkában is. Annak érdekében, hogy a `név`{:class="block3variables"} eltűnjön a színpadról, menj a `Változók`{:class="block3variables"} blokkba és vedd le a pipát a <0>név</0>{:class="block3variables"} változóról.