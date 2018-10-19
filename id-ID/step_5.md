## Langkah 3: Membuat keputusan

Kamu dapat memprogram chatbot untuk memutuskan balasan atau tindakan dia berdasarkan jawaban kamu terhadap pertanyaannya.

\--- task \---

Dapatkah kamu membuat chatbot bertanya "Apakah kamu sehat?", dan mengkodekan balasan, "Senang mendengarnya!" hanya **jika** pengguna menjawab "ya"?

Untuk menguji kode baru dengan benar, kamu harus mengujinya **dua kali**, sekali dengan jawaban "ya", dan sekali dengan jawaban "tidak".

Chatbot kamu harus membalas "Senang mendengarnya!" jika kamu menjawab "ya", tetapi tidak mengatakan apa pun jika kamu menjawab "tidak".

![Menguji balasan chatbot](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Setelah chatbot mengatakan "Halo", dia juga harus **menanyakan** "Apakah kamu sehat?". **Jika** kamu menjawab "ya", maka chatbot harus **mengatakan** "Senang mendengarnya!". \--- /hint \--- \--- hint \--- Berikut adalah blok kode tambahan yang kamu perlukan: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Berikut adalah tampilan seharusnya dari kode kamu: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Saat ini, chatbot kamu tidak mengatakan apa-apa jika kamu menjawab "tidak". Dapatkah kamu mengubah chatbot kamu untuk membalas "Oh tidak!" jika kamu menjawab "tidak" untuk pertanyaannya?

Uji dan simpan. Chatbot kamu sekarang harus mengatakan "Oh tidak!" jika kamu menjawab "tidak". Bahkan, dia akan mengatakan "Oh tidak!" jika kamu menjawab dengan apa pun selain "ya" (bagian **jika tidak** dalam blok `jika... maka / jika tidak` berarti **selain** itu).

![Menguji jawaban ya atau tidak](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Chatbot kamu sekarang harus mengatakan "Senang mendengarnya!" **jika** jawaban kamu "ya", tapi harus mengatakan "Oh tidak!" jika menjawab **selain** itu. \--- /hint \--- \--- hint \--- Berikut adalah blok kode yang kamu perlukan: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Berikut adalah tampilan seharusnya dari kode kamu: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Kamu dapat menaruh kode lain di dalam blok `jika... maka / jika tidak`, bukan hanya kode untuk membuat chatbot berbicara. Jika kamu mengklik tab **Kostum** pada chatbot, kamu akan melihat bahwa dia memiliki lebih dari satu kostum.

![kostum chatbot](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Dapatkah kamu mengubah kostum chatbot agar sesuai dengan jawaban kamu?

Uji dan simpan. Kamu harus melihat perubahan wajah chatbot tergantung pada jawaban kamu.

![Menguji kostum yang berubah](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Chatbot kamu sekarang harus juga **berganti kostum** tergantung pada jawaban yang diberikan. \--- /hint \--- \--- hint \--- Berikut adalah kode blok yang kamu perlukan: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Berikut adalah tampilan seharusnya dari kode kamu: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Sudahkah kamu melihat bahwa kostum chatbot kamu tetap sama dengan yang kamu ganti terakhir kali kalian berbicara? Dapatkah kamu memperbaikinya?

![Isu kostum](images/chatbot-costume-bug-test.png)

Uji dan simpan: Jalankan kode dan ketik "tidak" agar chatbot kamu terlihat prihatin. Ketika kamu menjalankan kode lagi, chatbot harus berganti tersenyum kembali sebelum menanyakan nama.

![Menguji perbaikan kostum](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- Ketika **sprite ini diklik**, chatbot awalnya harus ber**ganti kostum** ke muka tersenyum. \--- /hint \--- \--- hint \--- Berikut adalah blok kode yang kamu perlukan: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Berikut tampilan seharusnya dari kode kamu: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Tantangan: keputusan tambahan

Program chatbot kamu untuk menanyakan hal lain - dengan jawaban "ya" atau "tidak". Dapatkah kamu membuat chatbot membalas jawaban itu?

![tangkapan layar](images/chatbot-joke.png) \--- /challenge \---