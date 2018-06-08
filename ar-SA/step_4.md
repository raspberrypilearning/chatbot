## روبوت مُحاوِر

الآن، بعد أن أصبح لديك روبوت بشخصية معينة، لنُبرمجْه ليتحدث معك.

\--- task \---

أضف تعليمة برمجية لروبوتك بحيث عندما تنقر عليه، يسألك عن اسمك ثم يقول "ياله من اسم جميل!"

![Testing a ChatBot response](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- **عند النقر على كائن الروبوت**، يجب أن **يسألك** الروبوت عن اسمك. ثم يجب أن **يقول** "ياله من اسم جميل!" \--- /hint \--- \--- hint \--- فيما يلي قوالب التعليمات البرمجية التي ستحتاج إليها: ![Blocks for a ChatBot reply](images/chatbot-ask-blocks.png) \--- /hint \--- \--- hint \--- جب أن تكون التعليمة البرمجية التي تُدخلها كما يلي: ![Code for a ChatBot reply](images/chatbot-ask-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

الأن الروبوت بكل بساطة يُجيب بعبارة "ياله من اسم جميل!" في كل مرة، هل يمكنك تخصيص إجابة الروبوتك من خلال الإستفادة من إجابتك؟

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- hints \--- \--- hint \--- **عند النقر على كائن الروبوت**، يجب أن **يسألك** الروبوت عن اسمك. ثم يجب أن **يقول** "مرحباً" يليها **إجابتك**. \--- /hint \--- \--- hint \--- فيما يلي قوالب التعليمات البرمجية التي ستحتاج إليها: ![Blocks for a personalised reply](images/chatbot-answer-blocks.png) \--- /hint \--- \--- hint \--- جب أن تكون التعليمة البرمجية التي تُدخلها كما يلي: ![Code for a personalised reply](images/chatbot-answer-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

إذا خزَّنتَ إجابتك في **متغير**، فسيمكنك استخدامها لاحقًا، أنشئ متغيرًا جديدًا يُسمى `الاسم` لتخزين اسمك.

[[[generic-scratch-add-variable]]]

\--- /task \---

\--- task \---

هل يمكنك تخزين إجابتك في المتغير `الاسم` واستخدام هذا المتغير في إجابة الروبوت؟

يجب أن تعمل التعليمة البرمجية التي تُدخلها كما سبق: يجب أن يقول الروبوت مرحبًا، يليها اسمك.

![Testing a 'name' variable](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- **عند النقر على كائن الروبوت**، يجب أن **يسألك** الروبوت عن اسمك. You should then **set** the `name` variable to your **answer**. The chatbot should then **say** "Hi", followed by your **name**. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need: ![Blocks for a 'name' variable](images/chatbot-variable-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a 'name' variable](images/chatbot-variable-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Challenge: more questions

Program your chatbot to ask another question. Can you store the answer in a new variable?

![More questions](images/chatbot-question.png) \--- /challenge \---