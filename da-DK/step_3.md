## En snakende chatbot

Nu hvor du har en chatbot med en personlighed, skal du programmere det for at tale med dig.

\--- task \---

Klik på din chatbot sprite, og tilføj denne kode til den, så `når den klikkes`{: class = "block3events"}, beder den `om dit navn`{: class = "block3sensing"} og derefter siger `"Hvad en dejligt navn! "`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
når denne sprite klikket
spørg [Hvad er dit navn?] og vent
sige [Hvilket dejligt navn!] for (2) sekunder
```

\--- /task \---

\--- task \---

Klik på din chatbot for at teste din kode. Når chatbot beder om dit navn, skal du skrive det i feltet, der vises nederst i scenen, og derefter klikke på det blå mærke eller trykke på <kbd>Enter</kbd>.

![Testning af et ChatBot-svar](images/chatbot-ask-test1.png)

![Testning af et ChatBot-svar](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Lige nu svarer din chatbot "Hvilket dejligt navn!" hver gang du svarer. Du kan gøre chatbots svar mere personlige, så svaret er anderledes hver gang et andet navn indtastes.

Skift chatbot sprite kode til `tilslutte`{: class = "block3operators"} "Hej" med `svaret`{: class = "block3sensing"} til "Hvad er dit navn?" spørgsmål, så koden ser sådan ud:

![nano sprite](images/nano-sprite.png)

```blocks3
når denne sprite klikket
spørg [Hvad er dit navn?] og vent
sige (join [Hi] (svar) :: +) for (2) sekunder
```

![Afprøvning af et personligt svar](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Ved at gemme svaret i en **variabel**, kan du bruge det overalt dit projekt.

Opret en ny variabel kaldet `navn`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Skift nu din chatbot sprites kode til at indstille `navn`{: class = "block3variables"} variabel til `svar`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
Når denne sprite klikker
spørg [Hvad er dit navn?] og vent

+ sæt [navn v] til (svar)
siger (join [Hi] (navn :: variabler +)) for (2) sekunder
```

Din kode skal fungere som før: din chatbot skal sige hej ved at bruge det navn, du indtaster.

![Afprøvning af et personligt svar](images/chatbot-answer-test.png)

\--- /task \---

Test dit program igen. Bemærk, at svaret du indtaster gemmes i variablen `navn`{: class = "block3variables"}, og vises også øverst til venstre i scenen. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.