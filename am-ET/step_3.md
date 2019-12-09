## የሚያወራ የንግግር ሮቦት

አሁን የራሱ ጸባይ ያለው ሮቦት አላችሁ። ቀጥሎ ደግሞ እንዲያወራችሁ ልታደርጉት ነው።

\--- task \---

በቻትቦት ገጸ-ባህሪው ላይ ጠቅ አድርጉና ከዚያም የሚከተለውን እንዲያደርግ ይህን ኮድ ጨምሩበት፤ `ጠቅ ሲደረግ`{: class = "block3events"} `ስም ይጠይቃል`{: class = "block3sensing"} ከዚያም `"በጣም የሚያምር ስም! "`{: class = "block3looks"} ይላል።

![nano sprite](images/nano-sprite.png)

```blocks3
ይህ ስፕራይት ሲነካ
[ስም ማን ልበል?] ጠይቅና ጠብቅ
[በጣም የሚያምር ስም!] በል ለ (2) ሰከንዶች
```

\--- / task \---

\--- task \---

ኮዱን ለመሞከር በንግግር ሮቦቱ ላይ ጠቅ አድርጉ. ሮቦቱ ስም ሲጠይቅ ስማችሁን ከመድረኩ በታች ባለው ሳጥን ውስጥ ተይቡ፣ ከዚያም ሰማያዊውን ምልክት ጠቅ አድርጉ ወይም <kbd>Enter</kbd>ን ተጫኑ.

![የ ChatBot ምላሽ በመሞከር ላይ](images/chatbot-ask-test1.png)

![የ ChatBot ምላሽ በመሞከር ላይ](images/chatbot-ask-test2.png)

\--- / task \---

\--- task \---

አሁን የንግግር ሮቦቱ እናንተ በመለሳችሁ ቁጥር "በጥም ደስ የሚል ስም!" በማለት ይመልሳል። የሮቦቱን መልስ የበለጠ የግል እንዲሆን ለማድረግ, የተለያየ ስም በሚተየብበት ጊዜ የሮቦቱ መልስ የተለያየ እንዲሆን ማድረግ ይቻላል።

የንግግር ሮቦት ገጸ-ባህሪውን ኮድ እንደሚከተለው ለውጡት። "ሰላም" የሚለዉን "ስም ማን ልበል?" ከሚለው ጥያቄ `መልስ`{class = "block3operators"} ጋር `አገናኝ`{class = "block3operators"}።

![nano sprite](images/nano-sprite.png)

```blocks3
ይህ ስፕራይት ሲነካ
[ስም ማን ልበል?] ጠይቅና ጠብቅ
(አገናኝ [ሰላም!] (መልስ) :: +) ን በል ለ (2) ሰከንዶች
```

![ለግል የተበጀ ምላሽ ይሞክሩ](images/chatbot-answer-test.png)

\--- / task \---

\--- task \---

መልሱን በ **ተለዋዋጭ** በማስቀመጥ በፕሮጀክቱ ውስጥ ማንኛውም ቦታ መጠቀም ይቻላል።

`ስም`{: class = "block3variables"} የተባለ አዲስ ተለዋዋጭ ፍጠሩ።

[[[generic-scratch3-add-variable]]]

\--- / task \---

\--- task \---

አሁን `ስም`{: class = "block3variables"} የሚባለዉን ተለዋዋጭ ዋጋ ወደ `መልስ`{: class = "block3sensing"} ለመለወጥ የንግግር ሮቦቱን ኮድ ቀይሩት።

![nano sprite](images/nano-sprite.png)

```blocks3
ይህ ስፕራይት ሲነካ
[ስም ማን ልበል?] ጠይቅና ጠብቅ

[ስም v] ወደ (መልስ) ለውጥ
(አገናኝ [ሰላም!] (መልስ) :: +) ን በል ለ (2) ሰከንዶች
```

ኮዱ ልክ እንደበፊቱ መስራት አለበት። የንግግር ሮቦቱ ስማችሁን ተጠቅሞ ሰላም ማለት አለበት።

![ለግል የተበጀ ምላሽ ይሞክሩ](images/chatbot-answer-test.png)

\--- / task \---

ፕሮግራሙን በድጋሚ ሞክሩት። የጻፋችሁት መልስ `ስም`{: class = "block3variables"} የሚባለው ተለዋዋጭ ውስጥ መቀመጡን እንዲሁም በላይኛው ግራ ጠርዝ ላይ መታየቱን አስተውሉ። To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.