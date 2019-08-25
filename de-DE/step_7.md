## Ortswechsel

You can also program your chatbot to change its location!

![Ein Bühnenbild wechseln und ausprobieren](images/chatbot-backdrop-moon.png)

\--- task \---

Can you program your chatbot to ask "Do you want to go to the moon", and then change the backdrop when the answer is "yes"?

\--- hinweise \---

\--- hint \---

Your chatbot should `ask "Do you want to go to the moon?"`{:class="block3sensing"}, and `if`{:class="block3control"} you `answer`{:class="block3sensing"} "yes", it should `switch the backdrop to the moon`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Here are the code blocks you need to add to your chatbot code.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Jetzt musst du sicherstellen, dass dein Chatbot am richtigen Ort ist, wenn du darauf klickst, um mit ihm zu sprechen. Füge diesen Block oben in deinem Chatbot-Code ein:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Teste dein Programm, und antworte "ja", wenn der Chatbot fragt, ob du zum Mond willst. Du solltest sehen, dass sich der Standort des Chatbot verändert.

\--- /task \---

\--- task \---

Du kannst auch den folgenden Code in den neuen `if`{:class="block3control"} Block hinzufügen, um deinen Chatbot vier Mal auf- und abspringen zu lassen, wenn du mit "ja" antwortest:

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [ja]> then 
  switch backdrop to (moon v)

+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

\--- /task \---