## स्थान बदलना

आप अपने चैटबॉट को उसका स्थान बदलने के लिए भी प्रोग्राम कर सकते हैं!

![बदलती पृष्ठभूमि का परीक्षण](images/chatbot-backdrop-moon.png)

\--- task \---

क्या आप "Do you want to go to the moon" पूछने के लिए अपने चैटबोट को प्रोग्राम कर सकते हैं, और जब जवाब "yes" हो तो पृष्ठभूमि बदल जाए?

\--- hints \---

\--- hint \---

आपके चैटबोट को पूछना चाहिए `ask "Do you want to go to the moon?"`{:class="block3sensing"}, और `if`{:class="block3control"} आप `answer`{:class="block3sensing"} "yes", तो फिर `switch the backdrop to the moon`{:class="block3looks"}।

\--- /hint \---

\--- hint \---

यहां कोड ब्लॉक हैं जिन्हें आपको अपने चैटबॉट कोड में जोड़ने की आवश्यकता है।

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

आपका कोड ऐसा दिखना चाहिए:

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

अब आपको यह सुनिश्चित करने की आवश्यकता है कि जब आप उस पर बात करने के लिए क्लिक करते हैं तो आपका चैटबोट सही स्थान पर शुरू होता है। इस ब्लॉक को अपने चैटबोट कोड के शीर्ष पर जोड़ें:

![नैनो स्प्राइट](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

अपने प्रोग्राम का परीक्षण करें, और "yes" जवाब दें जब चैटबोट पूछता है कि क्या आप चाँद पर जाना चाहते हैं। आपको यह देखना चाहिए कि चैटबॉट का स्थान बदल जाता है।

\--- /task \---

\--- task \---

यदि आप "yes" उत्तर देते हैं तो चैटबॉट को चार बार ऊपर और नीचे कूदने के `if`{:class="block3control"} ब्लॉक के अंदर आप निम्नलिखित कोड भी जोड़ सकते हैं:

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