## Un chatbot parlant

Maintenant que vous avez un chatbot avec une personnalité, vous allez le programmer pour qu'il vous parle.

\--- task \---

Cliquez sur l' image - objet chatbot et ajoutez ce code afin que `quand on clique dessus`{: class = « block3events »}, il `vous demande votre nom`{: class = « block3sensing »} puis `dit « Quel joli nom!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez [Quel est votre nom?] et attendez
dites [Quel beau nom!] pendant (2) secondes
```

\--- /task \---

\--- task \---

Cliquez sur votre chatbot pour tester votre code. Lorsque le chatbot vous demande votre nom, tapez-le dans la zone qui apparaît au bas de la scène, puis cliquez sur le repère bleu ou appuyez sur <kbd>Entrée</kbd>.

![Tester une reponse du ChatBot](images/chatbot-ask-test1.png)

![Tester une reponse du ChatBot](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

En ce moment, votre chatbot répond "Quel joli nom!" chaque fois que vous répondez. Vous pouvez rendre la réponse du chatbot plus personnelle, de sorte que la réponse soit différente chaque fois que vous entrez un nom différent.

Modifiez le code du sprite du chatbot en `rejoignez`{: class = "block3operators"} "Hi" avec les `réponses`{: class = "block3sensing"} en "Quel est votre nom?" question, de sorte que le code ressemble à ceci:

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez à [quel est votre nom?] et attendez
dites (rejoignez [Bonjour] (réponse) :: +) pendant (2) secondes
```

![Tester une réponse personnalisée](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

En stockant la réponse dans une variable ****, vous pouvez l'utiliser n'importe où dans votre projet.

Créez une nouvelle variable appelée `nom`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Maintenant, changez le code de votre chatbot sprites pour définir la variable `name`{: class = "block3variables"} à `answer`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez à [quel est votre nom?] et attendez

+ réglez [nom v] sur (réponse)
dites (rejoignez [Hi] (nom :: variables +)) pendant (2) secondes
```

Votre code devrait fonctionner comme avant: votre chatbot devrait dire bonjour en utilisant le nom que vous avez entré.

![Tester une réponse personnalisée](images/chatbot-answer-test.png)

\--- /task \---

Testez à nouveau votre programme. Notez que la réponse que vous tapez est stockée dans la variable `name`{: class = "block3variables"} et également affichée dans le coin supérieur gauche de la scène. Pour le faire disparaître de la scène, accédez à la section des blocs `Data`{: class = "block3variables"} et cliquez sur la case en regard de `name`{: class = "block3variables"} pour qu'elle ne soit pas marquée.