## Döntéshozatal

Beállíthatod a chatbotot úgy, hogy eldöntse, mit kell tennie a kapott válaszok alapján.

Először módosítsd a chatbotodat úgy, hogy olyan kérdést tegyen fel, amelyre "igen" vagy "nem" lehet a válasz.

\--- task \---

Változtasd meg a chatbot kódját! A chatbot-nak fel kell tennie a következő kérdést "Jól vagy ", a `név`{:class="block3variables"} változó használatával. Aztán válaszolnia kell úgy, hogy "Ezt jó hallani!" `ha`{:class="block3control"} a kapott válasz "igen", de ne mondjon semmit, ha a válasz "nem".

![A chatbot válasz tesztelése](images/chatbot-if-test1-annotated.png)

![A chatbot válasz tesztelése](images/chatbot-if-test2.png)

![nano jelmez](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
kérdezd [Mi a neved?] és várj
[név v] legyen (válasz)
mondd: ([Szia ] és (név) összefűzve) (2) másodpercig
kérdezd ([Jól vagy ] és (név) összefűzve) és várj
ha <(válasz) = [igen]> akkor 
  mondd: [Ezt jó hallani!] (2) másodpercig
end
```

Az új kód helyes teszteléséhez **két próbát kell tenned**: egyszer az "igen" legyen a válasz, és másodszor pedig a "nem".

\--- /task \---

Jelenleg a chatbot nem mond semmit a "nem" válaszra.

\--- task \---

Változtasd meg a chatbot kódját úgy, hogy "Ó, nem!"-et mondjon, ha "nem"-mel válaszolsz a "Jól vagy" kérdésre.

Cseréld ki a `ha, akkor`{:class="block3control"} blokkot egy `ha, akkor, különben`{:class="block3control"} blokkra, ami ez tartalmazzon egy `mondd: "Ó, nem!"`{:class="block3looks"} kódot is, így a chatbot így már mindkét válaszodra tud reagálni.

![nano sprite](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
kérdezd [Mi a neved?] és várj
[név v] legyen (válasz)
mondd: ([Szia ] és (név) összefűzve) (2) másodpercig
kérdezd ([Jól vagy ] és (név) összefűzve) és várj
ha <(válasz) = [igen]> akkor 
  mondd: [Ezt jó hallani!] (2) másodpercig
különben 
  mondd: [Ó, nem!] (2) másodpercig
end
```

\--- /task \---

\--- task \---

Próbáld ki a kódod. Különböző válaszokat kell kapnod. Ha "igen"-nel (kis- és nagybetűk használatától függetlenül) válaszolsz a chatbotodnak "Ezt jó hallani!"-t kell mondania és "Ó, nem!"-et, ha **mást írsz be**.

![A chatbot válasz tesztelése](images/chatbot-if-test2.png)

![Igen/nem válasz tesztelése](images/chatbot-if-else-test.png)

\--- /task \---

Bármely kódot beírhatsz egy `ha, akkor, különben`{:class="block3control"} blokkba, nem csak olyat, amitől a chatbotod válaszol.

Ha rákattintasz a chatbot **Jelmezek** lapjára, látni fogod, hogy több jelmeze is van.

![chatbot jelmezek](images/chatbot-costume-view-annotated.png)

\--- task \---

Változtasd meg a chatbotod kódját úgy, hogy a chatbot válasszon a jelmezek közül, amikor beírsz egy választ.

![Változó jelmez tesztelése](images/chatbot-costume-test1.png)

![Változó jelmez tesztelése](images/chatbot-costume-test2.png)

Módosítsd a `ha, akkor, különben`{:class="block3control"} blokkot a `jelmez legyen`{:class="block3looks"} blokk hozzáadásával.

![nano jelmez](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
kérdezd [Mi a neved?] és várj
[Név v] legyen (válasz)
mondd: ([Szia ] és (Név) összefűzve) (2) másodpercig
kérdezd ([Jól vagy ] és (Név) összefűzve) és várj
ha <(válasz) = [igen]> akkor 
  jelmez legyen (nano-c v)
  mondd: [Ezt jó hallani!] (2) másodpercig
különben 
  jelmez legyen (nano-d v)
  mondd: [Ó nem!] (2) másodpercig
end
```

Próbáld ki és mentsd le a kódot. Azt kell majd látnod, hogy a chatbot arca a válaszától függően változik.

\--- /task \---

Észrevetted, hogy a chatbot jelmezének megváltozása után ez így is marad, és nem tér vissza az elsőre?

Ezt kipróbálhatod így: futtasd a kódot, és válaszolj "nem"-mel, hogy a chatbotod arcát boldogtalanra változzon. Ezután futtasd újra a kódját, és vedd észre, hogy a chatbot nem változik vissza mosolygósra, mielőtt megkérdezi a neved.

![Jelmezhiba](images/chatbot-costume-bug-test.png)

\--- task \---

A probléma megoldásához a chatbot kódjához tedd a `jelmez legyen`{: lass="block3looks"} blokkot a `ezen szereplőre kattintáskor`{:class="block3events"} blokk mögé.

![nano jelmez](images/nano-sprite.png)

```blocks3
ezen szereplőre kattintáskor
jelmez legyen (nano-a v)
kérdezd [Mi a neved?] és várj
```

![A jelmezhiba javításának tesztelése](images/chatbot-costume-fix-test.png)

\--- /task \---