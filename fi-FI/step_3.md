## Puhuva chatbot

Nyt kun sinulla on chatbot, jolla on persoonallisuus, aiot ohjelmoida sen keskustelemaan kanssasi.

\--- tehtävä \---

Napsauta chatbot-spriteäsi ja lisää tämä koodi siihen, että `kun sitä napsautetaan`{: class = "block3events"}, `pyytää nimeäsi`{: class = "block3sensing"} ja sitten `sanoo: kaunis nimi! "`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota
sanoa [Mikä ihana nimi!] (2) sekunniksi
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa koodi napsauttamalla chatbotia. Kun chatbot pyytää nimeäsi, kirjoita se ruudun alareunassa olevaan ruutuun ja napsauta sinistä merkkiä tai paina <kbd>Enter</kbd>.

![ChatBot-vastauksen testaus](images/chatbot-ask-test1.png)

![ChatBot-vastauksen testaus](images/chatbot-ask-test2.png)

\--- / tehtävä \---

\--- tehtävä \---

Juuri nyt chatbot vastaa "Mikä ihana nimi!" joka kerta, kun vastaat. Voit tehdä chatbotin vastauksen henkilökohtaisemmaksi, niin että vastaus on erilainen aina, kun kirjoitetaan eri nimi.

Muuta chatbot-sprite-koodia `jäseneksi`{: class = "block3operators"} "Hi" ja `vastaus`{: class = "block3sensing"} kohtaan "Mikä on nimesi?" kysymys, jotta koodi näyttää tältä:

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota
sanoa (liity [Hi] (vastaus) :: +) (2) sekunniksi
```

![Henkilökohtaisen vastauksen testaaminen](images/chatbot-answer-test.png)

\--- / tehtävä \---

\--- tehtävä \---

Kun tallennat vastauksen **muuttujaan**, voit käyttää sitä missä tahansa projektissasi.

Luo uusi muuttuja nimeltä `nimi`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- tehtävä \---

Vaihda chatbot sprites -koodisi ja aseta `nimi`{: class = "block3variables"} muuttujaksi `vastaus`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
kun tämä sprite napsautti
kysy [Mikä on nimesi?] ja odota

+ asettaa [nimi v] (vastaus)
sanomaan (liity [Hi] (nimi :: muuttujat +)) (2) sekunniksi
```

Koodisi pitäisi toimia kuten aikaisemmin: chatbotin pitäisi sanoa hei käyttämällä kirjoittamaasi nimeä.

![Henkilökohtaisen vastauksen testaaminen](images/chatbot-answer-test.png)

\--- / tehtävä \---

Testaa ohjelma uudelleen. Huomaa, että kirjoittamasi vastaus tallennetaan `nimen`{: class = "block3variables"} muuttujaan, ja se näkyy myös näyttämön vasemmassa yläkulmassa. Jotta se katoaisi vaiheesta, siirry kohtaan `Data`{: class = "block3variables"} ja napsauta `nimen`{: class = "block3variables"} vieressä olevaa ruutua niin, ettei se ole merkitty.