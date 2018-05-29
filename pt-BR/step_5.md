## Etapa 3: Tomando decisões

Você pode programar o seu chatbot para decidir o que dizer ou fazer com base nas suas respostas às suas perguntas.

\--- task \---

Você pode fazer o chatbot fazer a pergunta "Você está bem?", e codificá-lo para responder "Que bom ouvir isso!" somente **se** o usuário responder "sim"?

Para testar o seu novo código corretamente, você deve testá-lo **duas vezes**, uma vez com a resposta "sim" e uma vez com a resposta "não".

Seu chatbot deve responder "Que bom ouvir isso!" se você responder "sim", mas não diga nada se você responder "não".

![Testing a chatbot reply](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Após o seu chatbot ter dito "Oi", agora também deve **perguntar** "Você está bem?". **se** você responder "sim", então o chatbot deve **dizer** "Que bom ouvir isso!". \--- /hint \--- \--- hint \--- Aqui estão os blocos de código que você precisará: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Isto é como seu código deve se parecer: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

At the moment your chatbot doesn't doesn't say anything if you answer "no". Can you change your chatbot so that it also replies "Oh no!" if you answer "no" to its question?

Test and save. Your chatbot should now say "Oh no!" if you answer "no". In fact, it will say "On no!" if you answer with anything other than "yes" (the **else** in an `if/else` block means **otherwise**).

![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Your chatbot should now say "That's great to hear!" **if** your answer is "yes", but should say "Oh no!" if you answer something **else**. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need to use: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

You can put any code inside an `if/else` block, not just code to make your chatbot speak. If you click your chatbot's **Costume** tab, you'll see that it has more than one costume.

![chatbot costumes](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Can you change the chatbot's costume to match your response?

Test and save. You should see your chatbot's face change depending on your answer.

![Testing a changing costume](images/chatbot-costume-test.png)

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