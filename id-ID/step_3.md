## Chatbot yang bisa bicara

Sekarang Anda memiliki chatbot dengan kepribadian, Anda akan memprogramnya untuk berbicara dengan Anda.

\--- tugas \---

Klik sprite chatbot Anda, dan tambahkan kode ini ke `sehingga ketika diklik`{: class = "block3events"}, `meminta nama Anda`{: class = "block3sensing"} dan kemudian `berkata "What a a nama yang bagus!"`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
ketika sprite ini diklik
tanyakan [Siapa namamu?] dan tunggu
katakan [Nama yang bagus!] selama (2) detik
```

\--- /tugas \---

\--- tugas \---

Klik pada chatbot Anda untuk menguji kode Anda. Saat chatbot menanyakan nama Anda, ketikkan ke dalam kotak yang muncul di bagian bawah Stage, lalu klik pada tanda biru, atau tekan <kbd>Enter</kbd>.

![Menguji tanggapan ChatBot](images/chatbot-ask-test1.png)

![Menguji tanggapan ChatBot](images/chatbot-ask-test2.png)

\--- /tugas \---

\--- tugas \---

Saat ini, chatbot Anda menjawab "Nama yang sangat bagus!" setiap kali Anda menjawab. Anda dapat membuat balasan chatbot lebih pribadi, sehingga balasannya berbeda setiap kali nama yang berbeda diketik.

Ubah kode sprite obrolan menjadi `bergabung dengan`{: class = "block3operators"} "Hai" dengan `jawaban`{: class = "block3sensing"} ke "Siapa namamu?" pertanyaan, sehingga kode tersebut terlihat seperti ini:

![nano sprite](images/nano-sprite.png)

```blocks3
ketika sprite ini diklik
tanyakan [Siapa namamu?] dan tunggu
katakan (gabung [Hai] (jawab) :: +) selama (2) detik
```

![Menguji balasan yang dipersonalisasi](images/chatbot-answer-test.png)

\--- /tugas \---

\--- tugas \---

Dengan menyimpan jawaban dalam **variabel**, Anda dapat menggunakannya di mana saja proyek Anda.

Buat variabel baru yang disebut `nama`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- tugas \---

Sekarang, ubah kode sprite chatbot Anda untuk menetapkan `nama`{: class = "block3variables"} variabel menjadi `jawaban`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
ketika sprite ini diklik
tanyakan [Siapa namamu?] dan tunggu

+ set [nama v] menjadi (jawab)
katakan (gabung [Hai] (nama :: variabel +)) selama (2) detik
```

Kode Anda harus berfungsi seperti sebelumnya: chatbot Anda harus menyapa menggunakan nama yang Anda ketikkan.

![Menguji balasan yang dipersonalisasi](images/chatbot-answer-test.png)

\--- /tugas \---

Uji kembali program Anda. Perhatikan bahwa jawaban yang Anda ketikkan disimpan dalam variabel `name`{: class = "block3variables"}, dan juga ditampilkan di sudut kiri atas Stage. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.