## 3. Adım: Karar verme

Chatbot'unuzu, sorularına verdiğiniz yanıtlara dayanarak ne söyleyeceğinize veya ne yapacağınıza karar vermeniz için programlayabilirsiniz.

\--- görev \---

Chatbot'u "İyi misin?" Sorusunu sorabilir ve "Bunu duymak harika!" Sadece **ise** kullanıcı cevapları "evet"?

Düzgün Yeni kodu test etmek için, test etmeli **kez**kez cevap "evet" ve bir kez cevap "hayır" ile.

Sohbetçiniz cevap vermelidir "Bunu duymak harika!" "evet" cevabını verirsen, "hayır" diye cevaplarsan hiçbir şey söyleme.

![Bir chatbot cevabını test etme](images/chatbot-if-test.png)

\--- ipuçları \--- \--- ipucu \--- senin Chatbot söyledi sonra "Merhaba", şimdi de gerektiği **sormak** "İyi misin?". **ise** cevap "evet" ise Chatbot gerektiğini **söylemek** "Bunu duymak harika!". \--- / ipucu \--- \--- ipucu \--- İhtiyacınız olacak ekstra kod blokları: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- / ipucu \--- \--- ipucu \--- İşte kodunuzun nasıl göründüğü: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- / ipucu \--- \--- / ipuçları \---

\--- /görev \---

\--- görev \---

Şu anda chatbot "hayır" cevabını verirsen bir şey söylemez. Chatbot'unuzu değiştirerek "Oh no!" Eğer sorusuna "hayır" cevabını verirsen?

Test et ve kaydet. Sohbetçiniz artık "Ah hayır!" Demeli "hayır" diye cevaplarsan. Aslında, "Hayır!" (Eğer "evet" dışında herhangi bir şeyle cevap verirsen **else** bir in `/ else if` blok demektir **aksi**).

![Evet / hayır cevabı testi](images/chatbot-if-else-test.png)

\--- ipuçları \--- \--- ipucu \--- Sizin chatbotunuz artık "Bunu duymak harika!" **ise** Cevabınız "evet", ama demeliyim "Oh hayır!" Eğer başka bir şeye **cevap verirseniz**. \--- / ipucu \--- \--- ipucu \--- Kullanmanız gereken kod blokları şunlardır: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- / ipucu \--- \--- ipucu \--- İşte kodunuzun nasıl göründüğü: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- / ipucu \--- \--- / ipuçları \---

\--- /görev \---

\--- görev \---

Chatbot'unuzu konuşturmak için sadece kod değil, `if / else` bloğu içinde herhangi bir kod koyabilirsiniz. Chatbot'unuzun **Kostüm** sekmesini tıklarsanız, birden fazla kostümün olduğunu görürsünüz.

![chatbot kostümleri](images/chatbot-costume-view.png)

\--- /görev \---

\--- görev \---

Chatbot kostümünü cevabınıza göre değiştirebilir misiniz?

Test et ve kaydet. Yanıtınıza bağlı olarak chatbotunuzun yüzünü değiştirmelisiniz.

![Değişen bir kostümü test etme](images/chatbot-costume-test.png)

\--- ipuçları \--- \--- ipucu \--- Sizin chatbot ayrıca verilen cevaba bağlı olarak **kostüm** değiştirmelidir. \--- / ipucu \--- \--- ipucu \--- Kullanmanız gereken kod blokları şunlardır: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- / ipucu \--- \--- ipucu \--- İşte kodunuzun nasıl göründüğü: ![Code for a changing costume](images/chatbot-costume-code.png) \--- / ipucu \--- \--- / ipuçları \---

\--- /görev \---

\--- görev \---

Chatbot'unuzun kostümünün son konuştuğunuz zaman değiştiğini fark ettiniz mi? Bu sorunu çözebilir misin?

![Kostüm hatası](images/chatbot-costume-bug-test.png)

Test edin ve kaydedin: Kodunuzu çalıştırın ve "hayır" yazın, böylece sohbet arkadaşınız mutsuz görünür. Kodunuzu tekrar çalıştırdığınızda, adınızın sorulmasından önce chatbot'unuzun gülümseyen bir yüze dönüşmesi gerekir.

![Bir kostümün düzeltilmesini test etme](images/chatbot-costume-fix-test.png)

\--- ipuçları \--- \--- ipucu \--- Ne zaman **sprite tıklandığında**, senin Chatbot öncelikle şu **anahtar kostüm** gülümseyen yüzüne. \--- / hint \--- \--- hint \--- İşte eklemeniz gereken kod bloğu: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- / hint \--- \--- hint \--- İşte kodunuzun nasıl göründüğü: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- / ipucu \--- \--- / ipuçları \---

\--- /görev \---

\--- meydan okuma \---

## Zorluk: Daha fazla karar

Chatbot'unuzu başka bir soru sormak için programlayın - "evet" veya "hayır" cevabı olan bir şey. Chatbot'unuzun cevaba cevap vermesini sağlayabilir misiniz?

![ekran görüntüsü](images/chatbot-joke.png) \--- /meydan okuma \---