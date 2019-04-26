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

Change the chatbot sprite’s code to `join`{:class="block3operators"} "Hi" with the `answer`{:class="block3sensing"} to the "What's your name?" question, so that the code looks like this:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

By storing the answer in a **variable**, you can use it anywhere your project.

Create a new variable called `name`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \----

Now, change your chatbot sprites’s code to set the `name`{:class="block3variables"} variable to `answer`{:class="block3sensing"}:

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