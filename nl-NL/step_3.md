## Een pratende chatbot

Nu dat je een chatbot met een persoonlijkheid hebt, ga je het programmeren om met je te praten.

\--- task \---

Klik op je chatbot sprite, en voeg deze code toe zodat `wanneer op deze sprite wordt geklikt`{:class="block3events"}, het `vraagt om je naam`{:class="block3sensing"} en vervolgens `zegt "Wat een mooie naam!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
wanneer op deze sprite wordt geklikt :: events
vraag [Wat is je naam?] en wacht :: sensing
zeg [Wat een mooie naam!] (2) sec. :: looks
```

\--- /task \---

\--- task \----

Klik op je chatbot om je code te testen. Wanneer de chatbot je naam vraagt, typ deze in het vak dat aan de onderkant van het speelveld verschijnt, en klik dan op de blauwe-witte V, of druk op <kbd>Enter</kbd>.

![Testing a ChatBot response](images/chatbot-ask-test1.png)

![Testing a ChatBot response](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \----

Op dit moment antwoordt je chatbot met "Wat een mooie naam!" elke keer dat je antwoordt. Je kunt het antwoord van de chatbot persoonlijker maken, zodat het antwoord anders is elke keer dat een andere naam wordt ingetypt.

Wijzig de code van de chatbot sprite in `voeg en samen`{:class="block3operators"} "Hallo" met het `antwoord` {:class = "block3sensing"} bij de "Wat is je naam?" vraag, zodat de code er zo uitziet:

![nano sprite](images/nano-sprite.png)

```blocks3
wanneer op deze sprite wordt geklikt :: events
vraag [Wat is je naam?] en wacht :: sensing
zeg (voeg [Hoi ] en (antwoord :: sensing) samen :: + operators) (2) sec. :: looks
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Door het antwoord op te slaan in een **variabele**, kunt je het overal gebruiken in je project.

Maak een nieuwe variabele met de naam `naam`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \----

Wijzig nu de code van je chatbot sprite door de `antwoord`{:class="block3variables"} variabele te veranderen in de `naam`{:Class="block3sensing"} variabele:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

Your code should work as before: your chatbot should say hi using the name you type in.

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

Test your program again. Notice that the answer you type in is stored in the `name`{:class="block3variables"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Data`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.