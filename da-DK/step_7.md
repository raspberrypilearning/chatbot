## Ændring af placering

Du kan også programmere din chatbot for at ændre sin placering!

![Tester en skiftende baggrund](images/chatbot-backdrop-moon.png)

\--- task \---

Kan du programmere din chatbot til at spørge "Vil du gå til månen", og derefter ændre baggrunden, når svaret er "ja"?

\--- Tips \---

\--- hint \---

Din chatbot skal `spørge "Vil du gå til månen?"`{: class = "block3sensing"}, og `hvis`{: class = "block3control"} du `svar`{: class = "block3sensing"} "ja", bør det `skifte kulisse til måne`{: class = "block3looks"}.

\--- / hint \---

\--- hint \---

Her er de kodeblokke, du skal føje til din chatbot-kode.

![nano sprite](images/nano-sprite.png)

```blocks3
skift baggrund til (måne v)

spørg [Vil du gå til månen?] og vente

hvis <(svar) = [yes]> derefter 

ende
```

\--- / hint \---

\--- hint \---

Sådan ser din kode ud:

```blocks3
spørg [Vil du gå til månen?] og vent
hvis <(svar) = [yes]> derefter 
  skift baggrund til (måne v)
ende
```

\--- / hint \---

\--- /Tips \---

\--- /task \---

\--- task \---

Nu skal du sørge for, at din chatbot starter på det rigtige sted, når du klikker på den for at tale med den. Tilføj denne blok til toppen af din chatbot-kode:

![nano sprite](images/nano-sprite.png)

```blocks3
da denne sprite klikket

+ skift baggrund til (plads v)
```

\--- /task \---

\--- task \---

Test dit program, og svar "ja", når chatbot spørger om du vil gå til månen. Du skal se, at chatbots placering ændres.

\--- /task \---

\--- task \---

Du kan også føje følgende kode inden for den nye `hvis`{: class = "block3control"} blokke for at få chatbot'en til at springe op og ned fire gange, hvis du svarer "ja":

![nano sprite](images/nano-sprite.png)

```blocks3
hvis <(svar) = [yes]> derefter 
  skift baggrund til (måne v)

+ gentag (4) 
    skift y ved (10)
    vent (0,1) secs
    skift y ved (-10)
    vent
  ende
ende
```

\--- /task \---