## Un chatbot parlanchín

Ahora que tienes un chatbot con personalidad, vamos a programarlo para que hable contigo.

\--- task \---

Haz clic en el sprite de tu chatbot y agregue este código para que ` cuando haga clic ` {: class = "block3events"}, ` te pregunte tu nombre ` {: class = "block3sensing"} y luego ` diga "¡Qué nombre más bonito!" ` {: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
cuando se hace clic en este sprite
pregunta [¿Cuál es tu nombre?] y espera
diga [¡Qué nombre más bonito!] durante (2) segundos
```

\--- /task \---

\--- task \---

Haz clic en tu chatbot para probar tu código. Cuando el chatbot pida tu nombre, escríbelo en el cuadro que aparece en la parte inferior del escenario, y luego haz clic en la marca azul, o pulsa <kbd> Enter </kbd>.

![Comprobando una respuesta del chatbot](images/chatbot-ask-test1.png)

![Testing a ChatBot response](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Ahora mismo, tu chatbot contesta "¡Qué nombre más bonito!" cada vez que respondes. Puedes hacer que la respuesta del chat sea más personal, para que la respuesta sea diferente cada vez que se escriba un nombre diferente.

Cambia el código del sprite de tu chatbot a `unir`{:class="block3operators"} "Hola" con la `respuesta`{:class="block3sensing"} a la pregunta "¿Cómo te llamas?", de modo que el código se parezca a esto:

![nano sprite](images/nano-sprite.png)

```blocks3
cuando se hace clic en este sprite
pregunta [¿Cuál es tu nombre?] y espera
di (unir [Hola ] (respuesta) :: +) durante (2) segundos
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Almacenando la respuesta en una **variable**, puedes usarla en cualquier lugar del proyecto.

Crea una nueva variable llamada `nombre`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Ahora, cambia el código del sprite de tu chatbot para poner el valor de la variable `nombre`{:class="block3variables"} a `respuesta`{:class="block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
cuando se hace click en este sprite 
pregunta [¿Cómo te llamas? y espera

+ pon el valor de [nombre v] a (respuesta)
di (unir [Hola ] (nombre :: variables +)) durante (2) segundos
```

Tu código debería funcionar como antes: tu chatbot debería decir hola usando el nombre que escribiste.

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

Prueba tu programa de nuevo. Ten en cuenta que la respuesta que escribes está almacenada en la variable `name`{:class="block3variables"}, y también se muestra en la esquina superior izquierda del Escenario. Para que desaparezca del Escenario, ve a `Variables`{:class="block3variables"} en la sección de bloques y haz clic en la caja junto a `nombre`{:class="block3variables"} para que quede desmarcada.