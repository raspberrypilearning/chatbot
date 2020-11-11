## Tomando decisiones

Usted puede programar su chatbot para decidir qué hacer basado en las respuestas que recibe.

Primero, vas a hacer que tu chatbot haga una pregunta que se pueda responder con "sí" o "no".

--- task ---

Cambia el código de tu chatbot. Su chatbot debe hacer la pregunta "Estás bien nombre", usando el `nombre`{:class="block3variables"} variable. Entonces debería responder "¡Qué bueno es oir eso!" `si`{:class="block3control"} la respuesta que recibe es "sí", pero no digas nada si la respuesta es "no".

![Probando una respuesta del ChatBot](images/chatbot-if-test1-annotated.png)

![Probando una respuesta del ChatBot](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [¿Cómo te llamas?] and wait
set [nombre v] to (answer)
say (join [Hola ] (nombre)) for (2) seconds
+ask (join [Estás bien ] (nombre)) and wait
+if <(answer) = [sí]> then 
  say [¡Qué bueno es oir eso!] for (2) seconds
end
```

Para probar su nuevo código correctamente, debe probarlo **dos veces**: una vez con la respuesta "sí", y una vez con la respuesta "no".

--- /task ---

En este momento, tu chatbot no dice nada a la respuesta "no".

--- task ---

Cambia el código de tu chatbot para que responda "¡Oh no!" si recibe "no" como respuesta a "Estás bien nombre?".

Reemplace el bloque `si, entonces`{:class="block3control"} con un bloque `si, entonces, otro`{:class="block3control"} y incluya código para que el chatbot pueda `decir "¡Oh no!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [¿Cómo te llamas?] and wait
set [nombre v] to (answer)
say (join [Hola ] (nombre)) for (2) seconds
ask (join [¿Estás bien? ] (nombre)) and wait
+ if <(answer) = [sí]> then 
  say [¡Qué bueno es oir eso!] for (2) seconds
else 
+  say [¡Oh no!] for (2) seconds
end
```

--- /task ---

--- task ---

Prueba tu código. Obtendrás una respuesta diferente cuando respondes "no" y cuando responda "sí": el chatbot debe responder con "¡Qué bueno es oir eso!" al responder "sí" (que no distingue mayúsculas de minúsculas) y responder con "¡Oh no!" cuando respondes **cualquier cosa**.

![Probando una respuesta del ChatBot](images/chatbot-if-test2.png)

![Probando una respuesta de sí / no](images/chatbot-if-else-test.png)

--- /task ---

Puedes poner cualquier código dentro de un bloque `si, entonces, otro`, no solo el código para hacer que tu chatbot hable!

Si haces un clic en la pestaña **disfraz** de tu chatbot, verás que tiene más de un disfraz.

![Disfraces del chatbot](images/chatbot-costume-view-annotated.png)

--- task ---

Cambie el código de su chatbot para que el chatbot cambie de vestuario cuando escriba su respuesta.

![Probando un cambio de disfraz](images/chatbot-costume-test1.png)

![Probando un cambio de disfraz](images/chatbot-costume-test2.png)

Cambie el código dentro del bloque `si, entonces, en otro caso`{:class="block3control"} a `bloque para cambiar el traje`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [¿Cómo te llamas?] and wait
set [nombre v] to (answer)
say (join [Hola ] (nombre)) for (2) seconds
ask (join [¿Estás bien? ] (nombre)) and wait
if <(answer) = [sí]> then 
+  switch costume to (nano-c v)
  say [¡Qué bueno es oir eso!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [¡Oh no!] for (2) seconds
end
```

Prueba y guarda tu código. Debería ver cambiar el disfraz de su chatbot dependiendo de su respuesta.

--- /task ---

¿Has notado que, después de que el disfraz de tu chatbot haya cambiado, se mantiene así y no cambia de nuevo a lo que fue al principio?

Puede probar esto: ejecute su código y responda "no" para que la cara de su chatbot cambie a un aspecto infeliz. Luego vuelva a ejecutar su código y observe que su chatbot no vuelve a verse feliz antes de preguntar su nombre.

![Error de disfraz](images/chatbot-costume-bug-test.png)

--- task ---

Para solucionar este problema, agregue al código del chatbot para `cambiar traje`{:class="block3looks"} al inicio `cuando se hace clic en el personaje`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch costume to (nano-a v)
ask [¿Cómo te llamas?] and wait
```

![Prueba una solución de traje](images/chatbot-costume-fix-test.png)

--- /task ---