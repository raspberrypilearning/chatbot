## Step 3: Making decisions

You can program your chatbot to decide what to do, based on the user’s responses.

Let’s get your chatbot to ask the user a question which has a yes or no answer.

--- task ---

Your chatbot should ask the question "Are you OK name?", using the `name`{:class="blockoperators"} variable and reply "That's great to hear!" `if`{:class="blockcontrol"} the user answers "yes", but say nothing if you answer "no".

![Testing a chatbot reply](images/chatbot-if-test.png)

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) secs
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) secs
end
```

To test your new code properly, you should test it __twice__, once with the answer "yes", and once with the answer "no".

--- /task ---

At the moment your chatbot doesn't doesn't say anything if you answer "no". Lets change your chatbot so that it also replies "Oh no!" if you answer "no" to its question?

--- task ---

Replace the `if, then`{:class="blockcontrol"} an `if, then, else`{:class="blockcontrol"} block and include to code to `say "Oh no!"`{:class="blocklooks"}.

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) secs
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) secs
else 
  say [Oh no!] for (2) secs
end
```

--- /task ---


--- task ---

Test your code, you’ll now see that you get a response when you answer yes or no. Your chatbot should reply with ‘That’s great to hear!’ when you answer yes (which is not case-sensitive), but will reply with ‘Oh no!’ if you type anything else.

![Testing a yes/no reply](images/chatbot-if-else-test.png)

--- /task ---

You can put any code inside an `if, then, else`{:class="blockcontrol"} block, not just code to make your chatbot speak. If you click your chatbot's **Costume** tab, you'll see that it has more than one costume.

![chatbot costumes](images/chatbot-costume-view.png)

--- task ---

Now lets change the chatbot's costume to match your response.

![Testing a changing costume](images/chatbot-costume-test.png)

Change the code inside the `if, then, else`{:class="blockcontrol"} block to `switch costume`{:class="blocklooks"}.

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) secs
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 
  switch costume to [nano-c v]
  say [That's great to hear!] for (2) secs
else 
  switch costume to [nano-d v]
  say [Oh no!] for (2) secs
end
```

Test and save. You should see your chatbot's face change depending on your answer.


--- /task ---

Have you noticed that your chatbot's costume stays the same that it changed to the last time you spoke to it? 

Run your code and type "no", so that your chatbot looks unhappy. When you run your code again, your chatbot should change back to a smiling face before asking your name.

![Costume bug](images/chatbot-costume-bug-test.png)

--- task ---

To fix the problem you need to `switch costume`{:class="blocklooks"} at the start `when the sprite is clicked`{:class="blockevents"}.

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
switch costume to [nano-b v]
ask [What's your name?] and wait
```

![Testing a costume fix](images/chatbot-costume-fix-test.png)

--- /task ---

