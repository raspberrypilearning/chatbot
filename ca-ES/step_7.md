## Canviant la ubicació

També pots programar el teu xatbot per canviar la seva ubicació!

![S'està provant un canvi de fons d'escenari](images/chatbot-backdrop-moon.png)

\--- task \---

Pots programar el teu xatbot perquè pregunti "Vols anar a la lluna?" i després canviar el fons d'escenari si contesta "sí"?

\--- hints \---

\--- hint \---

El teu xatbot hauria de `preguntar "Vols anar a la Lluna?"`{:class="block3sensing"} i `si`{:class="block3control"} la teva `resposta`{:class="block3sensing"} és "sí", hauria de `canviar el fons de l'escenari al de la lluna`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Aquí tens els blocs de codi que has d’afegir al teu codi del xatbot.

![personatge nano](images/nano-sprite.png)

```blocks3
canvia el fons a (lluna v)

pregunta [Vols anar a la lluna?] i espera

si <(resposta) = [sí]> llavors 

fi
```

\--- /hint \---

\--- hint \---

Així és com s'hauria de veure el teu codi:

```blocks3
pregunta [Vols anar a la lluna?] i espera
si <(resposta) = [sí]> llavors 
  canvia el fons a (Lluna v)
fi
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ara t'has d'assegurar que el teu xatbot comença a la ubicació adequada quan fas clic per parlar amb ell. Afegeix aquest bloc a la part superior del codi del xatbot:

![personatge nano](images/nano-sprite.png)

```blocks3
quan es cliqui aquest personatge

+ canvia el fons a (espai v)
```

\--- /task \---

\--- task \---

Posa a prova el teu programa i respon "sí" quan el xatbot et pregunta si vols anar a la Lluna. Hauries de veure que la ubicació del xatbot canvia.

\--- /task \---

\--- task \---

També pots afegir el següent codi dins del nou bloc `si`{:class="block3control"} per fer saltar el xatbot amunt i avall quatre vegades si respons que "sí":

![personatge nano](images/nano-sprite.png)

```blocks3
si <(resposta) = [sí]> llavors 
  canvia el fons a (lluna v)

+ repeteix (4) 
    suma (10) a y
    espera (0,1) segons
    suma (-10) a y
    espera (0,1) segons
  fi
fi
```

\--- /task \---