## Adım 3: Qərarların alınması

Suallarınıza cavablarınıza əsaslanaraq nə demək və ya qərar verməyə qərar vermək üçün söhbət proqramınızı tərtib edə bilərsiniz.

+ Çatqoşa verə bilərikmi "Siz yaxşısınız?" Sualını soruşa bilərsiniz və cavab vermək üçün kodu "Eşitmək çox xoşdur!" **əgər** istifadəçi "yes" cavabını verirsə?
    
    Yeni kodunuzu düzgün sınaqdan keçirmək üçün onu **iki dəfə**, bir dəfə "yes" cavabını və bir dəfə "yox" cavabını test etməliyəm.
    
    Sizin cavab vermiş olduğunuz şifrə "Bu eşitmək çox xoşdur!" "bəli" cavabını verirsənsə, yoxsa "yox" deyə cavab verə bilməyəcəksiniz.
    
    ![Bir chatbot cavab test](images/chatbot-if-test.png)

\--- İpuçları \--- \--- ipucu \--- Çatibənizin "Salam" dedikdən sonra, indi də **** "Yaxşısınızmı?" **** "yes" cavabını verdiyiniz halda, chatbot **deməlidir** "Bu eşitmək böyük!". \--- / ipucu \--- \--- işarə \--- Sizə lazım olan əlavə kod blokları: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- / hint \--- \--- ipucu \--- Kodunuz necə olmalıdır: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- / ipucu \--- \--- / göstərişlər \---

+ Halbuki "cavabsız" cavab verdiyiniz halda, chatbot heç bir şey demir. Çatqaz blokunuzu dəyişdirə bilərsinizmi ki, o da "Oh no!" Cavab verir. sualına "yox" cavab verərsən?
    
    Test edin və qənaət edin. Çatdırılmağınız artıq "Oh no!" "yox" deyə cavab verirsən. In fact, it will say "On no!" if you answer with anything other than "yes" (the **else** in an `if/else` block means **otherwise**).
    
    ![Bəli / yox cavab test](images/chatbot-if-else-test.png)

\--- İpuçları \--- \--- ipucu \--- Sizin chatbot indi demək lazımdır "Bu eşitmək üçün böyük!" **cavabınız "yes" isə** isə "Oh no!" **başqa bir cavabınız varsa**. \--- / ipucu \--- \--- ipucu \--- İşdə istifadə etmək üçün lazım olan kod blokları: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- / hint \--- \--- ipucu \--- Kodunuzun necə görünməsi lazımdır: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- / ipucu \--- \--- / göstərişlər \---

+ `if / else` bloku daxilində hər hansı bir kodu yaza bilərsiniz. Sohbet bloğunuzun **Costume** sekmesini tıklasanız, birdən çox kostyum olduğunu görürsünüz.
    
    ![chatbot kostyumları](images/chatbot-costume-view.png)

+ Cavabınıza uyğun olaraq chatbotun kostyumunu dəyişə bilərsinizmi?
    
    Test edin və qənaət edin. Cavabınıza uyğun olaraq, chatbotun üzünü dəyişməlisiniz.
    
    ![Değişen kostyumu test etmə](images/chatbot-costume-test.png)

\--- İpuçları \--- \--- ipucu \--- Verdiyiniz cavabdan asılı olaraq chatbotunuz da **kostyum kostyumunu** qoymalıdır. \--- / ipucu \--- \--- ipucu \--- İşdə istifadə etmək üçün lazım olan kod blokları: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- / hint \--- \--- ipucu \--- Kodunuzun necə görünməsi lazımdır: ![Code for a changing costume](images/chatbot-costume-code.png) \--- / ipucu \--- \--- / göstərişlər \---

+ Çatqbotunuzun kostyumunun sonuncu dəfə dəyişdiyini dəyişdiyini fərq etdinizmi? Bu problemi düzəldə bilərsinizmi?
    
    ![Kostyum səhv](images/chatbot-costume-bug-test.png)
    
    Test edin və qeyd edin: Sizin kodunuzu işləyin və "yox" yazın, çünki söhbətiniz bədbəxt görünür. Kodunuzu yenidən çalıştırdığınızda, ismarıcınızı soruşmadan əvvəl, chatbotunuz gülümsəyən bir üzə dönməlidir.
    
    ![Kostyum düzəltmə testi](images/chatbot-costume-fix-test.png)

\--- ipuçları \--- \--- ipucu \--- **sprite**tıklandığında, chatbotunuz ilk olaraq **kostyum kostümünü** gülümseyen bir üzə keçməlidir. \--- / ipucu \--- \--- işarə \--- Əlavə etmək lazımdır kod blokudur: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- / hint \--- \--- ipucu \--- Kodunuzun necə görünməsi lazım: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- / ipucu \--- \--- / göstərişlər \---

\--- çağırış \---

## Çağırış: daha çox qərar

"Bəli" və ya "yox" cavabı ilə bir şey soruşmaq üçün chatbot proqramınızı hazırlayın. Çatışan cavab verməyə cavab verə bilərsinizmi?

![ekran görüntüsü](images/chatbot-joke.png) \--- / problem