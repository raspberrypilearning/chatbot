## Cambiando ubicación

También puedes programar tu chatbot para cambiar su ubicación!

![Probando un cambio de disfraz](images/chatbot-backdrop-moon.png)

\--- task \---

¿Puedes programar tu chatbot para preguntar "Quieres ir a la luna", y luego cambiar el fondo cuando la respuesta es "sí"?

\--- hints \---

\--- hint \---

Tu chatbot debería `preguntar "Desea ir a la luna?"`{:class="block3sensing"}, y `if`{:class="block3control"} que `answer`{:class="block3sensing"} "sí", debería `cambiar el fondo a la luna`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Aquí están los bloques de código que necesitas añadir a tu código de chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

Así es como debería verse tu código:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ahora necesitas asegurarte de que tu chatbot comienza en la ubicación correcta cuando haces clic en él para hablar con él. Añade este bloque a la parte superior de tu código de chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Prueba tu programa y responde "sí" cuando el chatbot te pregunte si quieres ir a la luna. Deberías ver como cambia la ubicación del chatbot.

\--- /task \---

\--- task \---

También puedes añadir el siguiente código dentro del nuevo `si`{:class="block3control"} bloque para hacer que el chatbot salte y baje cuatro veces si respondes "sí":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> then 
  switch backdrop to (moon v)

+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

\--- /task \---