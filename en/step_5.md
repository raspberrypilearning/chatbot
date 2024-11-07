## Changing location

You can also program your chatbot to change its location!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

Your chatbot should `ask "Do you want to go to the moon?"`{:class="block3sensing"}, and `if`{:class="block3control"} you `answer`{:class="block3sensing"} "yes", it should `switch the backdrop to the moon`{:class="block3looks"}.

--- task ---

This is what your code should look like:

```blocks3
when this sprite clicked
switch costume to (nano-a v)
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 
switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
+ ask [Do you want to go to the moon?] and wait
+ if <(answer) = [yes]> then 
+   switch backdrop to (moon v)
end
```

--- /task ---

--- task ---

Now you need to make sure that your chatbot starts in the right location when you click on it to talk to it. Add this block to the top of your chatbot code:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch backdrop to (space v)
switch costume to (nano-a v)
ask [What's your name?] and wait
```

--- /task ---

--- task ---

Test your code.

Answer "yes" when the chatbot asks if you want to go to the moon. You should see that the chatbot’s location changes.

--- /task ---

--- task ---

Make the chatbot jump up and down four times if you answer "yes":

![nano sprite](images/nano-sprite.png)

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

--- /task ---


--- task ---

Test your code. 

--- /task ---
