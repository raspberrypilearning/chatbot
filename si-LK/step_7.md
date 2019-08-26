## ස්ථානය(location) වෙනස් කිරීම

ඔබේ චැට්බෝට්හි(chatbot එකේ) පිහිටීම(location එක) වෙනස් කිරීම සඳහා ඔබට එය වැඩසටහන්ගත(program) කළ හැකිය!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

"ඔබට සඳට යාමට අවශ්‍යද"("Do you want to go to the moon") යනුවෙන් විමසීමට ඔබේ චැට්බෝට්(chatbot එක) ක්‍රමලේඛනය(program) කළ හැකිද, ඉන්පසු පිළිතුර "ඔව්(yes)" වන විට පසුබිම(backdrop එක) වෙනස් කළ හැකිද?

\--- hints \---

\--- hints \---

ඔබේ චැට්බෝට්(chatbot එක) `"ඔබට සඳට යාමට අවශ්‍යද?"("Do you want to go to moon?")`{:class="block3sensing"}, සහ `පිළිතුර(answer)`{:class="block3sensing"} "ඔව්(yes)"`නම්(if)`{:class="block3control"}, එහි `පසුබිම සඳට මාරු කළ යුතුය(switch the backdrop to moon)`{:class="block3looks"}.

\--- /hint \---

\--- hints \---

ඔබේ චැට්බෝට්(chatbot ගේ) කේතයට(code එකට) එකතු කිරීමට අවශ්‍ය කේත(code) කට්ටිය(block එක) මෙහි දැක්වේ.

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