## Locatie wijzigen

Je kunt je chatbot ook programmeren om de locatie te wijzigen!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

Kun je je chatbot programmeren om "Ik ga naar de maan, ga je mee?" te vragen en dan de achtergrond te veranderen wanneer het antwoord "ja" is?

\--- hints \---

\--- hint \---

Je chatbot zou moeten `vragen "Ik ga naar de maan. Ga je mee?"`{:class="block3sensing"}, en `als`{:class="block3control"} je `antwoord`{:class="block3sensing"} "ja" is, moet `de achtergrond veranderen in de maan`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Hier zijn de code blokken die je moet toevoegen aan je chatbot code.

![nano sprite](images/nano-sprite.png)

```blocks3
verander achtergrond naar (moon v) :: looks

vraag [Ik ga naar de maan. Ga je mee?] en wacht :: sensing

als <(antwoord :: sensing) = [ja] :: operators> dan :: control
end
```

\--- /hint \---

\--- hint \---

Dit is hoe je code eruit zou moeten zien:

```blocks3
vraag [Ik ga naar de maan. Ga je mee?] en wacht :: sensing
als <(antwoord :: sensing) = [ja] :: operators> dan 
  verander achtergrond naar (moon v) :: looks :: control
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \----

Nu moet je ervoor zorgen dat je chatbot op de juiste locatie start als je erop klikt om ermee te praten. Voeg dit blok toe aan de bovenkant van uw chatbot-code:

![nano sprite](images/nano-sprite.png)

```blocks3
wanneer op deze sprite wordt geklikt :: events

verander achtergrond naar (spatiebalk v) :: looks
```

\--- /task \---

\--- task \---

Test je programma en beantwoord "ja" wanneer de chatbot vraagt of je naar de maan wilt gaan. Je zou moeten zien dat de locatie van de chatbot verandert.

\--- /task \---

\--- task \----

U kunt ook de volgende code toevoegen binnen de nieuwe `als`{:class="block3control"} blok om de chatbot vier keer op en neer te laten springen als je "ja" antwoordt:

![nano sprite](images/nano-sprite.png)

```blocks3
als <(antwoord :: sensing) = [ja] :: operators> dan 
  verander achtergrond naar (moon v) :: looks
  herhaal (4) keer 
    verander y met (10) :: motion
    wacht (0.1) sec. :: control
    verander y met (-10) :: motion
    wacht (0.1) sec. :: control :: control
  end :: control
end
```

\--- /task \---