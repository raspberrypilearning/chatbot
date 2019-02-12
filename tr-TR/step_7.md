## Konum değiştirme

Chatbot'unuzu konumunu değiştirmek için de programlayabilirsiniz!

![Değişen bir zeminin test edilmesi](images/chatbot-backdrop-moon.png)

\--- task \---

Chatbotunuzu "Aya gitmek ister misiniz" diye sorabilir ve ardından cevap "evet" olduğunda fonu değiştirebilir misiniz?

\--- ipuçları \---

\---hint\---

Sohbetçiniz `sormalı "Aya gitmek ister misiniz?"`{: class = "block3sensing"} ve `ise`{: class = "block3control"} size `cevap`{: class = "block3sensing"} "evet", `fonu`aya dönüştürmeli sınıf = "block3looks"}.

\--- / ipucu \---

\---hint\---

İşte chatbot kodunuza eklemeniz gereken kod blokları.

![nano sprite](images/nano-sprite.png)

```blocks3
fonu değiştir (ay v)

isteyin [Ay'a gitmek ister misiniz?] ve <(cevap) = [yes]> sonra 

bitiyorsa

bekleyin
```

\--- / ipucu \---

\---hint\---

Bu, kodunuzun nasıl görünmesi gerektiğidir:

```blocks3
[? Eğer aya gitmek istiyorsunuz] sormak ve bekleyin
ise <(cevap) = [yes]> sonra 
  (ay v) geçiş zemin
ucunda
```

\--- / ipucu \---

\--- / ipuçları \---

\--- /görev \---

\--- task \---

Şimdi, onunla konuşmak için tıkladığınızda sohbetinizin doğru yerde başladığından emin olmanız gerekir. Bu bloğu chatbot kodunuzun en üstüne ekleyin:

![nano sprite](images/nano-sprite.png)

```blocks3
bu sprite

tıklandığında fonu değiştir (boşluk v)
```

\--- /görev \---

\--- task \---

Programınızı test edin ve chatbot aya gitmek isteyip istemediğinizi sorduğunda "evet" cevabını verin. Sohbetçi konumunun değiştiğini görmelisiniz.

\--- /görev \---

\--- task \---

Ayrıca " `" yanıtını verirseniz, chatbot'un dört kez aşağı ve yukarı zıplamasını sağlamak için aşağıdaki kodu yeni <code> eğer`{: class = "block3control"} bloğuna ekleyebilirsiniz:

![nano sprite](images/nano-sprite.png)

```blocks3
Eğer <(cevap) = [yes]> , sonra 
  (ay v) geçiş zemin

+ tekrar (4) 
    (10) ile değişim y
    bekleme (0.1) saniye
    (-10) ile değişikliği y
    bekleme (0.1) saniye
  son
son
```

\--- /task \---