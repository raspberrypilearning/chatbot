## A talking chatbot

Now that you have a chatbot with a personality, let's program it to talk to you.

--- task ---

Click on your chatbot character, and add this code to your chatbot so that `when it's clicked`{:class="blockevents"}, it `asks for your name`{:class="blocksensing"} and then `says "What a lovely name!"`{:class="blocklooks"}.

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) secs
```

--- /task ---

--- task ---

Click your chatbot to test it out. When you are asked your name, type it into the box along the bottom of the stage.

![Testing a ChatBot response](images/chatbot-ask-test.png)

--- /task ---


--- task ---

Your chatbot simply replies ‘What a lovely name!’ every time. You can personalise your chatbot’s reply, by making use of the user’s answer.

Change the chatbot’s code to `join`{:class="blockoperators"} "Hi" with the `answer`{:class="blocksensing"} to your question, so that it looks like this:

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer)) for (2) secs
```

![Testing a personalised reply](images/chatbot-answer-test.png)

--- /task ---

--- task ---

If you store the answer in a variable, you’ll be able to make use of it throughout your project.

Create a new variable called `name`{:class="blockdata"}.

[[[generic-scratch-add-variable]]]

--- /task ---

--- task ---

Once you’ve created your new variable, edit your chatbot’s code to look like this:

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) secs
```

Your code should work as before: your chatbot should say hello using your name.

![Testing a 'name' variable](images/chatbot-ask-test.png)

--- /task ---

If you test your program again, you’ll notice that the answer is stored in the `name`{:class="blockdata"} variable, and is shown in the top-left of the stage. (To hide this, just untick the tick-box next to `name`{:class="blockdata"} in the blocks palette.)


