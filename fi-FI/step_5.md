## Vaihe 3: Päätökset

Voit ohjelmoida chatbotsi päättää, mitä sanoa tai tehdä vastausten perusteella kysymyksiisi.

+ Voitteko tehdä chatbot kysyä "Oletko kunnossa?" Ja koodata sitä vastaamaan "Se on hienoa kuulla!" vain **jos** käyttäjä vastaa "kyllä"?
    
    Testaa uusi koodi kunnolla, kokeile sitä **kahdesti**, kerran vastauksella "kyllä" ja kerran vastauksella "ei".
    
    Chatbotisi pitäisi vastata "Se on hienoa kuulla!" jos vastaat "kyllä", mutta älä sano mitään, jos vastaat "ei".
    
    ![Chatbot-vastauksen testaaminen](images/chatbot-if-test.png)

\--- vinkit \--- \--- vinkki \--- Kun chatbot on sanonut "Hi", sen pitäisi nyt myös **kysyä** "Oletko kunnossa?". **Jos** vastaa "kyllä", chatbotin pitäisi **sanoa** "Se on hienoa kuulla!". \--- / hint \--- \--- vinkki \--- Tässä on tarvittavia ylimääräisiä koodilohkoja: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- / hint \--- \--- vinkki \--- Näin koodisi pitäisi näyttää: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- / hint \--- \--- / vinkit \---

+ Tällä hetkellä chatbot ei sano mitään, jos vastaat "ei". Voitko vaihtaa chatbota niin, että se vastaa myös "Oh no!" jos vastaat kysymykseenne "ei"?
    
    Testaa ja tallenna. Chatbotisi pitäisi nyt sanoa "Oh no!" jos vastaat "ei". Itse asiassa se sanoo "Ei!" jos vastaat muuta kuin "kyllä" ( **muuten** `jos / muut` estää **muuten**).
    
    ![Kyllä / ei vastauksen testaaminen](images/chatbot-if-else-test.png)

\--- vinkkejä \--- \--- vinkka \--- Sinun chatbot pitäisi nyt sanoa "Se on hienoa kuulla!" **jos** vastauksesi on "kyllä", mutta sen pitäisi sanoa "Oh no!" jos vastaat jotain **muuten**. \--- / hint \--- \--- vinkki \--- Tässä on koodilohkot, joita sinun on käytettävä: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- / hint \--- \--- vinkki \--- Näin sinun koodisi pitäisi näyttää: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- / hint \--- \--- / vinkit \---

+ Voit laittaa minkä tahansa koodin `if / else` -lohkoon, ei pelkästään koodiin, jotta chatbotisi puhuisi. Jos napsautat chatbotin **Puku** -välilehteä, näet, että sillä on useampi kuin yksi puku.
    
    ![chatbot-puvut](images/chatbot-costume-view.png)

+ Voitko vaihtaa chatbotin puku vastaamaan vasteesi?
    
    Testaa ja tallenna. Sinun pitäisi nähdä chatbotin kasvot vaihtelevat vastauksen mukaan.
    
    ![Testaa muuttuva puku](images/chatbot-costume-test.png)

\--- vinkit \--- \--- vinkka \--- Chatbotisi pitäisi nyt myös **vaihtaa puku** riippuen annetusta vastauksesta. \--- / hint \--- \--- vinkki \--- Tässä on koodilohkot, joita sinun on käytettävä: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- / hint \--- \--- vinkki \--- Näin sinun koodisi pitäisi näyttää: ![Code for a changing costume](images/chatbot-costume-code.png) \--- / hint \--- \--- / vinkit \---

+ Oletko huomannut, että chatbotin puku pysyy samana, että se muuttui viimeksi kun puhut siihen? Voitko korjata tämän ongelman?
    
    ![Pukusäätö](images/chatbot-costume-bug-test.png)
    
    Testaa ja tallenna: Suorita koodisi ja kirjoita "ei", jotta chatbotisi näyttää onnettomalta. Kun käytät koodia uudelleen, chatbot-tilisi tulee vaihtaa hymyileviin kasvoihin ennen kuin kysyy nimeäsi.
    
    ![Pukusuhteen testaaminen](images/chatbot-costume-fix-test.png)

\--- vinkit \--- \--- vinkki \--- Kun **spriteä napsautetaan**, chatbotin tulee ensin **vaihtaa puku** hymyileviin kasvoihin. \--- / hint \--- \--- vinkki \--- Tässä on koodilohko, jonka sinun on lisättävä: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- / hint \--- \--- vinkki \--- Näin koodisi pitäisi näyttää: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- / hint \--- \--- / vinkit \---

\--- haaste \---

## Haaste: enemmän päätöksiä

Voit ohjelmoida chatbotisi kysymään toisen kysymyksen - jotain "kyllä" tai "ei" vastausta. Voitteko soittaa chatbotisi vastaamaan vastaukseen?

![kuvakaappaus](images/chatbot-joke.png) \--- /haaste \---