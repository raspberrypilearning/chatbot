## Un ChiacchieRobot parlante

Adesso che hai un ChiacchieRobot con una personalità tutta sua, programmiamolo per farlo parlare.

--- task ---

Fai clic sul tuo sprite chiacchierobot e aggiungi questo codice in modo che `quando viene cliccato`{:class="block3events"}, `chieda il tuo nome`{:class="block3sensing"} e poi `dica "Che bel nome!"`{:Class="block3looks"}.

![sprite nano](images/nano-sprite.png)

```blocks3
quando si clicca questo sprite
chiedi [Come ti chiami?] e attendi
dire [Che bel nome!] per (2) secondi
```

--- /task ---

--- task ---

Clicca sul tuo chiacchierobot per testare il tuo codice. Quando il chiacchierobot chiede il tuo nome, digitalo nella casella che appare in fondo allo schermo, quindi fai clic sulla spunta blu o premi <kbd>Invio</kbd>.

![Testare la risposta del ChiacchieRobot](images/chatbot-ask-test1.png)

![Testare la risposta del ChiacchieRobot](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

In questo momento, il tuo chiacchierobot risponde "Che bel nome!" ogni volta che rispondi. Puoi rendere più personale la risposta, in modo che la risposta sia diversa ogni volta che viene digitato un nome diverso.

Cambia il codice dello sprite del chiacchierobot così da `concatenare`{:class="block3operators"} "Ciao" con la `risposta`{:class="block3sensing"} alla domanda "Qual è il tuo nome?", in modo che il codice assomigli a questo:

![sprite nano](images/nano-sprite.png)

```blocks3
quando si clicca questo sprite
chiedi [Come ti chiami?] e attendi
dire (unione di [Ciao ] e (risposta) :: +) per (2) secondi
```

![Testare una risposta personalizzata](images/chatbot-answer-test.png)

--- /task ---

--- task ---

Memorizzando la risposta in una **variabile**, puoi usarla ovunque nel tuo progetto.

Crea una nuova variabile chiamata `nome`{:Class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Ora, modifica il codice dello sprite del chiacchierobot per impostare la variabile `nome`{:class="block3variables"} al valore della `risposta`{:Class="block3sensing"}:

![sprite nano](images/nano-sprite.png)

```blocks3
quando si clicca questo sprite
chiedi [Come ti chiami?] e attendi

+ porta [nome v] a (risposta)
dire (unione di [Ciao ] e (nome :: + variables)) per (2) secondi
```

Il tuo codice dovrebbe funzionare come prima: il tuo ChiacchieRobot dovrebbe dire ciao usando il tuo nome.

![Testare una risposta personalizzata](images/chatbot-answer-test.png)

--- /task ---

Prova di nuovo il tuo codice. Nota che la risposta che hai digitato è memorizzata nella variabile `nome`{:class="block3variabili"} e viene mostrata anche nell'angolo in alto a sinistra dello schermo. Per farla sparire dallo schermo, vai nella sezione dei blocchi `Variabili`{:class="block3variables"} e togli il segno di spunta alla casella accanto alla variabile `nome`{:class="block3variables"} in modo che non sia contrassegnata.