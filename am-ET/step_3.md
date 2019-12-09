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
ይህ ስፒት
ጠቅ ሲያደርግ 
 የት እንደሆነ (ስምህ ምንድን ነው?) እና
(2) ሰከንዶች (ሰላምታ (መልስ)) (+) ተቀበል
```

![ለግል የተበጀ ምላሽ ይሞክሩ](images/chatbot-answer-test.png)

\--- / task \---

\--- ተግባር \---

መልሱን በ **ተለዋዋጭ**በማስቀመጥ በማናቸውም ፕሮጀክትዎ ውስጥ ሊጠቀሙበት ይችላሉ.

`ስም`{: class = "block3variables"} የተባለ አዲስ ተለዋዋጭ ይፈጥራል.

[[[generic-scratch3-add-variable]]]

\--- / task \---

\--- ተግባር \---

አሁን የ `ስም`{: class = "block3variables"} ለ `መልስ`{: class = "block3sensing"} ለውጦችን ለማስቀመጥ የ chatbot sprites ኮድዎን ይቀይሩ:

![nano sprite](images/nano-sprite.png)

```blocks3
ይህ ስፒት
ሲጫኑ (ስምዎ ምንድ ነው?) እና

+ ስብስብ [ስም v] ወደ (መልስ)
ይጠብቁ (ሰላምታ (ስም :: ልዩ ልዩ +)) ለ 2 ሰከንዶች
```

የእርስዎ ኮድ ልክ እንደበፊቱ መስራት አለበት: የእርስዎ የሚተዋወቀው ስም ተጠቅመው ለውይይት ያነጋግሩ.

![ለግል የተበጀ ምላሽ ይሞክሩ](images/chatbot-answer-test.png)

\--- / task \---

ፕሮግራምዎን በድጋሚ ይሞክሩ. የሚተይቡት መልስ በ `ስም`{: class = "block3variables"} ተለዋዋጭ ውስጥ ተስተካክሎ በደረጃው ላይኛው ግራ ጠርዝ ላይ ይታያል. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.