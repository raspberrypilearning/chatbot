## Pogovorni klepet

Zdaj, ko imate chatbot z osebnostjo, ga boste programirali, da se pogovori z vami.

\--- naloga \---

Kliknite na chatbot sprite in dodajte to kodo, tako da `ko je kliknila`{: class = "block3events"}, `vpraša za vaše ime`{: class = "block3sensing"} in nato `pravi: "Kaj lepo ime! "`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj
besedo [kako lepo ime!] za (2) sekund
```

\--- / naloga \---

\--- naloga \---

Kliknite svojo chatbot, da preizkusite svojo kodo. Ko chatbot zahteva vaše ime, ga vnesite v polje, ki se prikaže na dnu stopnje, nato pa kliknite modro oznako ali pritisnite <kbd>Enter</kbd>.

![Testiranje ChatBot odziva](images/chatbot-ask-test1.png)

![Testiranje ChatBot odziva](images/chatbot-ask-test2.png)

\--- / naloga \---

\--- naloga \---

Zdaj, vaš chatbot odgovori "Kako lepo ime!" vsakič, ko odgovorite. Odgovor klepetalnice lahko naredite bolj oseben, tako da bo odgovor drugačen vsakič, ko bo vneseno drugo ime.

Spremenite kodo chatbotovega spritea na `pridružite`{: class = "block3operators"} "Hi" z `odgovorom`{: class = "block3sensing"} na "Kako je vaše ime?" vprašanje, tako da koda izgleda takole:

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj
recimo (pridruži se [Hi] (odgovor) :: +) za (2) sekund
```

![Testiranje prilagojenega odgovora](images/chatbot-answer-test.png)

\--- / naloga \---

\--- naloga \---

S shranjevanjem odgovor v **spremenljivke**, ga lahko uporabljate kjerkoli svoj projekt.

Ustvarite novo spremenljivko z imenom `name`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- / naloga \---

\--- naloga \---

Sedaj spremenite kodo za chatbot sprites, da nastavite `ime`{: class = "block3variables"} spremenljivko na `odgovor`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
ko je ta geslo kliknilo
vprašaj [kako ti je ime?] in počakaj

+ nastavite [ime v] na (odgovor)
reci (pridruži se [Hi] (ime :: spremenljivke +)) za (2) sekund
```

Vaša koda bi morala delovati tako kot prej: vaš klepet bi moral pozdraviti ime, ki ga vnesete.

![Testiranje prilagojenega odgovora](images/chatbot-answer-test.png)

\--- / naloga \---

Ponovno preizkusite program. Upoštevajte, da je odgovor, ki ga vnesete, shranjen v spremenljivki `name`{: class = "block3variables"} in je prikazan tudi v zgornjem levem kotu stopnje. Če želite, da izgine iz stopnje, pojdite v razdelek `Data`{: class = "block3variables"} in kliknite na polje poleg `ime`{: class = "block3variables"}, tako da ni označeno.