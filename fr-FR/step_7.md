## Changer d'emplacement

Tu peux également programmer ton chatbot pour qu'il change d'emplacement!

![Test d'un arrière-plan changeant](images/chatbot-backdrop-moon.png)

--- task ---

Peux-tu programmer ton chatbot pour demander "Veux-tu aller sur la lune", puis changer de fond lorsque la réponse est "oui"?

--- hints ---


--- hint ---

Ton chatbot devrait `demander "Veux-tu aller sur la lune?"`{:class="block3sensing"}, et `si`{:class="block3control"} tu `réponds`{:class="block3sensing"} "oui", cela devrait `changer le fond en paysage lunaire`{:class="block3looks"}.

--- /hint ---

--- hint ---

Voici les blocs de code que tu dois ajouter à ton code chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (lune v)

ask [Veux-tu aller sur la lune?] and wait

if <(réponse) = [oui]> then

end
```

--- /hint---

--- hint ---

Voici à quoi ton code devrait ressembler:

```blocks3
ask [Veux-tu aller sur la lune?] and wait
if <(réponse) = [oui]> then
switch backdrop to (lune v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Maintenant, tu dois t'assurer que ton chatbot commence au bon endroit lorsque tu cliques dessus pour lui parler. Ajoute ce bloc en haut de ton code chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch backdrop to (espace v)
```

--- /task ---

--- task ---

Teste ton programme et répond "oui" lorsque le chatbot te demande si tu souhaites aller sur la lune. Tu devrais voir que l'emplacement du chatbot change.

--- /task ---

--- task ---

Tu peux également ajouter le code suivant dans le nouveau bloc `if`{:class="block3control"} pour que le chatbot saute quatre fois si tu réponds "oui":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [oui]> then 
  switch backdrop to (lune v)
+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

--- /task ---
