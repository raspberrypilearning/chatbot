## Changer emplacement

Vous pouvez également programmer votre chatbot pour qu'il change d'emplacement!

![Tester un costume changeant](images/chatbot-backdrop-moon.png)

\--- task \---

Pouvez-vous programmer votre chatbot pour demander "Voulez-vous aller sur la lune", puis changer de fond lorsque la réponse est "oui"?

\--- astuces \---

\--- hint \---

Votre chatbot devrait `demander "Voulez-vous aller sur la lune?"`{: class = "block3sensing"}, et `si`{: class = "block3control"} vous `répondez`{: class = "block3sensing"} "oui", il devrait `changer le fond de la lune`{: class = "block3looks"}.

\--- /hint \---

\--- hint \---

Voici les blocs de code que vous devez ajouter à votre code chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
changer la toile de fond en (lune v)

demander [voulez-vous aller sur la lune?] et attendre

si <(réponse) = [yes]> puis 

fin
```

\--- /indice \---

\--- hint \---

Voici à quoi votre code devrait ressembler:

```blocks3
demandez à [Voulez-vous aller sur la lune?] et attendez
si <(réponse) = [yes]> puis 
  commutez la toile de fond sur (lune v)
fin
```

\--- /indice \---

\--- /astuces \---

\--- /task \---

\--- task \---

Maintenant, vous devez vous assurer que votre chatbot commence au bon endroit lorsque vous cliquez dessus pour lui parler. Ajoutez ce bloc en haut de votre code chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
lorsque ce sprite a cliqué sur

+ basculer en arrière-plan sur (espace v)
```

\--- /task \---

\--- task \---

Testez votre programme et répondez "oui" lorsque le chatbot vous demande si vous souhaitez aller sur la lune. Vous devriez voir que l'emplacement du chatbot change.

\--- /task \---

\--- task \---

Vous pouvez également ajouter le code suivant dans le nouveau bloc `if`{: class = "block3control"} pour que le chatbot saute quatre fois si vous répondez "oui":

![nano sprite](images/nano-sprite.png)

```blocks3
si <(réponse) = [yes]> 
  change de fond pour (lune v)

+ répéte (4) 
    change y par (10)
    attente (0,1)
    change y par (-10)
    attente (0,1)
  fin
fin
```

\--- /task \---