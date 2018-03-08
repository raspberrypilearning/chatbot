## Changement d'emplacement

Vous pouvez aussi programmer votre chatbot pour changer son emplacement.

+ Ajoutez un autre fond à votre étape, par exemple le fond 'lune'.

	![screenshot](images/chatbot-moon.png)

+ Vous pouvez maintenant programmer votre chatbot pour changer l'emplacement en ajoutant ce code à votre chatbot :

	```blocks
		 demander [Je vais à la lune. Voulez-vous venir avec moi ?] et attendre
		si ((réponse) = [oui]) alors
			basculer sur l'arrière-plan [lune v]
		end
	```


	![screenshot](images/chatbot-outside.png)

+ Testez votre programme et répondez 'oui' si vous voulez aller sur la lune. Vous devriez voir que l'emplacement du chatbot a changé.

	![screenshot](images/chatbot-backdrop.png)

+ Votre chatbot change-t-il d'emplacement si vous ne tapez pas ? Qu'arrive-t-il lorsque vous tapez ` je ne suis pas sûr ` ?
