## කතා කරන චැට්බෝට්(chatbot)

දැන් ඔබට පෞරුෂයක්(personality එකක්) සහිත චැට්බෝට්(chatbot) එකක් ඇති බැවින්, එය ඔබ සමඟ කතා කරන පරිදි වැඩසටහන්ගත(program) කිරීමට හැකියි.

\--- task \---

Click on your chatbot sprite, and add this code to it so that `when it's clicked`{:class="block3events"}, it `asks for your name`{:class="block3sensing"} and then `says "What a lovely name!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

\--- /task \---

\--- task \---

ඔබේ කේතය(code එක) පරීක්ෂා(test) කිරීමට ඔබගේ චැට්බෝට්(chatbot එක) එක මත ක්ලික් කරන්න. චැට්බෝට්(chatbot) එක ඔබේ නම ඉල්ලූ විට, එය වේදිකාවේ පතුලේ ඇති කොටුවට ටයිප් කර නිල්(blue) සලකුණ(mark එක) මත ක්ලික් කරන්න, නැතහොත් <kbd>නිවේශන යතුර(Enter)</kbd> ඔබන්න.

![Testing a ChatBot response](images/chatbot-ask-test1.png)

![Testing a ChatBot response](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

මේ මොහොතේ, ඔබේ චැට්බෝට් පිළිතුරු දෙන්නේ "මොනතරම් ලස්සන නමක්ද! (What a lovely name!)" ඔබ පිළිතුරු දෙන සෑම අවස්ථාවකම. ඔබට ලැබෙන චැට්බෝට්ගේ(chatbot ගේ) පිළිතුර වඩාත්(more) පුද්ගලික(personal) එකක් කළ හැකිය, එවිට වෙනස් නමක් ටයිප් කරන සෑම අවස්ථාවකම පිළිතුර වෙනස් වේ.

Change the chatbot sprite’s code to `join`{:class="block3operators"} "Hi" with the `answer`{:class="block3sensing"} to the "What's your name?" question, so that the code looks like this:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

By storing the answer in a **variable**, you can use it anywhere your project.

Create a new variable called `name`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Now, change your chatbot sprites’s code to set the `name`{:class="block3variables"} variable to `answer`{:class="block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

Your code should work as before: your chatbot should say hi using the name you type in.

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- /task \---

Test your program again. Notice that the answer you type in is stored in the `name`{:class="block3variables"} variable, and is also shown in the top left-hand corner of the Stage. To make it disappear from the Stage, go to the `Data`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.