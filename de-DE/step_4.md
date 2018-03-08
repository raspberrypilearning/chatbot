## Entscheidungen treffen

Du kannst Deinen SprechBot so programmieren, dass er eine Entscheidung basierend darauf trifft, was der Nutzer antwortet.

+ Lass uns Deinen SprechBot dazu bringen eine Frage zu stellen, die mit `ja` oder `nein` beantwortet werden kann. Hier ist ein Beispiel, aber Du kannst auch eine andere Frage wählen, wenn Du möchtest:

	```blocks
		Wenn ich angeklickt werde
		frage [Hey! Wie heißt Du?] und warte
		setze [name v] auf (Antwort)
		sage <verbinde [Hallo ] (Name)> für (2) Sek.
		frage <verbinde [Geht es Dir gut?] (Name)> und warte
		falls ((Antwort) = [ja]) dann
			sage [Juhu! Das freut mich zu hören!] für (2) Sek.
		end
	```

	Bemerke, dass jetzt, wo Du den Namen des Nutzers in einer Variablen gespeichert hast, Du ihn sooft verwenden kannst, wie Du möchtest!

+ Um das Spiel korrekt zu testen, müsstest Du es zwei Mal spielen - ein Mal, wo Du als Antwort `nein` eingibst und ein Mal, wo Deine Antwort `ja` lautet. Du solltest nur dann eine Antwort vom SprechBot erhalten, `wenn` {.blockcontrol} die Antwort `ja` ist.

+ Das Problem mir Deinem SprechBot ist, dass er nicht antwortet, wenn der Nutzer `nein` sagt. Du kannst das Problem schnell lösen, indem Du den `wenn` {.blockcontrol}-Block zu einem `wenn/sonst` {.blockcontrol}-Block änderst, so dass der Code folgendermaßen aussieht:

	```blocks
		Wenn ich angeklickt werde
		frage [Hey! Wie heißt Du?] und warte
		setze [name v] auf (Antwort)
		sage <verbinde [Hallo ] (Name)> für (2) Sek.
		frage <verbinde (Name) [, geht es Dir gut?]> und warte
		falls ((Antwort)=[ja]) dann
			sage [Juhu! Das freut mich zu hören!] für (2) Sek.
		sonst
			sage [Oh!] für (2) Sek.
		end
	```

+ Wenn Du Deinen Code erneut testest, wirst Du sehen, dass Du sowohl eine Antwort erhältst, wenn Du `ja`, als auch wenn Du `nein` eingibst. Dein SprechBot sollte `Juhu! Das freut mich zu hören!` nur sagen, wenn die Antwort `ja` lautet und `Oh!`, wenn Du etwas anderes als `ja` eintippst.

	![screenshot](images/chatbot-else.png)

+ Du kannst zu jeder Art von Code einen `wenn` {.blockcontrol}- oder `sonst` {.blockcontrol}-Block einfügen, nicht nur zum Code, der Deinen Roboter zum Sprechen bringt. Du könntest beispielsweise das Kostüm bzw. den Ausdruck des SprechBots passend zu der Antwort wechseln.

	Wenn Du Dir die Kostüme Deines SprechBots anschaust, sieht Du, dass es mehr als eins gibt. (Wenn nicht, kannst Du jederzeit selbst welche hinzufügen!)

	![screenshot](images/chatbot-costumes.png)

	Du kannst diese Kostüme als Teil der Antwort Deines SprechBots benutzen, indem Du diesen Code hinzufügst:

	![screenshot](images/chatbot-costumes-code.png)

+ Teste Dein Programm und Du solltest sehen, dass sich die Reaktion des SprechBots entsprechend der Antwort verändert.

	![screenshot](images/chatbot-face.png)

--- challenge ---
## Herausforderung: Mehr Entscheidungen

Programmiere Deinen SprechBot, um eine andere Frage zu stellen - etwas, das mit `ja` oder `nein` beantwortet werden kann. Kannst Du Deinen SprechBot dazu bringen auf diese Frage zu antworten?

![screenshot](images/chatbot-joke.png)
--- /challenge ---
