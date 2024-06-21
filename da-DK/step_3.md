## En snakkende chatbot

Nu hvor du har en chatbot med en personlighed, skal du programmere det til at tale med dig.

\--- task \---

Klik på din chatbot-sprite, og tilføj denne kode til den, så `når der klikkes`{: class = "block3events"}, beder den `om dit navn`{: class = "block3sensing"} og derefter siger `"Sikke et dejligt navn! "`{: class = "block3looks"}.

![nano-sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

\--- /task \---

\--- task \---

Klik på din chatbot for at teste din kode. Når den beder om dit navn, skal du skrive det i feltet, der vises nederst på skærmen, og derefter klikke på det blå mærke eller trykke på <kbd>Enter</kbd>.

![Test af et ChatBot-svar](images/chatbot-ask-test1.png)

![Test af et ChatBot-svar](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Lige nu svarer din chatbot "Det er et dejligt navn!" hver gang du svarer. Du kan gøre chatbots svar mere personlige, så svaret er anderledes hver gang et andet navn indtastes.

Skift chatbot-sprite koden til `tilslutte`{: class = "block3operators"} "Hej" med `svaret`{: class = "block3sensing"} til "Hvad er dit navn?" spørgsmål, så koden ser sådan ud:

![nano-sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ say (join [Hi ] (answer) ) for (2) seconds
```

![Test af et personlig svar](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Ved at gemme svaret i en **variabel**kan du bruge det overalt i dit projekt.

Opret en ny variabel kaldet `navn`{:class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Skift nu din chatbot-sprites kode til at sætte `navn`{: class = "block3variables"} variabel til `svar`{: class = "block3sensing"}:

![nano-sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
+ say (join [Hi ] (name)) for (2) seconds
```

Din kode skal fungere som før: din chatbot skal sige hej ved at bruge det navn, du indtaster.

![Test af et personlig svar](images/chatbot-answer-test.png)

\--- /task \---

Test dit program igen. Bemærk, at svaret du indtaster gemmes i variablen `navn`{: class = "block3variables"}, og vises også øverst til venstre i scenen. Gå til `Variablerne` for at få det til at forsvinde fra scenen </code> {: class = "block3variables"} bloksektionen og klik på boksen ved siden af  navn </0> {:class = "block3variables"}, så det ikke er markeret.</p>