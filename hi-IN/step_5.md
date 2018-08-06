## चरण 3: निर्णय लेना

आप अपने चैटबॉट को अपने प्रश्नों के उत्तर के आधार पर क्या कहना है या क्या करना है यह तय करने के लिए प्रोग्राम कर सकते हैं।

\--- task \---

क्या आप चैटबॉट को "Are you OK?" पूछने के लिए तैयार कर सकते हैं, और उत्तर "That's great to hear!" बोलने के लिए कोड कर सकते हैं, **अगर** उपयोगकर्ता का उत्तर केवल "yes" हो?

अपने नए कोड को ठीक से जांचने के लिए, आपको इसको **दो बार** जांचना चाहिए।एक बार "yes" और एक बार "no" के साथ।

अगर आपका उत्तर "yes" है, तो आपके चैटबॉट को "That's great to hear!" जवाब देना चाहिए, परन्तु यदि आप "no" उत्तर देते हैं, तो इसे कुछ नहीं कहना चाहिए।

![Testing a chatbot reply](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- आपके चॅटबोट द्वारा "Hi" कहने के बाद, उसे अब "Are you OK?" भी **पूछना** चाहिए। **अगर** आपका उत्तर "yes" है, तो चॅटबोट को "That's great to hear!" **कहना** चाहिए। \--- /hint \--- \--- hint \--- ये वे अतिरिक्त कोड ब्लॉक हैं, जिनकी आपको आवश्यकता होगी: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- आपका कोड इस प्रकार दखाई देगा: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

इस समय अगर आपका उत्तर "no" है, तो आपका चैटबॉट कुछ नहीं कहता। क्या आप अपने चैटबॉट में परिवर्तन कर सकते हैं ताकि यह जवाब दे सके "Oh no!" यदि आप इसके प्रश्न के लिए "no" का जवाब देते हैं?

परीक्षण करें और सहेजें। यदि आप "no" उत्तर देते हैं, तो आपके चैटबॉट को "Oh no" कहना चाहिए। असल में, यदि आप "yes" के अलावा कोई अन्य उत्तर देते हैं, तो यह कहेगा "Oh no!" (`अगर/या` ब्लॉक में **वरना** का अर्थ **अन्यथा**होता है)।

![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- **यदि** आपका उत्तर "yes" है तो आपके चैटबॉट को अब "That's great to hear!" कहना चाहिए, लेकिन अगर आप कुछ **और** जवाब देते हैं तो इसे "Oh no!" कहना चाहिए। \--- /hint \--- \--- hint \--- ये वे कोड ब्लॉक हैं, जिनकी आपको आवश्यकता होगी: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- आपका कोड इस प्रकार दखाई देगा: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

अपने चैटबॉट को बुलवाने के लिए आप अगर/या<0> ब्लॉक के भीतर, यह कोड ही नहीं बल्कि कोई भी कोड जोड़ सकते हैं। यदि आप अपने चैटबॉट के <strong>Costume</strong> टैब पर क्लिक करें, तो आप देखेंगे कि इसमें एक से अधिक पोशाक हैं।</p>

<p><img src="images/chatbot-costume-view.png" alt="chatbot costumes" /></p>

<p>--- /task ---</p>

<p>--- task ---</p>

<p>क्या आप चैटबॉट की पोशाक को अपने प्रत्युत्तर से मिलाने के लिए बदल सकते हैं?</p>

<p>परीक्षण करें और सहेजें। आपको अपने उत्तर के आधार पर चैटबॉट के चेहरे में बदलाव दिखना चाहिए।</p>

<p><img src="images/chatbot-costume-test.png" alt="Testing a changing costume" /></p>

<p>--- hints ---
--- hint ---
Your chatbot should now also <strong>switch costume</strong> depending on the answer given.
--- /hint ---
--- hint ---
Here are the code blocks you'll need to use:
<img src="images/chatbot-costume-blocks.png" alt="Blocks for a changing costume" />
--- /hint ---
--- hint ---
Here's how your code should look:
<img src="images/chatbot-costume-code.png" alt="Code for a changing costume" />
--- /hint ---
--- /hints ---</p>

<p>--- /task ---</p>

<p>--- task ---</p>

<p>Have you noticed that your chatbot's costume stays the same that it changed to the last time you spoke to it? Can you fix this problem?</p>

<p><img src="images/chatbot-costume-bug-test.png" alt="Costume bug" /></p>

<p>Test and save: Run your code and type "no", so that your chatbot looks unhappy. When you run your code again, your chatbot should change back to a smiling face before asking your name.</p>

<p><img src="images/chatbot-costume-fix-test.png" alt="Testing a costume fix" /></p>

<p>--- hints ---
--- hint ---
When the <strong>sprite is clicked</strong>, your chatbot should first <strong>switch costume</strong> to a smiling face.
--- /hint ---
--- hint ---
Here's the code block you'll need to add:
<img src="images/chatbot-costume-fix-blocks.png" alt="Blocks for a costume fix" />
--- /hint ---
--- hint ---
Here's how your code should look:
<img src="images/chatbot-costume-fix-code.png" alt="Code for a costume fix" />
--- /hint ---
--- /hints ---</p>

<p>--- /task ---</p>

<p>--- challenge ---</p>

<h2>Challenge: more decisions</h2>

<p>Program your chatbot to ask another question - something with a "yes" or "no" answer. Can you make your chatbot respond to the answer?</p>

<p><img src="images/chatbot-joke.png" alt="screenshot" />
--- /challenge ---</p>