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

Тренутно твој робот одговара са "Какво дивно име!" сваки пут када одговориш. Можеш да прилагодиш његов одговор, тако да је одговор другачији сваки пут када се унесе друго име.

Промени код лика робота у `споји`{:class="block3operators"} "Здраво" са `одговор`{:class="block3sensing"} на питање "Како се зовеш?", тако да код изгледа овако:

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
изговори (споји [Здраво ] и (одговор) :: +) током (2) секунде
```

![Испробавање прилагођеног одговора](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Чувањем одговора у **променљивој**, можете га користити било где у пројекту.

Креирај нову променљиву која ће се звати `име`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Сада промени код робота да поставиш променљиву `име`{:class="block3variables"} у `одговор`{:class="block3sensing"}:

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај

+ нека [име v] буде (одговор)
изговори (споји [Здраво ] и (име :: + variables)) током (2) секунде
```

Твој код би требао да ради као и пре: твој робот би требао да каже здраво користећи твоје име.

![Испробавање прилагођеног одговора](images/chatbot-answer-test.png)

\--- /task \---

Поново испробај свој програм. Приметићеш да се твој одговор чува у променљивој `име`{:class="block3variables"}, а и да се приказује у горњем левом углу Позорнице. Да нестане са Позорнице, иди на одељак `Променљиве`{:class="block3variables"} и кликни на коцку до `име`{:class="block3variables"} тако да није обележена.