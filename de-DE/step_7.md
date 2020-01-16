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
wechsle zu Hintergrund (moon v)

frage [Möchtest du zum Mond fliegen?] und warte

wenn <(Antwort) = [ja]> dann 

end
```

\--- /hint \---

\--- hint \---

So sollte dein Code aussehen:

```blocks3
frage [Möchtest du zum Mond fliegen?] und warte
wenn <(Antwort) = [ja]> dann 
  wechsle zu Hintergrund (moon v)
end
```

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Jetzt musst du sicherstellen, dass dein Chatbot am richtigen Ort ist, wenn du darauf klickst, um mit ihm zu sprechen. Füge diesen Block oben in deinem Chatbot-Code ein:

![nano sprite](images/nano-sprite.png)

```blocks3
wenn diese Figur angeklickt wird

+ wechsle zu Hintergrund (space v)
```

\--- /task \---

\--- task \---

Teste dein Programm, und antworte "ja", wenn der Chatbot fragt, ob du zum Mond willst. Du solltest sehen, dass sich der Standort des Chatbot verändert.

\--- /task \---

\--- task \---

Du kannst auch den folgenden Code in den neuen `if`{:class="block3control"} Block hinzufügen, um deinen Chatbot vier Mal auf- und abspringen zu lassen, wenn du mit "ja" antwortest:

![nano sprite](images/nano-sprite.png)

```blocks3
wenn <(Antwort) = [ja]> dann 
  wechsle zu Hintergurnd (moon v)

+  wiederhole (4) 
    verändere y um (10)
    warte (0.1) Sekunden
    verändere y um (-10)
    warte (0.1) Sekunden
  end
end
```

\--- /task \---