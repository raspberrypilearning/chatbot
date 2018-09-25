## Changing location

You can also program your chatbot to change its location.

--- task ---

Add another backdrop to your Stage, for example the 'moon' backdrop.

![Adding a 'moon' backdrop](images/chatbot-moon.png)

--- /task ---

--- task ---

You can now program your chatbot to ask "Do you want to go to the moon?" and then change location if you answer "yes".

```blocks
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to [moon v]
end
```

![Testing a changing backdrop](images/chatbot-backdrop-test.png)

--- /task ---

--- task ---

You also need to make sure that your chatbot is in its original location when you start talking to it. Add this block to the top of your chatbot code:

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

if <(answer) = [yes]> then 
  switch backdrop to [moon v]
  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end

--- /task ---
