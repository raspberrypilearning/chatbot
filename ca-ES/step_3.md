## Un xatbot parlant

Ara que tens un xatbot amb personalitat, programem-lo per a què parli amb tu.

\--- task \---

Feu clic al vostre Sprite de xatbot i afegeix-li aquest codi perquè ` quan li facis clic ` {:class = "block3events"}, ` et demani el teu nom ` {:class = "block3sensing"} i després ` digui "Quin nom tan encantador"! ` {:class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
quan cliquis aquest sprite 
pregunta [Quin és el teu nom?] i espera
digues [Quin nom tan encantador!] durant (2) segons
```

\--- /task \---

\--- task \---

Fes clic al teu xatbot per provar el teu codi. Quan el xatbot et demani el teu nom, escriu-lo al quadre que apareix a la part inferior de l'Escenari i, a continuació, fes clic a la marca blava o prem <kbd>Intro</kbd>.

![Provant una resposta del Xatbot](images/chatbot-characters.png)

![Provant una resposta de Xatbot](images/chatbot-characters.png)

\--- /task \---

\--- task \---

Ara mateix, el teu xatbot respon "Quin nom tan encantador!" cada vegada que respons. Pots fer que la resposta del xatbot sigui més personal, de manera que la resposta sigui diferent cada vegada que s'escriu un altre nom.

Canvia el codi de l'sprite del xatbot per ` afegir` {:class = "block3operators"} "Hola" amb la ` resposta` {:class = "block3sensing"} a la pregunta "Quin és el teu nom?", perquè el codi es vegi així:

![nano sprite](images/nano-sprite.png)

```blocks3
quan cliquis aquest sprite 
pregunta [Quin és el teu nom?] i espera
digues (afegir [hola] (resposta)::+) durant (2) segons
```

![Prova una resposta personalitzada](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

En emmagatzemar la resposta en una **variable**, pots utilitzar-la en qualsevol lloc del teu projecte.

Crea una nova variable anomenada `nom`{:class = "blockvariable"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Ara, canvia el codi de l'sprite del teu xatbot per establir la variable `nom` {:class = "block3variables"} a `resposta` {:class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
quan cliques a aquest sprite
pregunta [Quin és el teu nom?] i espera

+ establir [nom v] a (resposta)
dir (afegir (nom :: variables +)) durant (2) segons
```

El teu codi hauria de funcionar com abans: el teu xatbot hauria de saludar amb el nom que has escrit.

![Prova una resposta personalitzada](images/chatbot-answer-test.png)

\--- /task \---

Torna a provar el teu programa. Tingues en compte que la resposta que escrius s'emmagatzema a la variable ` nom` {:class = "block3variables"} i també es mostra a l'extrem superior esquerre de l'Escenari. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.