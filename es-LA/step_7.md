## Cambiando ubicación

También puedes programar tu chatbot para cambiar su ubicación!

![Probando un cambio de disfraz](images/chatbot-backdrop-moon.png)

\--- tarea \---

¿Puedes programar tu chatbot para preguntar "Quieres ir a la luna", y luego cambiar el fondo cuando la respuesta es "sí"?

\--- pistas \---

\--- pista \---

Tu chatbot debería `preguntar "Desea ir a la luna?"`{:class="block3sensing"}, y `if`{:class="block3control"} que `answer`{:class="block3sensing"} "sí", debería `cambiar el fondo a la luna`{:class="block3looks"}.

\--- /pista \---

\--- pista \---

Aquí están los bloques de código que necesitas añadir a tu código de chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
cambiar el fondo a (luna)

pregunte [Desea ir a la luna?] y esperar

si (respuesta) = [si]; luego 

fin
```

\--- /pista \---

\--- pista \---

Así es como debería verse tu código:

```blocks3
pregunta [Desea ir a la luna?] y esperar
si (respuesta) = [si] luego 
  cambiar de fondo a (luna)
fin
```

\--- /consejo \---

\--- / consejos \---

\--- /tarea \---

\--- tarea \---

Ahora necesitas asegurarte de que tu chatbot comienza en la ubicación correcta cuando haces clic en él para hablar con él. Añade este bloque a la parte superior de tu código de chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
cuando haces click sobre tu avatar

+ cambiar de fondo (espacio v)
```

\--- / tarea \---

\--- tarea \---

Evalúa tu programa y responde "sí" cuando el chatbot pregunta si quieres ir a la luna. Debes ver que la ubicación del chatbot cambia.

\--- / tarea \---

\--- tarea \---

También puedes añadir el siguiente código dentro del nuevo `si`{:class="block3control"} bloque para hacer que el chatbot salte y baje cuatro veces si respondes "sí":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(respuesta) = [si]> entonces 
  cambiar de fondo a (luna v)

+  repetir (4) 
    cambiar y por (10)
    esperar (0.1) segundos
    cambiar y por (-10)
    esperar (0.1) segs
  fin
fin
```

\--- / tarea \---