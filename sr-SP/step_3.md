## Робот који разговара

Сада када имаш робота са личношћу, програмираћемо га да разговара са тобом.

\--- task \---

Кликни на лик робота, а затим му додај следећи код, тако да `када је кликнуто на овај лик`{:class="block3events"}, `пита како се зовеш`{:class="block3sensing"}, а затим `изговари "Какво дивно име!"`{:class="block3looks"}.

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
изговори [Какво дивно име!] током (2) секунде
```

\--- /task \---

\--- task \---

Кликни на робота да испробаш свој код. Када те робот упита за име, откуцај га у поље на дну Позорнице, а затим кликни на плаву ознаку или притисни тастер <kbd>Enter</kbd>.

![Испробавање роботовог одговора](images/chatbot-ask-test1.png)

![Испробавање роботовог одговора](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Right now, your chatbot replies "What a lovely name!" every time you answer. You can make the chatbot’s reply more personal, so that the reply is different every time a different name is typed in.

Промени код лика робота у `споји`{:class="block3operators"} "Здраво" са `одговор`{:class="block3sensing"} на питање "Како се зовеш?", тако да код изгледа овако:

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

Поново испробај свој програм. Приметићеш да се твој одговор чува у променљивој `име`{:class="block3variables"}, а и да се приказује у горњем левом углу Позорнице. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.