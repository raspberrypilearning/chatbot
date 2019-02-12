## Mengubah lokasi

Anda juga dapat memprogram chatbot Anda untuk mengubah lokasinya!

![Menguji latar belakang yang berubah](images/chatbot-backdrop-moon.png)

\--- tugas \---

Bisakah Anda memprogram chatbot Anda untuk bertanya "Apakah Anda ingin pergi ke bulan", dan kemudian mengubah latar belakang ketika jawabannya adalah "ya"?

\--- petunjuk \---

\--- petunjuk \---

Chatbot Anda harus `bertanya "Apakah Anda ingin pergi ke bulan?"`{: class = "block3sensing"}, dan `jika`{: class = "block3control"} Anda `menjawab`{: class = "block3sensing"} "ya", seharusnya `harus mengganti latar belakang ke bulan`{: class = "block3looks"}.

\--- / petunjuk \---

\--- petunjuk \---

Berikut adalah blok kode yang perlu Anda tambahkan ke kode chatbot Anda.

![nano sprite](images/nano-sprite.png)

```blocks3
beralih latar belakang ke (bulan v)

tanyakan [Apakah Anda ingin pergi ke bulan?] dan tunggu

jika <(jawaban) = [yes]> lalu 

akhir
```

\--- / petunjuk \---

\--- petunjuk \---

Seperti inilah seharusnya kode Anda:

```blocks3
tanyakan [Apakah Anda ingin pergi ke bulan?] dan tunggu
jika <(jawaban) = [yes]> lalu 
  ubah latar belakang ke (bulan v)
ujung
```

\--- / petunjuk \---

\--- / petunjuk \---

\--- /tugas \---

\--- tugas \---

Sekarang Anda perlu memastikan bahwa chatbot Anda mulai di lokasi yang tepat ketika Anda mengkliknya untuk berbicara dengannya. Tambahkan blok ini ke bagian atas kode chatbot Anda:

![nano sprite](images/nano-sprite.png)

```blocks3
ketika sprite ini diklik

+ alihkan latar ke (spasi v)
```

\--- /tugas \---

\--- tugas \---

Uji program Anda, dan jawab "ya" ketika chatbot bertanya apakah Anda ingin pergi ke bulan. Anda harus melihat bahwa lokasi chatbot berubah.

\--- /tugas \---

\--- tugas \---

Anda juga dapat menambahkan kode berikut di dalam blok `jika`{: class = "block3control"} baru untuk membuat chatbot melompat-lompat empat kali jika Anda menjawab "ya":

![nano sprite](images/nano-sprite.png)

```blocks3
jika <(jawab) = [yes]> maka 
  beralih latar belakang ke (bulan v)

+ ulangi (4) 
    ubah y oleh (10)
    tunggu (0,1) dtk
    ubah y oleh (-10)
    tunggu (0,1) dtk
  end
end
```

\--- /tugas \---