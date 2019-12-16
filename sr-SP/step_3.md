## Робот који разговара

Now that you have a chatbot with a personality, you're going to program it to talk to you.

\--- task \---

Click on your chatbot sprite, and add this code to it so that `when it's clicked`{:class="block3events"}, it `asks for your name`{:class="block3sensing"} and then `says "What a lovely name!"`{:class="block3looks"}.

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
изговори [Какво дивно име!] током (2) секунде
```

\--- /task \---

\--- task \---

Click on your chatbot to test your code. When the chatbot ask for your name, type it into the box that appears at the bottom of the Stage, and then click on the blue mark, or press <kbd>Enter</kbd>.

![Испробавање роботовог одговора](images/chatbot-ask-test1.png)

![Испробавање роботовог одговора](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Right now, your chatbot replies "What a lovely name!" every time you answer. You can make the chatbot’s reply more personal, so that the reply is different every time a different name is typed in.

Change the chatbot sprite’s code to `join`{:class="block3operators"} "Hi" with the `answer`{:class="block3sensing"} to the "What's your name?" question, so that the code looks like this:

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
изговори (споји [Здраво ] и (одговор) :: +) током (2) секунде
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Чувањем одговора у **променљивој**, можете га користити било где у пројекту.

Креирај нову променљиву која ће се звати `име`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Now, change your chatbot sprites’s code to set the `name`{:class="block3variables"} variable to `answer`{:class="block3sensing"}:

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај

+ нека [име v] буде (одговор)
изговори (споји [Здраво ] и (име :: + variables)) током (2) секунде
```

Your code should work as before: your chatbot should say hi using the name you type in.

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

Поново испробај свој програм. Notice that the answer you type in is stored in the `name`{:class="block3variables"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.