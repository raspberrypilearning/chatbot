## Räägib jututuba

Nüüd, kui teil on isikupäraga jututuba, siis kavatsete programmeerida seda sinuga rääkima.

\--- ülesanne \---

Klõpsake oma vestlusbotil ja lisage see kood nii, et `kui seda klõpsatakse`{: class = "block3events"}, `küsib sinu nime`{: class = "block3sensing"} ja seejärel `ütleb: "Mis a armas nimi! "`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis su nimi on?] ja oodake
ütlema [Mis armas nimi!] (2) sekundit
```

\--- / ülesanne \---

\--- ülesanne \---

Koodi testimiseks klõpsake oma vestlusbotil. Kui chatbot küsib teie nime, tippige see väljale, mis kuvatakse lava allosas, ja seejärel klõpsake sinisel märgil või vajutage <kbd>Enter</kbd>.

![ChatBot'i vastuse testimine](images/chatbot-ask-test1.png)

![ChatBot'i vastuse testimine](images/chatbot-ask-test2.png)

\--- / ülesanne \---

\--- ülesanne \---

Just nüüd, teie vestlusbot vastab "Milline armas nimi!" iga kord, kui vastate. Saate muuta vestluspanu vastuse isiklikumaks, nii et vastus on erinev iga kord, kui sisestatakse mõni teine nimi.

Muutke chatbot sprite'i koodiks `liituda`{: class = "block3operators"} "Hi" `vastusega`{: class = "block3sensing"} "Mis su nimi on?" küsimus, nii et kood näeb välja selline:

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis su nimi on?] ja oodake
ütlema (liitu [Hi] (vastus) :: +) (2) sekundit
```

![Isikliku vastuse testimine](images/chatbot-answer-test.png)

\--- / ülesanne \---

\--- ülesanne \---

Kui salvestate vastuse **muutuja**, saate seda kasutada kõikjal, kus teie projekt on.

Loo uus muutuja nimega `name`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- / ülesanne \---

\--- ülesanne \---

Nüüd muutke oma chatbot spritese koodi `nime`{: class = "block3variables"} muutmiseks `vastuseks`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas
küsi [Mis on sinu nimi?] ja oodake

+ set [nimi v] (vastus)
(liituda [Hi] (nimi :: muutujad +)) (2) sekundit
```

Teie kood peaks toimima nii nagu varem: teie vestlusbot peaks ütlema hiirega, kasutades teie sisestatud nime.

![Isikliku vastuse testimine](images/chatbot-answer-test.png)

\--- / ülesanne \---

Testige oma programmi uuesti. Pange tähele, et vastus, mille sisestate, salvestatakse muutuja `nime`{: class = "block3variables"} ja seda näidatakse ka lava ülemises vasakus nurgas. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.