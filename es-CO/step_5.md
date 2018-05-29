## Paso 3: Tomando decisiones

Puedes programar tu chatbot para que decida qué decir o hacer en función de tus respuestas a sus preguntas.

\--- task \---

¿Puedes hacer que el chatbot haga la pregunta "¿Estás bien?" y añadir código para que responda "¡Esto es estupendo!" solo **si** el usuario responde "sí"?

Para probar tu nuevo código correctamente, debes probarlo **dos veces**, una vez con la respuesta "sí", y una con la respuesta "no".

Tu chatbot debería responder "¡Esto es estupendo!" si respondes "sí", pero no decir nada si respondes "no".

![Testing a chatbot reply](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Después de que tu chatbot haya dicho "hola", ahora también debería **preguntar** "¿Estas bien?". **Si** tu respuesta es "sí", entonces el chatbot debe **decir** "¡Esto es estupendo!". \--- /hint \--- \--- hint \--- Estos son los bloques de código extra que vas a necesitar: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Tu código debería quedar así: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

De momento, tu chatbot no dice nada si respondes "no". ¿Puedes cambiar tu chatbot para que también responda "¡Oh, no!" si respondes "no" a su pregunta?

Prueba y guarda. Tu chatbot ahora debería decir "¡Oh, no!" si respondes "no". De hecho, dirá "¡Oh no!" si respondes con algo que no sea "sí" (el **si no** en un bloque `si/si no` significa **en caso contrario**).

![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Tu chatbot debería decir "Esto es estupendo!" **si** tu respuesta es "si", pero debería decir "Oh no!" si contestas otra cosa.**si no**. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need to use: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

You can put any code inside an `if/else` block, not just code to make your chatbot speak. If you click your chatbot's **Costume** tab, you'll see that it has more than one costume.

![chatbot costumes](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Can you change the chatbot's costume to match your response?

Test and save. You should see your chatbot's face change depending on your answer.

![Testing a changing costume](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Your chatbot should now also **switch costume** depending on the answer given. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need to use: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Have you noticed that your chatbot's costume stays the same that it changed to the last time you spoke to it? Can you fix this problem?

![Costume bug](images/chatbot-costume-bug-test.png)

Test and save: Run your code and type "no", so that your chatbot looks unhappy. When you run your code again, your chatbot should change back to a smiling face before asking your name.

![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- When the **sprite is clicked**, your chatbot should first **switch costume** to a smiling face. \--- /hint \--- \--- hint \--- Here's the code block you'll need to add: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Challenge: more decisions

Program your chatbot to ask another question - something with a "yes" or "no" answer. Can you make your chatbot respond to the answer?

![screenshot](images/chatbot-joke.png) \--- /challenge \---