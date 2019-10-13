## Mudar de localização

Também podes programar o teu robô para mudar a sua localização!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

Podes programar o teu robô falante para perguntar "Queres ir à lua?" e, depois mudar de cenário se responderes "sim"?

\--- hints \---

\--- hint \---

O teu robô deve `perguntar "Queres ir à lua?"`{:class="block3sensing"}, e `se`{:class="block3control"} a `resposta`{:class="block3sensing"} for "sim", deve `mudar o cenário para a lua`{:class="block3look"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos que precisas de adicionar ao código do teu robô falante.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Now you need to make sure that your chatbot starts in the right location when you click on it to talk to it. Add this block to the top of your chatbot code:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Test your program, and answer "yes" when the chatbot asks if you want to go to the moon. You should see that the chatbot’s location changes.

\--- /task \---

\--- task \---

You can also add the following code inside the new `if`{:class="block3control"} block to make the chatbot jump up and down four times if you answer "yes":

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

\--- /task \---