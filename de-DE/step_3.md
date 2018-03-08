## Ein sprechender Roboter

Jetzt, wo Du einen SprechBot mit einer echten Persönlichkeit hast, lass uns ihm das Sprechen beibringen!

+ Klicke auf Deine SprechBot-Figur und füge ihr diesen Code hinzu:

	```blocks
		Wenn ich angeklickt werde
		frage [Hey! Wie heißt Du?] und warte
		sage [Was für ein hübscher Name!] für (2) Sek.
	```

+ Klicke auf deinen SprechBot, um den Code zu testen. Wenn Du aufgefordert wirst Deinen Namen zu sagen, tippe diesen in die Box am unteren Rand der Bühne ein.

	![screenshot](images/chatbot-text.png)

+ Dein SprechBot antwortet nun jedes Mal einfach `Was für ein hübscher Name!`. Personalisiere die Antwort Deines SprechBots, indem Du die Antwort des Nutzers gebrauchst. Ändere den Code des SprechBots, so dass dieser wie folgt aussieht.

	```blocks
		Wenn ich angeklickt werde
		frage [Hey! Wie heißt Du?] und warte
		sage <verbinde [Hallo] (Antwort)> für (2) Sek.
	```

Um den letzten Block zu erstellen, wirst du zunächst auf den grünen `verbinde`{:class="blockoperators"}-Block klicken und ihn in den `sage`{:class="blocklooks"}-Block ziehen müssen.

![screenshot](images/chatbot-join.png)

Du kannst dann den Text `hello` zu, sagen wir mal, `Hallo` ändern, und den hellblauen `Antwort`{:class="blocksensing"}-Block (aus dem Bereich 'Fühlen') in den `world`-Text ziehen.

![screenshot](images/chatbot-answer.png)

+ Teste dieses neue Programm. Funktioniert es so, wie Du es erwartet hast? Kannst Du eines der Probleme lösen, die Du entdeckst? (Tipp: Du kannst versuchen irgendwo ein Leerzeichen einzufügen!)

+ Vielleicht möchtest Du den Namen des Nutzers in einer Variable speichern, damit Du diesen später an anderer Stelle nutzen kannst. Erstelle eine neue Variable namens `Name`{:class="blockdata"}. Wenn Du vergessen hast wie man das macht, wird Dir das Ballons-Projekt auf die Sprünge helfen.

+ Die Information, die Du eingegeben hast, ist in einer speziellen Variable namens `Antwort`{:class="blocksensing"} bereits gespeichert worden. Gehe in die Fühlen-Block-Gruppe und klicke auf den Antwort-Block, so dass ein Vermerk auftaucht. Der aktuelle Wert in `Antwort`{:class="blocksensing"} sollte in der oberen linken Ecke der Bühne angezeigt werden.

+ Sobald Du Deine neue Variable erstellt hast, stelle sicher, dass der Code Deines SprechBots so aussieht:

	```blocks
		Wenn ich angeklickt werde
		frage [Hey! Wie heißt Du?] und warte
		setze [name v] auf (Antwort)
		sage <verbinde [Hi] (name)> für (2) Sek.
	```

+ Wenn Du Dein Programm nochmals testest, wirst Du feststellen, dass die Antwort in der `Name`{:class="blockdata"}-Variable gespeichert worden ist und in der oberen linken Ecke der Bühne angezeigt wird. Die `Name`{:class="blockdata"}-Variable sollte nun den gleichen Wert enthalten wie die `Antwort`{:class="blocksensing"}-Variable.

	![screenshot](images/chatbot-variable.png)

	Wenn Du die Variable lieber nicht auf der Bühne sehen möchtest, kannst Du auf das Kontrollkästchen neben der Namensvariablen in dem 'Skripte'-Reiter klicken, um diese zu verbergen.

--- challenge ---
## Herausforderung: Mehr Fragen

Programmiere Deinen SprechBot so, dass er eine weitere Frage stellt. Kannst die Antwort in einer Variablen speichern?

![screenshot](images/chatbot-question.png)
--- /challenge ---
