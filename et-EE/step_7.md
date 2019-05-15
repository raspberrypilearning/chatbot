## Asukoha muutmine

Saate oma vestlusboti programmeerida ka selle asukoha muutmiseks!

![Muutuva tausta testimine](images/chatbot-backdrop-moon.png)

\--- ülesanne \---

Kas te saate oma vestlusboti programmeerida, et küsida "Kas sa tahad minna kuule" ja seejärel muuta tausta, kui vastus on "jah"?

\--- vihjed \---

\--- vihje \---

Teie chatbot peaks `küsida: "Kas sa tahad minna Kuule?"`{: class = "block3sensing"} ja `kui`{: class = "block3control"} te `vastus`{: class = "block3sensing"} "jah", peaks `lülitama kuu taustaks`: class = "block3looks"}.

\--- / vihje \---

\--- vihje \---

Siin on koodiplokid, mida peate oma chatbot koodile lisama.

![nano sprite](images/nano-sprite.png)

```blocks3
lülita taustaks (moon v)

küsi [Kas soovite minna kuu juurde?] ja oodake

kui <(vastus) = [yes]> siis 

lõpp
```

\--- / vihje \---

\--- vihje \---

Seda peaks teie kood välja nägema:

```blocks3
küsi [Kas sa tahad minna kuule?] ja oodata
kui <(vastus) = [yes]> seejärel 
  lüliti taustaks (kuu v)
lõpp
```

\--- / vihje \---

\--- / vihjed \---

\--- / ülesanne \---

\--- ülesanne \---

Nüüd peate veenduma, et teie vestlusbot algab õiges kohas, kui klõpsate sellele rääkida. Lisage see plokk teie vestlusboksi koodi ülaosale:

![nano sprite](images/nano-sprite.png)

```blocks3
kui see sprite klõpsas

+ lülita taustaks (tühik v)
```

\--- / ülesanne \---

\--- ülesanne \---

Testige oma programmi ja vastake "jah", kui vestlusbot küsib, kas soovite minna kuu. Sa peaksid nägema, et vestlusboti asukoht muutub.

\--- / ülesanne \---

\--- ülesanne \---

Uue `sse võite lisada ka järgmise koodi, kui`{: class = "block3control"} blokeerida, et vestlusbot hüpata üles ja alla neli korda, kui vastate "jah":

![nano sprite](images/nano-sprite.png)

```blocks3
kui <(vastus) = [yes]> siis 
  lüliti taustaks (kuu v)

+ korrata (4) 
    muutus y poolt (10)
    oota (0,1) sekundit
    muutus y (-10)
    oota (0,1) sekundit
  ots

```

\--- / ülesanne \---