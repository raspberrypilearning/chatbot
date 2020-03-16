## Cambio de ubicación

¡También puedes programar tu chatbot para cambiar su ubicación!

![Comprobar un cambio de fondo](images/chatbot-backdrop-moon.png)

\--- task \---

¿Puedes programar tu chatbot para que pregunte "¿Quieres ir a la luna?" y luego cambiar el fondo cuando la respuesta es "sí"?

\--- hints \---

\--- hint \---

Tu chatbot debería `preguntar "¿Quieres ir a la luna?"`{:class="block3sensing"}, y `si`{:class="block3control"} tú `respondes`{:class="block3sensing"} "sí", debería `cambiar el fondo a la luna`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Aquí tienes los bloques de código que necesitas añadir a tu código chatbot.

![objeto nano](images/nano-sprite.png)

```blocks3
cambiar fondo a (moon v)

preguntar [¿Quieres ir a la luna?] y esperar

si <(respuesta) = [si]> entonces

fin
```

\--- /hint \---

\--- hint \---

Así es como debe verse tu código:

```blocks3
preguntar [¿Quieres ir a la luna?] y esperar
si <(respuesta) = [si]> entonces
 cambiar fondo a (moon v)
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ahora tienes que asegurarte de que tu chatbot comienza en la ubicación correcta cuando hagas clic en él para hablarle. Añade este bloque a la parte superior del código de tu chatbot:

![objeto nano](images/nano-sprite.png)

```blocks3
al hacer clic en sprite

+cambiar fondo a (space v)
```

\--- /task \---

\--- task \---

Prueba tu programa y responde "sí" cuando el chatbot te pregunte si quieres ir a la luna. Deberías ver como cambia la ubicación del chatbot.

\--- /task \---

\--- task \---

También puedes añadir el siguiente código dentro del nuevo bloque `si`{:class="block3control"} para hacer que el chatbot salte cuatro veces si respondes "sí":

![objeto nano](images/nano-sprite.png)

```blocks3
si <(respuesta) = [si]> entonces
  cambiar fondo a (moon v)

+ repetir (4)
   sumar a y (10)
   esperar (0.1) segundos
   sumar a y (-10)
   esperar (0.1) segundos
```

\--- /task \---