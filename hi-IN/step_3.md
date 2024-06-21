## बात करने वाला चैटबॉट

अब जब आपके पास एक व्यक्तित्व वाला चैटबॉट है, तो आप इसे अपने साथ बात करने के लिए प्रोग्राम करेंगे।

\--- task \---

अपने चैटबोट स्प्राइट पर क्लिक करें, और इस कोड को उसमें जोड़ें ताकि`when it's clicked`{:class="block3events"}, यह `asks for your name`{:class="block3sensing"} और फिर`says "What a lovely name!"`{:class="block3looks"}।

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करने के लिए अपने चैटबॉट पर क्लिक करें। जब चैटबॉट आपका नाम पूछता है, तो उसे स्टेज के नीचे दिखाई देने वाले बॉक्स में टाइप करें, और फिर नीले निशान पर क्लिक करें, या <kbd>Enter</kbd>दबाएं।

![चैटबॉट प्रतिक्रिया का परीक्षण करना](images/chatbot-ask-test1.png)

![चैटबॉट प्रतिक्रिया का परीक्षण करना](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

अभी, आपका चैटबॉट जवाब देता है "What a lovely name!" हर बार जब आप जवाब देते हैं। आप चैटबोट के जवाब को अधिक व्यक्तिगत बना सकते हैं, ताकि हर बार एक अलग नाम टाइप करने पर जवाब अलग हो।

चैटबॉट स्प्राइट के कोड को बदलें `join`{:class="block3operators"} के लिये "Hi" को `answer`{:class="block3sensing"} के साथ "What's your name?" प्रश्न के, ताकि कोड इस तरह दिखे:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ say (join [Hi ] (answer) ) for (2) seconds
```

![एक वैयक्तिकृत उत्तर का परीक्षण करना](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

**वेरिएबल** में जवाब को सेव करके, आप इसका अपने प्रोजेक्ट में कहीं भी उपयोग कर सकते हैं।

`name`{:class="block3variables"} नामक एक नया वेरिएबल बनाएं।

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

अब, `name`{:class="block3variables"} वेरिएबल (variable) को `answer`{:class="block3sensing"} पर सेट करने के लिए अपने चैटबॉट स्प्राइट के कोड को बदलें:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
+ say (join [Hi ] (name)) for (2) seconds
```

आपका कोड पहले की तरह काम करना चाहिए: आपके चैटबॉट को आपके द्वारा लिखे गए नाम का उपयोग करके हाय कहना चाहिए।

![एक वैयक्तिकृत उत्तर का परीक्षण करना](images/chatbot-answer-test.png)

\--- /task \---

अपने प्रोग्राम का फिर से परीक्षण करें। ध्यान दें कि आपके द्वारा टाइप किया गया उत्तर `name`{:class="block3variables"} वेरियबल में सेव हो गया है, और यह स्टेज के ऊपरी बाएं कोने में भी दिखाया गया है। इसे स्टेज से गायब करने के लिए, `Variables`{:class="block3variables"} ब्लॉक सेक्शन में जाएं और `name`{:class="block3variables"} के आगे वाले बॉक्स पर क्लिक करें ताकि यह चिह्नित न हो।