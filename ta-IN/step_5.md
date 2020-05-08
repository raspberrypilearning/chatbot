## முடிவுகளை எடுத்தல்

உங்கள் சாட்போட்டைப் பெறும் பதில்களின் அடிப்படையில் என்ன செய்ய வேண்டும் என்பதைத் தீர்மானிக்க நீங்கள் அதை ப்ரொக்ராம் செய்யலாம்.

முதலில், உங்கள் சாட்போட் "ஆம்" அல்லது "இல்லை" என்று பதிலளிக்கக்கூடிய கேள்வியைக் கேட்க வைக்கப் போகிறீர்கள்.

\--- task \---

உங்கள் சாட்போட்டின் Codeஐ மாற்றவும். உங்கள் சாட்போட் `name`{:class="block3variables"} variable-ஐ பயன்படுத்தி "நீங்கள் நன்றாக இருக்கிறீர்களா name" என்ற கேள்வியைக் கேட்க வேண்டும். பின்னர், அதற்க்கு "ஆம்"(yes) என்று பதில் `வந்தால்0>{:class="block3control"}, "கேட்க மிகவும் நன்றாக உள்ளது!" என்ற திரும்ப சொல்ல வேண்டும். அதற்கு "இல்லை" என்று பதில் வந்தால் எதுவும் சொல்லக் கூடாது.</p>

<p><img src="images/chatbot-if-test1-annotated.png" alt="Testing a chatbot reply" /></p>

<p><img src="images/chatbot-if-test2.png" alt="Testing a chatbot reply" /></p>

<p><img src="images/nano-sprite.png" alt="nano sprite" /></p>

<pre><code class="blocks3">when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
end
`</pre> 

To test your new code properly, you should test it **twice**: once with the answer "yes", and once with the answer "no".

\--- /task \---

At the moment, your chatbot doesn't doesn't say anything to the answer "no".

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