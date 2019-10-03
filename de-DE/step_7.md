## Ortswechsel

Du kannst deinen Chatbot auch programmieren, damit er seinen Standort wechselt!

![Ein Bühnenbild wechseln und ausprobieren](images/chatbot-backdrop-moon.png)

\--- task \---

Kannst Du deinen Chatbot programmieren zu fragen: "Würdest du gerne zum Mond fliegen?" und dann den Standort ändern, wenn die Antwort "Ja" ist?

\--- hinweise \---

\--- hint \---

Dein Chatbot sollte `fragen: "Möchtest du zum Mond fliegen?"`{:class="block3sensing"}, und `wenn`{:class="block3control"} deine `Antwort`{:class="block3sensing"} "ja" ist, sollte derHintergrund zum Mond wechseln.`den Hintergrund auf den Mond wechseln`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke, die du deinem Chatbot-Code hinzufügst.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Möchtest du zum Mond fliegen?] and wait

if <(answer) = [ja]> then 

end
```

\--- /hint \---

\--- hint \---

So sollte dein Code aussehen:

```blocks3
ask [Möchtest du zum Mond fliegen?] and wait
if <(answer) = [ja]> then 
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