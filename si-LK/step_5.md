## තීරණ ගැනීම

ඔබට ලැබෙන පිළිතුරු මත පදනම්ව කුමක් කළ යුතුද යන්න තීරණය කිරීම සඳහා ඔබේ චැට්බෝට්(chatbot) වැඩසටහන්ගත(program) කළ හැකිය.

පළමුව, ඔබ ඔබේ චැට්බෝට්(chatbot) එක මගින් "ඔව්(yes)" හෝ "නැත(no)" යනුවෙන් පිළිතුරු දිය හැකි ආකාරයේ ප්‍රශ්නයක් ඇසීමට සලස්වයි.

\--- task \---

ඔබගේ චැට්බෝට්(chatbot) එකේ කේතය(code එක) වෙනස් කරන්න. ඔබේ චැට්බෝට්(chatbot) එක විසින් `නාමය(name)`{:class="block3variables"} විචල්‍යය(variable එක) භාවිතා කරමින් <0>ඔබට කොහොමද නාමය("Are you OK name")</0> යන ප්‍රශ්නය ඇසිය යුතුය. එයට ලැබෙන පිළිතුර "ඔව්"("yes") `නම්(if)`{:class="block3control"} එවිට එය පිළිතුරු දිය යුත්තේ "එය ඇසීමත් සතුටක්!"("That's great to hear!") ලෙසටයි, නමුත් පිළිතුර "නැත"("no") නම් කිසිවක් නොකියා සිටියයුතුයි.

![Testing a chatbot reply](images/chatbot-if-test1-annotated.png)

![Testing a chatbot reply](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then
  say [That's great to hear!] for (2) seconds
end
```

ඔබගේ නව කේතය නිසියාකාරව පරීක්ෂා(test) කිරීමට, ඔබ එය **දෙවරක්(twice)** පරීක්ෂා කළ යුතුය: වරක් "ඔව්"("yes") යන පිළිතුර යොදමින් හා, එක් වරක් "නැත"("No") යන පිළිතුර යොදමින් පරීක්ෂා කිරීම වඩා සුදුසු වේ.

\--- /task \---

මේ මොහොතේ, ඔබගේ චැට්බෝට්(chatbot එක) "නැත"("no") යන පිළිතුරට කිසිවක් නොකියයි.

\--- task \---

Change your chatbot's code so that it replies "Oh no!" if it receives "no" as the answer to "Are you OK name".

Replace the `if, then`{:class="block3control"} block with an `if, then, else`{:class="block3control"} block, and include code so the chatbot can `say "Oh no!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
else 
+  say [Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

Test your code. You should get a different response when you answer "no" and when you answer "yes": your chatbot should reply with "That’s great to hear!" when you answer "yes" (which is not case-sensitive), and reply with "Oh no!" when you answer **anything else**.

![Testing a chatbot reply](images/chatbot-if-test2.png)

![Testing a yes/no reply](images/chatbot-if-else-test.png)

\--- /task \---

You can put any code inside an `if, then, else`{:class="block3control"} block, not just code to make your chatbot speak!

If you click your chatbot's **Costumes** tab, you'll see that there is more than one costume.

![chatbot costumes](images/chatbot-costume-view-annotated.png)

\--- task \---

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Testing a changing costume](images/chatbot-costume-test1.png)

![Testing a changing costume](images/chatbot-costume-test2.png)

Change the code inside the `if, then, else`{:class="block3control"} block to `switch costume`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

Test and save your code. You should see your chatbot's face change depending on your answer.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Costume bug](images/chatbot-costume-bug-test.png)

\--- task \---

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Testing a costume fix](images/chatbot-costume-fix-test.png)

\--- /task \---