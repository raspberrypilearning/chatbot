## Tomando decisiones

Puedes programar tu chatbot para que decida qué hacer en función de las respuestas que recibe.

Primero, vas a hacer que tu chatbot haga una pregunta que pueda responderse con "sí" o "no".

\--- task \---

Cambia el código de tu chatbot. Tu chatbot debe hacer la pregunta "Estas bien nombre", usando la variable `nombre`{:class="block3variables"}. Entonces debería responder "¡Me alegra oírlo!" `si`{:class="block3control"} la respuesta que recibe es "sí", pero no decir nada si la respuesta es "no".

![Testing a chatbot reply](images/chatbot-if-test1-annotated.png)

![Comprobando la respuesta del chatbot](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [¿Cómo te llamas?] and wait
set [nombre v] to (answer)
say (join [Hola] (name)) for (2) seconds
+ask (join [Estás bien] (nombre)) and wait
+if <(answer) = [sí]> then 
  say [¡Me alegra oírlo!] for (2) seconds
end
```

Para probar tu nuevo código correctamente, debes probarlo **dos veces **, una vez con la respuesta "sí", y otra con la respuesta "no".

\--- /task \---

De momento, tu chatbot no dice nada a la respuesta "no".

\--- task \---

Cambia el código de tu chatbot para que responda "¡Oh no!" si recibe "no" como respuesta a "¿Estás bien nombre?".

Sustituye el bloque `if, then`{:class="block3control"} con un bloque `if, then, else`{:class="block3control"}, e incluye código para que el chatbot pueda `decir "Oh no!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [¿Cómo te llamas?] and wait
set [nombre v] to (answer)
say (join [Hola] (name)) for (2) seconds
ask (join [Estás bien ] (name)) and wait

+ if <(answer) = [sí]> then 
  say [¡Me alegra oírlo!] for (2) seconds
else 
+  say [¡Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

Prueba tu código. Deberías obtener una respuesta diferente cuando respondes "no" y cuando respondes "sí": tu chatbot debería responder con "¡Me alegra oírlo! cuando respondas "sí" (que no es sensible a mayúsculas/minúsculas), y responder con "¡Oh no!" cuando respondas **cualquier otra cosa**.

![Testing a chatbot reply](images/chatbot-if-test2.png)

![Comprobando una respuesta si/no](images/chatbot-if-else-test.png)

\--- /task \---

You can put any code inside an `if, then, else`{:class="block3control"} block, not just code to make your chatbot speak!

If you click your chatbot's **Costumes** tab, you'll see that there is more than one costume.

![chatbot costumes](images/chatbot-costume-view-annotated.png)

\--- task \---

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Testing a changing costume](images/chatbot-costume-test1.png)

![Testing a changing costume](images/chatbot-costume-test2.png)

Change the code inside the `if, then, else`{:class="block3control"} block to `switch costume`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

Test and save your code. You should see your chatbot's face change depending on your answer.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Costume bug](images/chatbot-costume-bug-test.png)

\--- task \---

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- /task \---