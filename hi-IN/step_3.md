## बात करने वाला चैटबॉट

अब जब आपके पास व्यक्तित्व वाला चैटबॉट है, तो चलिए इसे आपसे बात करने के लिए प्रोग्राम करें।

--- task ---

अपने चैटबोट स्प्राइट पर क्लिक करें, और इस कोड को इसमें जोड़ें ताकि `जब यह क्लिक किया जाए`{:class="block3events"}, यह `आपका नाम पूछता है`{:class="block3sensing"} और फिर `कहते हैं "What a lovely name!"`{:class="block3looks"}।

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

--- /task ---

--- task ---

अपने कोड का परीक्षण करने के लिए अपने चैटबॉट पर क्लिक करें। जब चैटबोट आपका नाम पूछती है, तो इसे उस बॉक्स में टाइप करें जो स्टेज के नीचे दिखाई देता है, और फिर नीले निशान पर क्लिक करें, या <kbd>दर्ज करें दबाएं</kbd> ।

![चैटबॉट प्रतिक्रिया का परीक्षण करना](images/chatbot-ask-test1.png)

![चैटबॉट प्रतिक्रिया का परीक्षण करना](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

अभी, आपका चैटबॉट जवाब देता है "What a lovely name!" हर बार जब आप जवाब देते हैं। आप चैटबोट के उत्तर को अधिक व्यक्तिगत बना सकते हैं, ताकि हर बार एक अलग नाम टाइप करने पर उत्तर अलग-अलग हो।

चैटबॉट स्प्राइट के कोड को `से जुड़ें (join)`{:class="block3operators"} "Hi" के लिए "What's your name?" प्रश्न, ताकि कोड इस तरह दिखे:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![निजीकृत उत्तर का परीक्षण करना](images/chatbot-answer-test.png)

--- /task ---

--- task ---

**चर में उत्तर को संग्रहीत करके**, आप इसे अपने प्रोजेक्ट के लिए कहीं भी उपयोग कर सकते हैं।

एक नया चर बनाएं `name`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

अब, `name`{:class="block3variables"} सेट करने के लिए अपने चैटबॉट स्प्राइट्स कोड को बदल दें चर से `answer`{:class="block3sensing"}:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

आपका कोड पहले की तरह काम करना चाहिए: आपके चैटबॉट को आपके द्वारा लिखे गए नाम का उपयोग करके नमस्ते कहना चाहिए।

![निजीकृत उत्तर का परीक्षण करना](images/chatbot-answer-test.png)

--- /task ---

अपने कार्यक्रम का फिर से परीक्षण करें। ध्यान दें कि आपके द्वारा टाइप किया गया उत्तर `name`{:class="block3variables"} में संग्रहीत है वैरिएबल, और स्टेज के ऊपरी बाएं कोने में भी दिखाया गया है। इसे मंच से गायब करने के लिए, `Variables`{:class="block3variables"} पर जाएं खंड को ब्लॉक करता है और `name`{:class="block3variables"} के आगे स्थित बॉक्स पर क्लिक करता है ताकि यह चिह्नित न हो।