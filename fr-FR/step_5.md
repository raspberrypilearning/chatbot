## Étape 3: Prendre des décisions

Vous pouvez programmer votre chatbot pour qu'il decide quoi dire ou faire en fonction de vos réponses à ses questions.

\--- task \---

Pouvez-vous faire en sorte que le chatbot pose la question "Allez vous bien ?", Et le code pour répondre "Je suis heureux de l'entendre!" seulement ** si ** l'utilisateur répond "oui"?

Pour tester correctement votre nouveau code, vous devez le tester deux fois ** ** , une fois avec la réponse "oui", et une fois avec la réponse "non".

Votre chatbot devrait répondre "Je suis content de l'entendre!" si vous répondez «oui», mais ne rien dire si vous répondez «non».

![Tester une reponse du ChatBot](images/chatbot-if-test.png)

\--- astuces \--- \--- indice \--- Après que votre chatbot a dit "Salut", il devrait maintenant aussi pouvoir demander** "Ça va?"** . ** Si ** vous répondez "oui", alors le chatbot devrait ** dire ** "C'est bon à entendre!". \--- / indice \--- \--- indice \--- Voici les blocs de code supplémentaires dont vous aurez besoin: <0 /> \--- / indice \--- \--- indice \--- Voici à quoi devrait ressembler votre code: <1 /> \--- / indice \--- \--- / astuces \---

\--- /task \---

\--- task \---

En ce moment votre chatbot ne dit rien si vous répondez "non". Pouvez-vous changer votre chatbot pour qu'il réponde aussi "Oh non!" Si vous répondez "non" à sa question?

Tester et enregistrer. Votre chatbot devrait maintenant dire "Oh non!" si vous répondez "non". En fait, il dira "On non!" si vous répondez avec autre chose que "oui" (le ** sinon ** dans un bloc ` si / sinon ` signifie ** autrement** ).

![Tester une reponse du ChatBot](images/chatbot-if-else-test.png)

\--- hint \--- \--- hint \--- Votre chatbot devrait maintenant dire **"C'est bon de l'entendre!" ** si votre réponse est "oui", mais devrait dire "Oh non!" si vous répondez à autre chose ** ** . \--- /hint \--- \--- hint \--- Voici les blocs de code dont tu auras besoin: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Ton code devrait ressembler à ceci: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Vous pouvez mettre n'importe quel code dans un bloc ` si / sinon `, pas seulement du code pour faire parler votre chatbot. Si vous cliquez sur l'onglet Costume ** de votre chatbot ** , vous verrez qu'il y a plus d'un costume.

![costumes de chatbot](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Pouvez-vous changer le costume du chatbot pour qu'il corresponde à votre réponse?

Testez et enregistrez. Vous devriez voir le visage de votre chatbot changer en fonction de votre réponse.

![Tester un costume changeant](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Votre chatbot devrait maintenant ** changer de costume ** en fonction de la réponse donnée. \--- /hint \--- \--- hint \--- Voici les blocs de code dont tu auras besoin: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Ton code devrait ressembler à ceci: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Avez-vous remarqué que le costume de votre chatbot reste le même qu'a la dernière fois qu'il a été changer quand vous lui avez parlé? Pouvez-vous résoudre ce problème?

![Bug de costume
](images/chatbot-costume-bug-test.png)

Testez et enregistrez: exécutez votre code et tapez "non", afin que votre chatbot ne soit pas satisfait. Lorsque vous réexécutez votre code, votre chatbot doit revenir à un visage souriant avant de demander votre nom.

![Test d'une correction de costume](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- Quand le sprite ** est cliqué ** , votre chatbot doit d'abord ** changer de costume ** à un visage souriant. \--- /hint \--- \--- hint \--- Voici les blocs de code dont tu auras besoin: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Ton code devrait ressembler à ceci: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- Défi\---

## Challenge : plus d'objets

Programmez votre chatbot pour poser une autre question - quelque chose avec une réponse «oui» ou «non». Pouvez-vous faire en sorte que votre chatbot réponde à la réponse?

![capture d'écran](images/chatbot-joke.png) \--- /défi \---