## A talking chatbot

Now that you have a chatbot with a personality, you're going to program it to talk to you.

--- task ---

Click on your chatbot sprite, and add this code to it so that `when it's clicked`{:class="blockevents"}, it `asks for your name`{:class="blocksensing"} and then `says "What a lovely name!"`{:class="blocklooks"}.

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) secs
```

--- /task ---

--- task ---

Click on your chatbot to test your code. When the chatbot ask for your name, type it into the box that appears at the bottom of the Stage, and then click on the blue mark, or press <kbd>Enter</kbd>.

![Testing a ChatBot response](images/chatbot-ask-test.png)

--- /task ---

--- task ---

Right now, your chatbot replies "What a lovely name!" every time you answer. You can make the chatbot’s reply more personal, so that the reply is different every time a different name is typed in.

Change the chatbot sprite’s code to `join`{:class="blockoperators"} "Hi" with the `answer`{:class="blocksensing"} to the "What's your name?" question, so that the code looks like this:

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer)) for (2) secs
```

![Testing a personalised reply](images/chatbot-answer-test.png)

--- /task ---

--- task ---

By storing the answer in a **variable**, you can use it anywhere your project.

Create a new variable called `name`{:class="blockdata"}.

[[[generic-scratch-add-variable]]]

--- /task ---

--- task ---

Now, change your chatbot sprites’s code to set the `name`{:class="blockdata"} variable to `answer`{:class="blocksensing"}:

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) secs
```

Your code should work as before: your chatbot should say hi using the name you type in.

![Testing a 'name' variable](images/chatbot-ask-test.png)

--- /task ---

Test your program again. Notice that the answer you type in is stored in the `name`{:class="blockdata"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Data`{:class="blockdata"} blocks section and click on the box next to `name`{:class="blockdata"} so that it is not marked.

