## Changement d'emplacement

Vous pouvez programmer votre chatbot pour qu'il décide quoi faire en fonction des réponses qu'il reçoit.

Tout d'abord, vous allez demander à votre chatbot de poser une question à laquelle on peut répondre par "oui" ou par "non".

\--- task \---

Changez le code de votre chatbot. Votre chatbot devrait poser la question "Êtes-vous OK nom", en utilisant la variable `nom`{: class = "block3variables"}. Ensuite, il devrait répondre "ça fait plaisir à entendre!" `si`{: class = "block3control"} la réponse reçue est "oui", mais ne dit rien si la réponse est "non"

![Tester une reponse du ChatBot](images/chatbot-if-test1-annotated.png)

![Tester une reponse du ChatBot](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez à [quel est votre nom?] et attendez
jeu [nom v] pour (répondre)
dire (rejoindre [Hi] (nom)) pendant (2) secondes
+ demander (rejoindre [Etes-vous d'accord] (nom)) et attendez
+ si <(réponse) = [yes]> puis 
  dites [Cela fait plaisir à entendre!] pendant (2) secondes
fin
```

Pour tester votre nouveau code correctement, vous devez le tester **deux fois**: une fois avec la réponse "oui" et une fois avec la réponse "non".

\--- /task \---

Pour le moment, votre chatbot ne dit rien à la réponse "non".

\--- task \---

Changez le code de votre chatbot pour qu'il réponde "Oh non!" s'il reçoit "non" comme réponse à "Êtes-vous OK nom".

Remplacez le bloc `if, puis`{: class = "block3control"} par un bloc `if, alors, sinon`{: class = "block3control"}, et incluez du code pour que le chatbot `puisse dire "Oh non!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez à [Comment vous appelez-vous?] et attendez
set [nom v] pour (répondre)
dites (rejoignez [Hi] (nom)] pendant (2) secondes
demandez (rejoignez [Êtes-vous OK] ( name)) et attendez

+ si <(réponse) = [yes]> puis 
  dites [Cela fait plaisir à entendre!] pendant (2) secondes
sinon 
+ dites [Oh non!] pendant (2) secondes
fin
```

\--- /task \---

\--- task \---

Testez votre code. Vous devriez obtenir une réponse différente lorsque vous répondez "non" et lorsque vous répondez "oui": votre chatbot doit répondre avec "C'est génial d'entendre!" lorsque vous répondez "oui" (ce qui n’est pas sensible à la casse), et répondez par "Oh non!" quand vous répondez à **rien d'autre**.

![Tester une reponse du ChatBot](images/chatbot-if-test2.png)

![Tester une reponse du ChatBot](images/chatbot-if-else-test.png)

\--- /task \---

Vous pouvez mettre n'importe quel code dans un bloc `si, alors, sinon`{: class = "block3control"}, et pas seulement du code pour faire parler votre chatbot!

Si vous cliquez sur l'onglet **Costumes** votre chatbot, vous verrez qu'il y a plus d'un costume.

![costumes de chatbot](images/chatbot-costume-view-annotated.png)

\--- task \---

Changez le code de votre chatbot pour qu'il change de costume lorsque vous tapez votre réponse.

![Tester un costume changeant](images/chatbot-costume-test1.png)

![Tester un costume changeant](images/chatbot-costume-test2.png)

Modifiez le code à l'intérieur du `si, alors, sinon`{: class = "block3control"} bloc en `switch costume`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
quand ce sprite a cliqué sur
demandez à [quel est votre nom?] et attendez
set [nom v] pour (répondre)
dire (rejoindre [Hi] (nom)) pendant (2) secondes
demander (rejoindre [Etes-vous d'accord] nom) et attendez
si <(réponse) = [yes]> puis 

+ changez de costume en (nano-c v)
  dites [C’est génial à entendre!] pendant (2) secondes
sinon 
+ changez de costume en (nano- d v)
  dire [Oh non!] pendant (2)
secondes
```

Testez et enregistrez votre code. Vous devriez voir le visage de votre chatbot changer en fonction de votre réponse.

\--- /task \---

Avez-vous remarqué qu'après que le costume de votre chatbot ait changé, il reste comme ça et ne revient pas à ce qu'il était au début?

Vous pouvez essayer ceci: lancez votre code et répondez "non" pour que le visage de votre chatbot change de look. Ensuite, relancez le code et notez que votre chatbot ne redevient pas heureux avant de vous demander votre nom.

![Bug de costume
](images/chatbot-costume-bug-test.png)

\--- task \---

Pour résoudre ce problème, ajoutez au code du chatbot `costume`: {: class = "block3looks"} au début `lorsque vous cliquez sur le sprite`{: class = "block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
lorsque ce sprite a cliqué sur

+ basculer costume vers (nano-a v)
demander à [quel est votre nom?] et attendre
```

![Test d'une correction de costume](images/chatbot-costume-fix-test.png)

\--- /task \---