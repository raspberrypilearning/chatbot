## Cambia posizione

Puoi anche programmare il tuo chatterbot a cambiare la sua posizione.

+ Aggiungi un altro scenario al tuo quadro,per esempio lo scenario 'luna'.

	![screenshot](images/chatbot-moon.png)

+ Ora puoi programmare il tuo chatterbot a cambiare posizione, aggiungendo questo codice al tuo chatterbot:

	```blocks
		chiedi [Vado sulla luna. Vuoi venire con me?] e attendi
		se ((risposta) = [si]) allora
  			passa allo sfondo [moon v]
		end
	```

+ Devi anche assicurarti che il tuo chatterbot sia fuori quando inizi a parlarci. Aggiungi questo blocco in cima al codice chatterbot:

	![screenshot](images/chatbot-outside.png)

+ Prova il tuo programma, e rispondi 'sì' quando ti viene chiesto se vuoi andare sulla luna. Vedrai che la posizione del chatterbot è cambiata.

	![screenshot](images/chatbot-backdrop.png)

+ Il tuo chatterbot cambia posizione se digiti 'no'? Che succede se digiti 'non lo so'?

+ Puoi anche aggiungere questo codice dentro il blocco 'se' {.blockcontrol}, per far saltare il tuo chatterbot su e giù per 4 volte se la risposta è 'sì':

	```blocks
	ripeti (4) volte
  		cambia y di (10)
  		attendi (0.1) secondi
  		cambia y di (-10)
  		attendi (0.1) secondi
	end
	```

	![screenshot](images/chatbot-loop.png)

+ Prova di nuovo il codice. Il tuo chatterbot salta su e giù se rispondi 'sì'?
