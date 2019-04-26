## Un chatbot que habla

Ahora que tienes un chatbot con una personalidad, lo vas a programar para hablar contigo.

\--- tarea \---

Haga clic en su personaje y añada este código para que `cuando le haga clic en`{:class="block3events"}, le `pida su nombre`{:class="block3sensing"} y luego `diga "¡Qué nombre tan encantador!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
cuando le haga clic a su personaje
pregunte [¿Cuál es su nombre?] y espere
diga [¡Qué nombre tan bonito!] por (2) segundos
```

\--- / tarea \---

\--- tarea \---

Haga clic en su chatbot para probar su código. Cuando el chatbot pregunte por su nombre, escríbalo en el cuadro que aparece en la parte inferior del escenario y luego haga clic en la marca azul o presione <kbd> Entrar </kbd>.

![Probando una respuesta del ChatBot](images/chatbot-ask-test1.png)

![Probando una respuesta del ChatBot](images/chatbot-ask-test2.png)

\--- / tarea \---

\--- tarea \---

Ahora mismo, tu chatbot responde "¡Qué nombre encantador!" cada vez que contestas. Puedes hacer que la respuesta del chatbot sea más personal, de modo que la respuesta sea diferente cada vez que se escriba un nombre diferente.

Cambia el código del personaje de tu chatbot a ` unirse ` {: class = "block3operators"} "Hola" con la respuesta ` ` {: class = "block3sensing"} al "¿Cuál es tu nombre?" Pregunta, para que el código se vea así:

![nano sprite](images/nano-sprite.png)

```blocks3
cuando le de click a su personaje 
pregunte [¿Cuál es su nombre?] y espere
respuesta (join [Hola] (respuesta) :: +) durante (2) segundos
```

![Probando una respuesta personalizada](images/chatbot-answer-test.png)

\--- / tarea \---

\--- tarea \---

Guardando la respuesta en una variable ****, puedes usarla en cualquier parte de tu proyecto.

Crear una nueva variable llamada nombre ` ` {: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- / tarea \---

\--- tarea \---

Ahora, cambie el código de su chatbot para establecer el nombre ` ` {: class = "block3variables"} variable para ` responder ` {: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
cuando le haga clic a su chatbot
pregunte [¿Cuál es su nombre?] y espere

+ configurar [nombre v] a (responder)
decir (unirse a [Hola] (nombre :: variables +)) durante (2) segundos
```

Tu código debería funcionar como antes: tu chatbot debería decir hola usando el nombre que escribes.

![Probando una respuesta personalizada](images/chatbot-answer-test.png)

\--- / tarea \---

Prueba tu programa de nuevo. Tenga en cuenta que la respuesta que escriba se almacena en la variable `name`{:class="block3variables"} y también se muestra en la esquina superior izquierda de la etapa. Para que desaparezca del Stage, vaya a la sección `Data`{:class="block3variables"} y haga clic en el cuadro junto a `name`{:class="block3variables"} para que no esté marcado.