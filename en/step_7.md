## Changing location

You can also program your chatbot to change its location.

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

--- task ---

--- hints ---

--- hint ---

Can you now program your chatbot to `ask "Do you want to go to the moon?"`{:class="blocksensing"} and `if`{:class="blocksensing"} you `answer`{:class="blockdata"} yes it should `switch the backdrop to the moon`{:class="blocklooks"}.

--- /hint ---

--- hint ---

Here are the code blocks you'll need to add to your chatbot code.

![nano sprite](images/nano-sprite.png)
```blocks
switch backdrop to [moon v]

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

--- /hint ---

--- hint ---

This is what your code should look like:

```blocks
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to [moon v]
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

You also need to make sure that your chatbot is in its original location when you start talking to it. Add this block to the top of your chatbot code:

![nano sprite](images/nano-sprite.png)
```blocks
when this sprite clicked
switch backdrop to [space v]
```

--- /task ---

--- task ---

Test your program, and answer yes when asked if you want to go to the moon. You should see that the chatbot’s location has changed.

--- /task ---

--- task ---

You can also add this code inside your if block, to make your chatbot jump up and down four times if the answer is yes:

![nano sprite](images/nano-sprite.png)
```blocks
if <(answer) = [yes]> then 
  switch backdrop to [moon v]
  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

--- /task ---
