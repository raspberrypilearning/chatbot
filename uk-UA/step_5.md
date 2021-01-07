## Прийняття рішень

Ти можеш запрограмувати свого чат-бота, щоб він вирішував що робити на основі відповідей, які отримує.

Спочатку, ти запрограмуєш свого чат-бота задавати питання, на яке можна відповісти "так" або "ні".

\--- task \---

Зміни код свого чат-бота. Твій чат-бот має запитувати "В тебе все гаразд, <ім’я>", використовуючи змінну `ім’я`{:class="block3variables"}. Далі він має відповісти "Чудово!", `якщо`{:class="block3control"} отримує відповідь "так", і нічого не казати, якщо відповідь "ні".

![Тестування відповіді Чат-бота](images/chatbot-if-test1-annotated.png)

![Тестування відповіді Чат-бота](images/chatbot-if-test2.png)

![спрайт nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
end
```

Щоб правильно перевірити свій новий код, потрібно зробити це **двічі**: один раз з відповіддю "так" і один раз з відповіддю "ні".

\--- /task \---

At the moment, your chatbot doesn't say anything to the answer "no".

\--- task \---

Зміни код свого чат-бота так, щоб він відповідав "О ні!", якщо отримує відповідь "ні" на питання "В тебе все гаразд, <ім’я>".

Заміни блок `якщо, то`{:class="block3control"} на блок `якщо, то, інакше`{:class="block3control"} і додай код, щоб чат-бот міг `говорити "О ні!"`{:class="block3looks"}.

![спрайт nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
else 
+  say [Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

Перевір свій код. Ти маєш отримати різні репліки, коли ти відповідаєш "так" і "ні": твій чат-бот має відповідати "Чудово!", коли ти відповідаєш "так" (великими чи малими літерами), і відповідати "О ні!", коли ти даєш **будь-яку іншу** відповідь.

![Тестування відповіді Чат-бота](images/chatbot-if-test2.png)

![Тестування позитивної/негативної відповіді](images/chatbot-if-else-test.png)

\--- /task \---

Ти можеш помістити будь-який код всередину блоку `якщо, то, інакше`{:class="block3control"}, не лише код, щоб твій чат-бот розмовляв!

Якщо ти клацнеш на вкладку чат-бота **Образи**, то побачиш, що там більше одного образа.

![образи чат-бота](images/chatbot-costume-view-annotated.png)

\--- task \---

Зміни код чат-бота, щоб він змінював образи, коли ти ввів свою відповідь.

![Тестування зміни образу](images/chatbot-costume-test1.png)

![Тестування зміни образу](images/chatbot-costume-test2.png)

Зміни код всередині блока `якщо, то, інакше`{:class="block3control"}, щоб `змінити образ`{:class="block3looks"}.

![спрайт nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

Протестуй та збережи свій код. Ти маєш побачити, як обличчя твого чат-бота змінюється в залежності від твоєї відповіді.

\--- /task \---

Чи помітив (-ла) ти, що після того, як образ чат-бота змінюється, він таким залишається і не змінюється на той, яким був спочатку?

Можеш спробувати ось що: запусти свій код і дай відповідь "ні", щоб обличчя чат-бота стало сумним. Далі запусти свій код знову і зверни увагу, що твій чат-бот не стає знову радісним перед тим, як запитати твоє ім’я.

![Помилковий образ](images/chatbot-costume-bug-test.png)

\--- task \---

Щоб вирішити цю проблему, додай до коду чат-бота блок `змінити образ`{:class="block3looks"} на початку `коли спрайт натиснуто`{:class="block3events"}.

![спрайт nano](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Тестування виправлення образу](images/chatbot-costume-fix-test.png)

\--- /task \---