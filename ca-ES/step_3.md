## Un xatbot parlant

Ara que tens un xatbot amb personalitat, programem-lo per a què parli amb tu.

--- task ---

Fes clic al teu personatge de xatbot i afegeix-li aquest codi perquè `quan li facis clic`{:class="block3events"}, `et demani el teu nom`{:class="block3sensing"} i després `digui "Quin nom tan bonic"!`{:class="block3looks"}.

![personatge nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Com et dius?] and wait
say [Quin nom tan bonic!] for (2) seconds
```

--- /task ---

--- task ---

Fes clic al teu xatbot per provar el teu codi. Quan el xatbot et demani el teu nom, escriu-lo al quadre que apareix a la part inferior de l'Escenari i, a continuació, fes clic a la marca blava o prem <kbd>Intro</kbd>.

![Provant una resposta del Xatbot](images/chatbot-characters.png)

![Provant una resposta de Xatbot](images/chatbot-characters.png)

--- /task ---

--- task ---

Ara mateix, el teu xatbot respon "Quin nom tan bonic!" cada vegada que respons. Pots fer que la resposta del xatbot sigui més personal, de manera que la resposta sigui diferent cada vegada que s'escriu un altre nom.

Canvia el codi del personatge del xatbot per `unir`{:class="block3operators"} "Hola" amb la `resposta`{:class="block3sensing"} a la pregunta "Com et dius?", perquè el codi es vegi així:

![personatge nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Com et dius?] and wait
say (join [Hola ] (answer) :: +) for (2) seconds
```

![Provant una resposta personalitzada](images/chatbot-answer-test.png)

--- /task ---

--- task ---

En emmagatzemar la resposta en una **variable**, pots utilitzar-la en qualsevol lloc del teu projecte.

Crea una nova variable anomenada `nom`{:class="blockvariable"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Ara, canvia el codi del personatge del teu xatbot per assignar la variable `nom`{:class="block3variables"} a `resposta`{:class="block3sensing"}:

![personatge nano](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Com et dius?] and wait
+ set [nom v] to (answer)
say (join [Hola ] (nom :: variables +)) for (2) seconds
```

El teu codi hauria de funcionar com abans: el teu xatbot hauria de saludar amb el nom que has escrit.

![Provant una resposta personalitzada](images/chatbot-answer-test.png)

--- /task ---

Torna a provar el teu programa. Tingues en compte que la resposta que escrius s'emmagatzema a la variable `nom`{:class="block3variables"} i també es mostra a l'extrem superior esquerre de l'Escenari. Per fer que desaparegui de l'Escenari, ves a la secció de blocs anomenada `Variables`{:class="block3variables"} i fes clic a la casella que hi ha al costat de `nom`{:class="block3variables"} perquè no quedi marcat.