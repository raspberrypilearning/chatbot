## Крок 3: Прийняття рішень

Ви можете запрограмувати вашого чат-бота вирішувати, що казати або відштовхуватись від ваших відповідей на питання.

\--- task \---

Чи можете ви запрограмувати чат-бота запитувати "Ти в порядку?", і запрограмувати відповідати "Радий це чути!" тільки **якщо** відповідь користувача "так"?

Щоб правильно перевірити свій новий код, потрібно перевірити його **двічі**, один раз з відповіддю "так", і один раз з відповіддю "ні".

Ваш чат-бот повинен відповісти "Радий це чути!" якщо ви відповідаєте "так", але не казати нічого, якщо ви відповідаєте "ні".

![Testing a chatbot reply](images / chatbot-if-test.png)

\--- hints \--- \--- hint \--- Після того, як ваш чат-бот сказав "Привіт", йому слід також **запитати** "Ти в порядку?". **Якщо** ви відповідаєте "так", тоді чат-бот повинен **сказати** "Радий це чути!". \--- /hint \--- \--- hint \--- Ось додаткові кодові блоки, які вам знадобляться: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Так має виглядати ваш код: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

На даний момент ваш чат-бот не робить нічого, якщо ви відповідаєте "ні". Чи можна змінити вашого чат-бота, щоб він також відповідав "О ні!" якщо ви відповідаєте "ні" на запитання?

Перевірте та збережіть. Тепер ваш чат-бот повинен сказати "О ні!" якщо ви відповідаєте "ні". Насправді він буде сказати "О ні!" на будь-яку відповідь, окрім "так" ( **інше** в `якщо/інше` блок означає **в іншому випадку**).

![Testing a yes/no reply](images / chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Тепер ваш чат-бот має казати "Радий це чути!" **якщо** ваша відповідь "так", але казати "О ні!", якщо відповідь якась **інша**. \--- /hint \--- \--- hint \--- Ось кодові блоки, які вам знадобляться: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Так має виглядати ваш код: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Ви можете помістити будь-який код всередину `якщо/інакше` блоку, не тільки код, щоб ваш чат-бот розмовляв. Якщо ви натиснете на вашому чат-боті на вкладку **костюм**, ви побачите, що в ньому більше одного костюма.

![chatbot costumes](images / chatbot-costume-view.png)

\--- /task \---

\--- task \---

Чи можете ви змінити костюм чат-бота, відповідно до ваших відповідей?

Перевірте та збережіть. Ви повинні побачити зміни на обличчі вашого чат-бота в залежності від вашої відповіді.

![Testing a changing costume](images / chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Your chatbot should now also **switch costume** depending on the answer given. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need to use: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Have you noticed that your chatbot's costume stays the same that it changed to the last time you spoke to it? Can you fix this problem?

![Costume bug](images/chatbot-costume-bug-test.png)

Test and save: Run your code and type "no", so that your chatbot looks unhappy. When you run your code again, your chatbot should change back to a smiling face before asking your name.

![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- When the **sprite is clicked**, your chatbot should first **switch costume** to a smiling face. \--- /hint \--- \--- hint \--- Here's the code block you'll need to add: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Challenge: more decisions

Program your chatbot to ask another question - something with a "yes" or "no" answer. Can you make your chatbot respond to the answer?

![screenshot](images/chatbot-joke.png) \--- /challenge \---