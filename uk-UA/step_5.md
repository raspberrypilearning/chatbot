## Прийняття рішень

Ти можеш запрограмувати свого чат-бота, щоб він вирішував що робити на основі відповідей, які отримує.

Спочатку, ти запрограмуєш свого чат-бота задавати питання, на яке можна відповісти "так" або "ні".

\--- task \---

Зміни код свого чат-бота. Твій чат-бот має запитувати "В тебе все гаразд, <ім’я>", використовуючи змінну `ім’я`{:class="block3variables"}. Далі він має відповісти "Чудово!", `якщо`{:class="block3control"} отримує відповідь "так", і нічого не казати, якщо відповідь "ні".

![Testing a chatbot reply](images/chatbot-if-test1-annotated.png)

![Testing a chatbot reply](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

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

Наразі твій чат-бот нічого не каже після відповіді "ні".

\--- task \---

Зміни код свого чат-бота так, щоб він відповідав "О ні!", якщо отримує відповідь "ні" на питання "В тебе все гаразд, <ім’я>".

Заміни блок `якщо, то`{:class="block3control"} на блок `якщо, то, інакше`{:class="block3control"} і додай код, щоб чат-бот міг `говорити "О ні!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

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

![Testing a chatbot reply](images/chatbot-if-test2.png)

![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- /task \---

You can put any code inside an `if, then, else`{:class="block3control"} block, not just code to make your chatbot speak!

If you click your chatbot's **Costumes** tab, you'll see that there is more than one costume.

![chatbot costumes](images/chatbot-costume-view-annotated.png)

\--- task \---

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Testing a changing costume](images/chatbot-costume-test1.png)

![Testing a changing costume](images/chatbot-costume-test2.png)

Change the code inside the `if, then, else`{:class="block3control"} block to `switch costume`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

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

Test and save your code. You should see your chatbot's face change depending on your answer.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Costume bug](images/chatbot-costume-bug-test.png)

\--- task \---

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- /task \---