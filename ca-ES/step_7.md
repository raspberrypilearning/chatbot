## S'està canviant la ubicació

També pots programar el teu xatbot per canviar la seva ubicació!

![S'està provant un canvi de fons d'escenari](images / chatbot-backdrop-moon.png)

\--- task \---

Pots programar el teu xatbot perquè pregunti "Vols anar a la lluna?" i després canviar el fons d'escenari si contesta "sí"?

\--- hint \---

\--- hint \---

El teu xatbot hauria de ` preguntar "Vols anar a la Lluna?" ` {: class = "block3sensing"} i ` si ` {: class = "block3control"}la teva ` resposta ` {: class = "block3sensing"} és "sí", hauria de ` canviar l'escenari de fons a la lluna ` {: class = "block3looks"}.

\--- /hint \---

\--- hint \---

Aquí tens els blocs de codi que has d’afegir al teu codi del xatbot.

![nano sprite](images / nano-sprite.png)

```blocks3
canvi de fons a (lluna v)

pregunta [Voleu anar a la lluna?] i espera

si <(resposta) = [sí]> llavors 

fi
```

\--- /hint \---

\--- hint \---

Així és com s'hauria de veure el teu codi:

```blocks3
pregunta [Vols anar a la lluna?] i espera
si <(resposta) = [si]> llavors 
  canviar fons a (Lluna v)
final
```

\--- /hint \---

\--- /hint \---

\--- /task \---

\--- task \---

Ara t'has d'assegurar que el teu xatbot comenca a la ubicació adequada quan fas clic per parlar amb ell. Afegeix aquest bloc a la part superior del codi del xatbot:

![nano sprite](images / nano-sprite.png)

```blocks3
quan es fa clic a aquest sprite

+ canviar de fons a (espai v)
```

\--- /task \---

\--- task \---

Posa a prova el teu programa i respon "sí" quan el xatbot et pregunta si vols anar a la Lluna. Hauries de veure que la ubicació del xatbot canvia.

\--- /task \---

\--- task \---

També pots afegir el següent codi dins del nou bloc ` si ` {: class = "block3control"} per fer saltar el xatbot amunt i avall quatre vegades si respons que "sí":

![nano sprite](images / nano-sprite.png)

```blocks3
si <(resposta) = [yes]> després 
  canvieu el fons a (lluna v)

+ repeteix (4) 
    canvieu y per (10)
    espera (0,1) segons
    canvieu y per (-10)
    espera (0,1) segons
  final
final
```

\--- /task \---