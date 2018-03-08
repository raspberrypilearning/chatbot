## Cambiar la ubicación

También puedes programar a tu robot parlanchín para que cambie su ubicación.

+ Añade otro fondo a tu escenario, por ejemplo el fondo "moon" (luna).

	![screenshot](images/chatbot-moon.png)

+ Ahora puedes programar a tu robot parlanchín para que cambie de ubicación si le añades este código:

	```blocks
		preguntar [Me voy a la luna. ¿Quieres venir conmigo?] y esperar
		si ((respuesta) = [sí]) entonces
			cambiar fondo a [moon v]
		fin
	```

+ También debes asegurarte de que tu robot parlanchín esté fuera cuando empiezas a hablarle. Añade este bloque al principio del código de tu robot parlanchín:

	![screenshot](images/chatbot-outside.png)

+ Prueba tu programa, y contesta `sí` cuando te pregunte si quieres ir a la luna. La ubicación del robot parlanchín debería cambiar.

	![screenshot](images/chatbot-backdrop.png)

+ ¿Cambia de ubicación tu robot parlanchín si escribes `no`? ¿Y qué pasa si escribes `No estoy seguro`?

+ También puedes agregar este código dentro de tu bloque `si` {.blockcontrol}, para hacer que tu robot parlanchín salte 4 veces si la respuesta es `sí`:

	```scratch
	repetir (4)
		cambiar y por (10)
		esperar (0.1) segundos
		cambiar y por (-10)
		esperar (0.1) segundos
	fin
	```

	![screenshot](images/chatbot-loop.png)

+ Prueba tu código una vez más. ¿Salta tu robot parlanchín si contestas que `sí`?
