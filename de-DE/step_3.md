## Ein sprechender Chatbot

Jetzt, wo du einen Chatbot mit einer eigenen Persönlichkeit hast, lass' uns ihn so programmieren, dass er mit dir spricht.

--- task ---

Klicke auf deinen Chatbot-Sprite und füge diesen Code hinzu, sodass, `wenn darauf geklickt wird`{:class="block3events"}, er `nach deinem Namen fragt`{:class="block3sensing"} und dann `"Was für ein schöner Name!"` {:class="block3looks"} sagt.

![nano sprite](images/nano-sprite.png)

```blocks3
wenn die Figur angeklickt wird
frage [Wie heißt du?] und warte
sage [Was für ein schöner Name!] für (2) Sekunden
```

--- /task ---

--- task ---

Klicke auf deinen Chatbot, um deinen Code zu testen. Wenn der Chatbot nach deinem Namen fragt, schreibe ihn in das Feld unten auf der Bühne, und klicke dann auf das blaue Feld, oder drücke <kbd>Enter</kbd>.

![Eine ChatBot-Antwort ausprobieren](images/chatbot-ask-test1.png)

![Eine ChatBot-Antwort ausprobieren](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

Jetzt antwortet dein Chatbot "Was für ein schöner Name!" jedes Mal wenn du antwortest. Du kannst die Antwort des Chatbots persönlicher gestalten, sodass die Antwort jedes Mal anders ist, wenn ein anderer Name eingegeben wird.

Ändere den Sprite Codes des Chatbots auf `verbinde`{:class="block3operators"} "Hallo" mit der `Antwort`{:class="block3sensing"} zu der "Wie heißt du? - Frage, sodass der Code wie folgt aussieht:

![nano sprite](images/nano-sprite.png)

```blocks3
wenn die Figur angeklickt wird
frage [Wie heißt du?] und warte
sage (teilnehmen [Hallo] (Antwort) :: +) für (2) Sekunden
```

![Eine personalisierte Antwort ausprobieren](images/chatbot-answer-test.png)

--- /task ---

--- task ---

Wenn du die Antwort in einer **Variable** speicherst, kannst du sie überall in deinem Projekt verwenden.

Erstelle eine neue Variable gennant `Name`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Ändere den Chatbot Sprite Code nun, um die `Name`{:class="block3variables"} Variable auf die `Antwort` Variable {:class="block3sensing"} umzuändern:

![nano sprite](images/nano-sprite.png)

```blocks3
wenn die Figur angeklickt wird
frage [Wie heißt du?] und warte
+ setze [Name v] auf (Antwort)
sage (verbinde [Hallo] und (Antwort) :: +) für (2) Sekunden
```

Dein Code soll wie zuvor funktionieren: dein Chatbot soll dich mit Hallo und dem Namen, den du eingetippt hast, begrüßen.

![Eine personalisierte Antwort ausprobieren](images/chatbot-answer-test.png)

--- /task ---

Teste dein Programm erneut. Beachte, dass die Antwort die du eingibst, in der `Name`{:class="block3variables"} Variable gespeichert wird, und auch in der oberen linken Ecke der Bühne angezeigt wird. Um die Variable von der Bühne verschwinden zu lassen, gehe zum `Variablen`{:class="block3variables"} Block-Abschnitt und klicke auf die Box links neben `Name`{:class="block3variables"}, sodass die Variable nicht mehr markiert ist.