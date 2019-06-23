## Changer emplacement

Tu peux également programmer ton chatbot pour qu'il change d'emplacement!

![Test d'un arrière-plan changeant](images/chatbot-backdrop-moon.png)

\--- task \---

Peux-tu programmer ton chatbot pour demander "Veux-tu aller sur la lune", puis changer de fond lorsque la réponse est "oui"?

\--- hints \---

\--- hint \---

Ton chatbot devrait `demander "Veux-tu aller sur la lune?"`{: class = "block3sensing"}, et `si`{: class = "block3control"} tu `réponds`{: class = "block3sensing"} "oui", cela devrait `changer le fond en paysage lunaire`{: class = "block3looks"}.

\--- /hint \---

\--- hint \---

Voici les blocs de code que tu dois ajouter à ton code chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
changer la toile de fond en (lune v)

demander [Veux-tu aller sur la lune?] et attendre

si <(réponse) = [oui]> alors

fin
```

\--- /hint\---

\--- hint \---

Voici à quoi ton code devrait ressembler:

```blocks3
demander [Veux-tu aller sur la lune?] et attendre
si <(réponse) = [oui]> alors 
basculer sur l'arrière plan (lune v)
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Maintenant, tu dois t'assurer que ton chatbot commence au bon endroit lorsque tu cliques dessus pour lui parler. Ajoute ce bloc en haut de ton code chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
lorsque ce sprite est cliqué

+ basculer sur arrière-plan (espace v)
```

\--- /task \---

\--- task \---

Teste ton programme et répond "oui" lorsque le chatbot te demande si tu souhaites aller sur la lune. Tu devrais voir que l'emplacement du chatbot change.

\--- /task \---

\--- task \---

Tu peux également ajouter le code suivant dans le nouveau bloc `if`{: class = "block3control"} pour que le chatbot saute quatre fois si tu réponds "oui":

![nano sprite](images/nano-sprite.png)

```blocks3
si <(réponse) = [yes]> alors 
  bascule sur l'arrière-plan (lune v)

+ répéter (4) 
mettre y à (10)
attente (0,1) secondes
mettre y à (-10)
attente (0,1) secondes
fin
fin
```

\--- /task \---