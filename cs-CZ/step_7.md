## Změna polohy

Můžete také nastavit svůj chatbot, abyste změnili jeho polohu!

![Testování měnící se pozadí](images/chatbot-backdrop-moon.png)

\--- task \---

Můžete naplánovat svůj chatbot a zeptat se "Chcete jít na Měsíc", a pak změňte pozadí, když je odpověď "ano"?

\--- tipy \---

\--- hint \---

Váš Chatbot měla `ptát „Ty chceš jít na Měsíc?“`{: class = "block3sensing"} a `pokud`{: class = "block3control"} `odpovědí`{: class = "block3sensing"} ano, `by měl přepnout pozadí na měsíc`{ class = "block3looks"}.

\--- /tip \---

\--- hint \---

Zde jsou blokové kódy, které musíte přidat do kódu chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
přepnout zpět na (měsíc v)

požádat [Chcete jít na Měsíc?] a počkat

pokud <(odpověď) = [yes]> pak 

konce
```

\--- /tip \---

\--- hint \---

Tak by měl vypadat váš kód:

```blocks3
zeptejte se [chcete jít na Měsíc?] a počkat
pokud <(odpověď) = [yes]> pak 
  spínající pozadí na (měsíc v)
konce
```

\--- /tip \---

\--- /tipy \---

\--- /task \---

\--- task \---

Nyní se musíte ujistit, že vaše chatbot se spustí na správném místě, když na ni kliknete a promluvíte si s ním. Přidejte tento blok do horní části kódu chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
kdy tento sprite kliknul

+ přepnout zpět na (prostor v)
```

\--- /task \---

\--- task \---

Otestujte svůj program a odpovězte "ano", když se chatbot zeptá, jestli chcete jít na Měsíc. Měli byste vidět, že se místo chatbotu změní.

\--- /task \---

\--- task \---

Můžete také přidat následující kód do nového bloku `if`: {class = "block3control"}, pokud chcete odpovědět "yes" čtyřikrát nahoru a dolů.

![nano sprite](images/nano-sprite.png)

```blocks3
pokud <(odpověď) = [yes]> potom 
  spínací kulisu (měsíc v)

+ opakování (4) 
    změna y podle (10),
    čekací (0,1) sekund
    změna y od (-10)
    čekací (0,1) sekund
  konec
konce
```

\--- /task \---