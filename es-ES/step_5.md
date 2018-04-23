## Paso 3: Tomando decisiones

Puedes programar tu chatbot para que decida qué decir o hacer en función de tus respuestas a sus preguntas.

+ ¿Puedes hacer que el chatbot haga la pregunta "¿Estás bien?" Y añadir código para que responda "¡Qué bueno es escuchar eso!" solo ** si ** el usuario responde "sí"?
    
    Para probar tu nuevo código correctamente, debes probarlo ** dos veces **, una vez con la respuesta "sí", y una con la respuesta "no".
    
    Tu chatbot debería responder "¡Qué bueno es escucharlo!" si respondes "sí", pero no decir nada si respondes "no".
    
    ![Testing a chatbot reply](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Después de que tu chatbot haya dicho "hola", ahora también debería ** preguntar ** "¿Estas bien?". **Si** tu respuesta es "sí", entonces el chatbot debe **decir** "¡Qué bueno es escucharlo!". \--- / hint \--- \--- hint \--- Aquí están los bloques de código que necesitarás: <0 /> \--- / hint \--- \--- hint \--- Así es como debe ser tu código: <1 /> \--- / hint \--- \--- / hints \---

+ Por el momento, tu chatbot no dice nada si respondes "no". ¿Puedes cambiar tu chatbot para que también responda "¡Oh, no!" si respondes "no" a su pregunta?
    
    Prueba y guarda. Tu chatbot ahora debería decir "¡Oh, no!" si respondes "no". De hecho, dirá "¡Oh no!" si respondes con algo que no sea "sí" (el ** si no ** en un bloque ` si / si no ` significa ** en caso contrario **).
    
    ![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Tu chatbot ahora debería decir "¡Qué bueno es escucharlo!" ** si ** tu respuesta es "sí", pero debería decir "¡Oh, no!" si respondes algo ** diferente **. \--- / hint \--- \--- hint \--- Aquí están los bloques de código que necesitarás: <0 /> \--- / hint \--- \--- hint \--- Así es como debe ser tu código: <1 /> \--- / hint \--- \--- / hints \---

+ Puedes poner cualquier código dentro de un bloque ` si / si no `, no solo el código para hacer que tu chatbot hable. Si haces un clic en la pestaña ** disfraz ** de tu chatbot, verás que tiene más de un disfraz.
    
    ![chatbot costumes](images/chatbot-costume-view.png)

+ ¿Puedes cambiar el disfraz de chatbot para que coincida con tu respuesta?
    
    Prueba y guarda. Deberías ver que la cara de tu chatbot cambia según tu respuesta.
    
    ![Testing a changing costume](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Tu chatbot ahora también debería ** cambiar de disfraz ** dependiendo de la respuesta dada. \--- / hint \--- \--- hint \--- Aquí están los bloques de código que necesitarás: <0 /> \--- / hint \--- \--- hint \--- Así es como debe ser tu código: <1 /> \--- / hint \--- \--- / hints \---

+ ¿Has notado que el disfraz de tu chatbot sigue siendo el mismo al que cambió la última vez que hablaste con él? ¿Puedes arreglar este problema?
    
    ![Costume bug](images/chatbot-costume-bug-test.png)
    
    Prueba y guarda: Ejecuta tu código y escribe "no", para que tu chatbot parezca infeliz. Cuando vuelvas a ejecutar tu código, tu chatbot debería volver a tener una cara sonriente antes de preguntar tu nombre.
    
    ![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- Cuando **se hace un clic en el sprite **, tu chatbot primero debería ** cambiar el disfraz ** a una cara sonriente. \--- / hint \--- \--- hint \--- Aquí están los bloques de código que necesitarás: <0 /> \--- / hint \--- \--- hint \--- Así es como debe ser tu código: <1 /> \--- / hint \--- \--- / hints \---

\--- challenge \---

## Desafío: más decisiones

Programa tu chatbot para hacer otra pregunta, algo con una respuesta "sí" o "no". ¿Puedes hacer que tu chatbot responda a la respuesta?

![screenshot](images/chatbot-joke.png) \--- /challenge \---