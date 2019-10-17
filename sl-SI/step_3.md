## Govoreči klepetalni robot

Sedaj ko imaš klepetalnega robota z osebnostjo, ga boš sprogramiral-a, da se bo pogovarjal s tabo.

\--- task \---

Klikni na figuro klepetalnega robota in dodaj to kodo, tako da `ko kliknemo to figuro`{: class = "block3events"}, `vpraša za vaše ime`{: class = "block3sensing"} in nato `reče: "Kako lepo ime! "`{: class = "block3looks"}.

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj
reci [Kako lepo ime!] za (2) sekund
```

\--- /task \---

\--- task \---

Klikni na svojega klepetalnega robota, da preizkusiš kodo. Ko te vpraša za ime, ga vnesi v polje, ki se pojavi na dnu odra in nato klikni modro oznako ali pritisni <kbd>Enter</kbd>.

![Testiranje odziva klepetalnega robota](images/chatbot-ask-test1.png)

![Testiranje odziva klepetalnega robota](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Za zdaj tvoj klepetalni robot odgovori: "Kako ljubko ime!", vsakič, ko odgovoriš. Odgovor robota lahko narediš bolj osebnega, tako da bo odgovor drugačen vsakič, ko bo vnešeno drugo ime.

Spremeni kodo figure klepetalnega robota, tako da `združi`{: class="block3operators"} "Živjo" z `odgovorom`{: class="block3sensing"} na vprašanje: "Kako ti je ime?". Koda mora izgledati takole:

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj
reci (združi [Živjo, ] (odgovor) :: +) za (2) sekund
```

![Testiranje personaliziranega odgovora](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Ko shraniš odgovor v **spremenljivko**, ga lahko uporabiš kjerkoli v svojem projektu.

Ustvari novo spremenljivko, ki se bo imenovala `ime`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Sedaj spremeni kodo za figuro klepetalnega robota, tako da nastavi spremenljivko `ime`{: class = "block3variables"} na `odgovor`{: class = "block3sensing"}:

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro
vprašaj [Kako ti je ime?] in počakaj

+ nastavi [ime v] na (odgovor)
reci (združi [Živijo, ] (ime :: spremenljivke +)) za (2) sekund
```

Tvoja koda bi morala delovati tako kot prej: tvoj klepetalni robot bi moral reči "Živijo, " in ime, ki si ga vnesel.

![Testiranje personaliziranega odgovora](images/chatbot-answer-test.png)

\--- /task \---

Ponovno preizkusi program. Pomni, da je odgovor, ki si ga vnesel, shranjen v spremenljivki `ime`{: class = "block3variables"} in je prikazan tudi v zgornjem levem kotu odra. Če želiš, da izgine iz odra, pojdi v razdelek `Spremenljivke`{: class = "block3variables"} in klikni na polje poleg spremenljivke `ime`{: class = "block3variables"}, tako da ni več označeno.