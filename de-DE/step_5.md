## Entscheidungen treffen

Du kannst deinen Chatbot so programmieren, dass er basierend auf den erhaltenen Antworten entscheidet, was zu tun ist.

Zuerst lässt du deinen Chatbot eine Frage stellen, die mit "Ja" oder "Nein" beantwortet werden kann.

\--- task \---

Ändere den Code deines Chatbots. Dein Chatbot sollte die Frage "Geht's dir gut, Name?, und dabei die `name ` {: class = "block3variables"}-Variable verwenden. Dann sollte er "Das freut mich!" antworten, `wenn`{:class="block3control"} die Antwort, die er bekommt "ja" ist, aber nichts sagen, wenn die Antwort "nein" ist.

![Eine ChatBot-Antwort ausprobieren](images/chatbot-if-test1-annotated.png)

![Eine ChatBot-Antwort ausprobieren](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Wie heißt du?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Geht's dir gut ] (name)) and wait
+if <(answer) = [ja]> then 
  say [Das freut mich!] for (2) seconds
end
```

Um deinen neuen Code korrekt zu testen, solltest Du ihn **zweimal** ausprobieren, einmal mit der Antwort "ja" und einmal mit "nein".

\--- /task \---

Im Moment sagt dein Chatbot nichts, wenn die Antwort "nein" ist.

\--- task \---

Ändere den Code deines Chatbots so, dass er "Oh nein!" antwortet, wenn er "nein" als Antwort auf "Gehts dir gut, name" erhält.

Replace the `if, then`{:class="block3control"} block with an `if, then, else`{:class="block3control"} block, and include code so the chatbot can `say "Oh no!"`{:class="block3looks"}.

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

Test your code. You should get a different response when you answer "no" and when you answer "yes": your chatbot should reply with "That’s great to hear!" when you answer "yes" (which is not case-sensitive), and reply with "Oh no!" when you answer **anything else**.

![Eine ChatBot-Antwort ausprobieren](images/chatbot-if-test2.png)

![Eine Ja/Nein-Antwort ausprobieren](images/chatbot-if-else-test.png)

\--- /task \---

You can put any code inside an `if, then, else`{:class="block3control"} block, not just code to make your chatbot speak!

If you click your chatbot's **Costumes** tab, you'll see that there is more than one costume.

![Chatbot Kostüme](images/chatbot-costume-view-annotated.png)

\--- task \---

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Ein Kostüm wechseln und ausprobieren](images/chatbot-costume-test1.png)

![Ein Kostüm wechseln und ausprobieren](images/chatbot-costume-test2.png)

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

![Kostüm-Fehler](images/chatbot-costume-bug-test.png)

\--- task \---

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Ein anderes Kostüm testen](images/chatbot-costume-fix-test.png)

\--- /task \---