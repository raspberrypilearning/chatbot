## ሥፍራውን መለወጥ

እንዲሁም የውይይት መድረሻዎን ለመቀየር ቻት ያብጁ.

![ተለዋጭን የጀርባ ምስል በመሞከር ላይ](images/chatbot-backdrop-moon.png)

\--- ተግባር \---

"ወደ ጨረቃ መሄድ ትፈልጋላችሁ ወይ?" ለመጠየቅ ቻት ላትዎን መርጠው ማውጣት ይችላሉ, እና መልሱ «አዎ» ከሆነ የጀርባውን ለውጥ ይለውጡ?

\--- ምክሮች \---

\--- hint \---

የእርስዎ chatbot ይገባል `"ወደ ጨረቃ መሄድ ትፈልጋለህ?" ይጠይቁ`{: class = "block3sensing"}, እና `ከሆነ`: {class = "block3control"} እርስዎ `መልስ`: {class = "block3sensing"} "አዎ" ይህ ይገባል `ጨረቃ ወደ የጀርባ መቀየር`{: class = "block3looks"}.

\--- /hint \---

\--- hint \---

ወደ ቻትቦድ ኮዴዎ ለመጨመር የሚያስፈልጉዎትን የቁጥር ቁልፎች እዚህ አሉ.

![nano sprite](images/nano-sprite.png)

```blocks3
backdrop ወደ (moon v) ይቀይሩ

ጥያቄ [ወደ ጨረቃ ሄደው መሄድ ይፈልጋሉ?]

እና <ከሆነ (መልስ) = [yes]> እና 

በኋላ
```

\--- /hint \---

\--- hint \---

ይህ ኮድዎ ምን እንደሚመስሉ ነው:

```blocks3
[ወደ ጨረቃ መሄድ ትፈልጋለህ?] እና
ከተመለስ <(መልስ) = [yes]> በመቀጠል 
  ወደ ኋላ ተመለስ ወደ (ጨረቃ)
መጨረሻ
```

\--- /hint \---

\--- / prinements \---

\--- / task \---

\--- ተግባር \---

አሁን ቻት ሩም እርስዎ ለመነጋገር ሲፈልጉ ትክክለኛውን ቦታ መጀመሩን ማረጋገጥ አለብዎት. ይህን ጥምር ወደ ቻት-ኮትዎ አናት ላይ አክል:

![nano sprite](images/nano-sprite.png)

```blocks3
ይህ sprite

ጠቅታ ሲጨርስ Backdrop ን ወደ (space v) ይቀይሩ
```

\--- / task \---

\--- ተግባር \---

ፕሮግራምዎን ይፈትሹ, እና «አዎ» ብለው ይመልሱ መልስዎ ወደ የጨረቃ ጉዞ መሄድ ከፈለጉ <ጥያቄ> ሲለው ነው. የቻትቦክ አከባቢው መለወጥ እንዳለብዎ ማየት አለብዎት.

\--- / task \---

\--- ተግባር \---

በተጨማሪም በአዲሱ ውስጥ የሚከተለውን ኮድ ማከል ይችላሉ `ከሆነ`እናንተ "አዎ" በማለት መመለስ ከሆነ chatbot እስከ መዝለል እና አራት ጊዜ ወደታች ለማድረግ: {class = "block3control"} የማገጃ:

![nano sprite](images/nano-sprite.png)

```blocks3
ከሆነ <(መልስ) = [yes]> በዚያን 
  (ጨረቃ v) ይቀይሩ የጀርባ

; + ተደጋጋሚ (4) 
    (10) በማድረግ ለውጥ y
    መጠበቅ (0.1) ሰከንድ
    (-10) በ ለውጥ y
    መጠበቅ (0.1) ሰከንድ
  መጨረሻ
መጨረሻ
```

\--- / task \---