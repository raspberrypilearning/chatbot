## स्थान बदलना

आप अपना स्थान बदलने के लिए अपने चैटबोट को भी प्रोग्राम कर सकते हैं!

![पृष्ठभूमि बदलने का परीक्षण करना](images/chatbot-backdrop-moon.png)

\--- task \---

क्या आप "क्या आप चाँद पर जाना चाहते हैं" पूछने के लिए अपने चैटबोट को प्रोग्राम कर सकते हैं, और जब जवाब "हाँ" हो तो पृष्ठभूमि बदल दें?

\--- hints \---

\--- hint \---

आपके चैटबोट को ` पूछना चाहिए "क्या आप चाँद पर जाना चाहते हैं?" ` {} वर्ग = "ब्लॉक 3 सेंसिंग"}, और ` यदि ` {= class = "block3control"} आप ` उत्तर दें ` {"class =" block3sensing "}" हाँ ", यह ` पृष्ठभूमि को चंद्रमा पर स्विच करना चाहिए ` {: वर्ग = "block3looks"}।

\--- /hint \---

\--- hint \---

यहां कोड ब्लॉक हैं जिन्हें आपको अपने चैटबोट कोड में जोड़ना होगा।

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

यहाँ दिखाया गया है कि आपका कोड कैसा दिखना चाहिए:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

अब आपको यह सुनिश्चित करने की आवश्यकता है कि जब आप उस पर बात करने के लिए उस पर क्लिक करते हैं तो आपका चैटबोट सही स्थान पर शुरू होता है। इस ब्लॉक को अपने चैटबोट कोड के शीर्ष पर जोड़ें:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

अपने कार्यक्रम का परीक्षण करें, और "हां" का जवाब दें जब चैटबोट पूछता है कि क्या आप चाँद पर जाना चाहते हैं। आपको यह देखना चाहिए कि चैटबॉट की लोकेशन बदल जाती है।

\--- /task \---

\--- task \---

आप निम्न कोड को नए ` के अंदर भी जोड़ सकते हैं ` {"class =" block3control "} ब्लॉकबॉट बनाने के लिए ब्लॉक करें और यदि आप" हां "का जवाब देते हैं तो चार बार ऊपर और नीचे कूदें:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> then 
  switch backdrop to (moon v)

+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

\--- /task \---