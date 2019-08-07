## Robot koji govori

Sad kada imaš robota s osobnošću, programirat ćemo ga da razgovara s tobom.

\--- task \---

Kliknite na lika chatbota i dodaj mu ovaj kôd tako da, `kada klikneš na njega`{:class="block3events"}, pita za `tvoje ime`{:class="block3sensing"}, a zatim `kaže "Imaš lijepo ime!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
Kada je lik kliknut
pitaj [Kako se zoveš?] i čekaj
govori [Imaš lijepo ime!] (2) sekundi
```

\--- /task \---

\--- task \---

Klikni na svog chatbota i testiraj kôd. Kad chatbot zatraži tvoje ime, upiši ga u okvir koji se pojavi na dnu Pozornice, a zatim klikni na plavu kvačicu ili pritisni <kbd>Enter</kbd>.

![Testiranje robotova odgovora](images/chatbot-ask-test1.png)

![Testiranje robotova odgovora](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Trenutačno tvoj chatbot odgovara „Imaš lijepo ime!” svaki put kad odgovoriš. Odgovor chatbota možeš učiniti osobnijim, tako da je odgovor različit svaki put kada se unese drugo ime.

Change the chatbot sprite’s code to `join`{:class="block3operators"} "Hi" with the `answer`{:class="block3sensing"} to the "What's your name?" question, so that the code looks like this:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![Testiranje prilagođenog odgovora](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

By storing the answer in a **variable**, you can use it anywhere your project.

Create a new variable called `name`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Now, change your chatbot sprites’s code to set the `name`{:class="block3variables"} variable to `answer`{:class="block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

Your code should work as before: your chatbot should say hi using the name you type in.

![Testiranje prilagođenog odgovora](images/chatbot-answer-test.png)

\--- /task \---

Test your program again. Notice that the answer you type in is stored in the `name`{:class="block3variables"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Data`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.