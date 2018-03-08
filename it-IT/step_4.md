## Prendere decisioni

Puoi programmare il tuo chatterbot a decidere cosa fare, a seconda delle risposte dell'utente.

+ Facciamo in modo che il tuo chatterbot faccia una domanda all'utente che abbia come risposta 'sì' o 'no'. Ecco un esempio, ma se preferisci puoi cambiare la domanda:

	```blocks
		quando si clicca questo sprite
		chiedi [Ehi! Come ti chiami?] e attendi
		porta [nome v] a (risposta)
		dire (unione di [Ciao ] e (nome)) per (2) secondi
		chiedi (unione di [Stai bene ] e (nome)) e attendi
		se ((risposta) = [si]) allora
  			dire [Mi fa piacere!] per (2) secondi
		end
	```

	Nota che hai ora salvato il nome dell'utente in una variabile, e puoi usarlo ogni volta che vorrai.

+ Per testare correttamente questo programma, dovrai provarlo due volte - una volta digitando 'no' come risposta, e un'altra volta digitando 'sì'. Otterrai una reazione dal tuo chatterbot `se`{:class="blockcontrol"} rispondi 'sì'.

+ Il problema del chatterbot è che non dà una risposta se l'utente risponde 'no'. Puoi risolvere questo problema cambiando il blocco `se`{:class="blockcontrol"} a un blocco `se/altrimenti`{:class="blockcontrol"}, in modo che il tuo codice adesso sia così:

	```blocks
		quando si clicca questo sprite
		chiedi [Ehi! Come ti chiami?] e attendi
		porta [nome v] a (risposta)
		dire (unione di [Ciao ] e (nome)) per (2) secondi
		chiedi (unione di [Stai bene ] e (nome)) e attendi
		se ((risposta) = [si]) allora
  			dire [Mi fa piacere!] per (2) secondi
  		altrimenti
  			dire [Oh no!] per (2) secondi
		end
	```

+ Se provi il tuo codice, vedrai che avrai una reazione quando rispondi 'sì' o 'no'. Il tuo chatterbot risponderà 'Mi fa piacere!' quando tu rispondi 'sì', ma risponderà 'Oh no!' se digiti qualsiasi altra risposta (`altrimenti`{:class="blockcontrol"} significa 'diversamente').

	![screenshot](images/chatbot-else.png)

+ Dentro un blocco `se`{:class="blockcontrol"} o `altrimenti`{:class="blockcontrol"} puoi mettere qualsiasi codice, e non solo il codice che fa parlare il tuo chatterbot. Per esempio, puoi cambiare il costume del chatterbot er farlo combaciare con la risposta.

	Se dai un'occhiata agli costummi del chatterbot, noterai che ce ne sono più di uno. (Se non ci sono, puoi sempre aggiungerli tu!)

	![screenshot](images/chatbot-costumes.png)

	Puoi usare questi costumii come parte della risposta del tuo chatterbot, aggiungendo questo codice:

	![screenshot](images/chatbot-costumes-code.png)

+ Prova il tuo programma e vedrai che la faccia del tuo chatterbot cambierà in base alla risposta che dai.

	![screenshot](images/chatbot-face.png)

--- challenge ---
## Sfida: Altre decisioni

Programma il tuo chatterbot a fare un'altra domanda - che abbia come risposta 'sì' o 'no'. Sai come far reagire il tuo chatterbot alla risposta?

![screenshot](images/chatbot-joke.png)
--- /challenge ---
