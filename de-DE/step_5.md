## Entscheidungen treffen

Du kannst deinen Chatbot dazu programmieren, aufgrund deiner Antworten auf seine Fragen zu entscheiden, was er sagt oder tut.

--- task ---

Kannst Du den Chatbot dazu programmieren, die Frage "Geht es dir gut?" zu stellen und dann mit "Das ist schön zu hören!" zurück zu antworten, aber nur **falls** die Antwort des Anwenders "ja" ist?

Um deinen neuen Code korrekt zu testen, solltest du ihn **zweimal** ausprobieren, einmal mit der Antwort "ja" und einmal mit "nein".

Dein Chatbot sollte antworten "Das ist schön zu hören!" wenn du "ja" antwortest, aber nichts sagen, wenn du "nein" antwortest.

![Eine ChatBot-Antwort ausprobieren](images/chatbot-if-test.png)

--- hints --- --- hint --- Nachdem dein Chatbot "Hi" gesagt hat, sollte er nun **fragen**: "Geht es dir gut?". **Falls** du mit "ja" antwortest, sollte der Chatbot "Das ist schön zu hören!" **sagen**. --- /hint --- --- hint --- Hier sind die zusätzlichen Code-Blöcke, die du brauchen wirst: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) --- /hint --- --- hint --- So sollte dein Code aussehen: ![Code for a chatbot reply](images/chatbot-if-code.png) --- /hint --- --- /hints ---

--- /task ---

--- task ---

Im Moment sagt dein Chatbot nichts, wenn du mit "nein" antwortest. Kannst du deinen Chatbot so verändern, dass er, wenn du seine Frage mit "nein" beantwortest, "Oh nein!" zurück antwortet?

Testen und speichern. Dein Chatbot sollte jetzt "Oh nein!" sagen wenn du mit "nein" antwortest. Er wird sogar dann "Oh nein!" sagen, wenn du irgendetwas anderes als "ja" antwortest. (Das **sonst** im `falls/sonst`-Block bedeutet **in allen anderen Fällen**).

![Eine Ja/Nein-Antwort ausprobieren](images/chatbot-if-else-test.png)

--- hints --- --- hint --- Dein Chatbot sollte jetzt sagen: "Das ist schön zu hören!" **falls** du mit "ja" antwortest, sollte aber "Oh nein!" sagen, falls du **sonst** etwas antwortest. --- /hint --- --- hint --- Hier sind die Code-Blöcke, die du brauchen wirst: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) --- /hint --- --- hint --- So sollte dein Code aussehen: ![Code for a yes/no reply](images/chatbot-if-else-code.png) --- /hint --- --- /hints ---

--- /task ---

--- task ---

Du kannst allen möglichen Code in einem `falls/sonst`-Block ablegen, nicht bloß Code, der deinen Chatbot sprechen lässt. Wenn du auf die Registerkarte **Kostüme** für die Figur deines Chatbots klickst, wirst du sehen, dass sie mehrere Kostüme hat.

![Chatbot Kostüme](images/chatbot-costume-view.png)

--- /task ---

--- task ---

Kannst du das Kostüm des Chatbots so anpassen, dass es zu deiner Antwort passt?

Testen und speichern. Du solltest sehen, dass sich das Gesicht deines Chatbots in Abhängigkeit von deiner Antwort verändert.

![Ein Kostüm wechseln und ausprobieren](images/chatbot-costume-test.png)

--- hints --- --- hint --- Dein Chatbot sollte jetzt zusätzlich je nach der gegebenen Antwort den Block **wechsle zu Kostüm** ausführen. --- /hint --- --- hint --- Hier sind die Code-Blöcke, die du brauchen wirst: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) --- /hint --- --- hint --- So sollte dein Code aussehen: ![Code for a changing costume](images/chatbot-costume-code.png) --- /hint --- --- /hints ---

--- /task ---

--- task ---

Ist dir aufgefallen, dass sich das Kostüm deines Chatbots nicht verändert hat, seit du das letzte Mal mit ihm gesprochen hast? Kannst Du dieses Problem beheben?

![Kostüm-Fehler](images/chatbot-costume-bug-test.png)

Testen und speichern - Führe deinen Code aus und gib "nein" ein, so dass dein Roboter traurig schaut. Wenn du dein Programm erneut startest, sollte dein Chatbot wieder ein fröhliches Gesicht zeigen, bevor er nach deinem Namen fragt.

![Ein anderes Kostüm testen](images/chatbot-costume-fix-test.png)

--- hints --- --- hint --- Wenn die **Figur angeklickt** wird, sollte dein Chatbot zuerst ein **wechsle zu Kostüm** "fröhliches Gesicht" ausführen. --- /hint --- --- hint --- Hier sind die zusätzlichen Code-Blöcke, die du brauchen wirst: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) --- /hint --- --- hint --- So sollte dein Code aussehen: ![Code for a costume fix](images/chatbot-costume-fix-code.png) --- /hint --- --- /hints ---

--- /task ---

--- challenge ---

## Herausforderung: zusätzliche Entscheidungen

Programmiere deinen Chatbot, um eine weitere Frage zu stellen - irgendetwas, auf das man mit "ja" oder "nein" antwortet. Kannst du deinen Chatbot auf die Antwort reagieren lassen?

![screenshot](images/chatbot-joke.png) --- /challenge ---
