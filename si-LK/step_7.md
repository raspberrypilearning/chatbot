## ස්ථානය(location) වෙනස් කිරීම

ඔබේ චැට්බෝට්හි(chatbot එකේ) පිහිටීම(location එක) වෙනස් කිරීම සඳහා ඔබට එය වැඩසටහන්ගත(program) කළ හැකිය!

![වෙනස්වන පසුබිම(backdrop) පරීක්ෂා(test) කිරීම](images/chatbot-backdrop-moon.png)

\--- task \---

"ඔබට සඳට යාමට අවශ්‍යද"("Do you want to go to the moon") යනුවෙන් විමසීමට ඔබේ චැට්බෝට්(chatbot එක) ක්‍රමලේඛනය(program) කළ හැකිද, ඉන්පසු පිළිතුර "ඔව්(yes)" වන විට පසුබිම(backdrop එක) වෙනස් කළ හැකිද?

\--- hints \---

\--- hints \---

ඔබේ චැට්බෝට්(chatbot එක) `"ඔබට සඳට යාමට අවශ්‍යද?"("Do you want to go to moon?")`{:class="block3sensing"}, සහ `පිළිතුර(answer)`{:class="block3sensing"} "ඔව්(yes)"`නම්(if)`{:class="block3control"}, එහි `පසුබිම සඳට මාරු කළ යුතුය(switch the backdrop to moon)`{:class="block3looks"}.

\--- /hint \---

\--- hints \---

ඔබේ චැට්බෝට්(chatbot ගේ) කේතයට(code එකට) එකතු කිරීමට අවශ්‍ය කේත(code) කට්ටිය(block එක) මෙහි දැක්වේ.

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hints \---

ඔබගේ කේතය(code එක) මෙබඳු එකක් විය යුතුයි:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then
  switch backdrop to (moon v) 
end
```

\--- /hint \---

\--- /hint \---

\--- /task \---

\--- task \---

දැන් ඔබ කතාබස් කිරීමට එය මත ක්ලික් කළ විට ඔබේ චැට්බෝට් නිවැරදි ස්ථානයෙන් ආරම්භ වන බවට වග බලා ගත යුතුය. ඔබගේ චැට්බෝට්(chatbot ගේ) කේතයේ(code එකේ) ඉහළට මෙම කට්ටිය(block එක) එක් කරන්න:

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

ඔබේ වැඩසටහන(program එක) පරීක්ෂා(test) කර, ඔබට සඳට යාමට අවශ්‍ය දැයි චැට්බෝට්(chatbot එක) ඇසූ විට "ඔව්(yes)" යනුවෙන් පිළිතුරු දෙන්න. චැට්බෝට්හි පිහිටීම වෙනස් වන බව ඔබට දැකගත හැකිය.

\--- /task \---

\--- task \---

ඔබට නව `නම්(if)`{class="block3control"} කට්ටිය(block එක) ඇතුළත පහත කේතය(code එක) එකතු කළ හැකිය. එමගින් ඔබ "ඔව්(yes)" යනුවෙන් පිළිතුරු දෙන්නේ නම් චැට්බෝට්(chatbot එක) හතර වතාවක් ඉහළට හා පහළට පනීවි.

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> then
  switch backdrop to (moon v)

+ repeat (4) 
   change y by (10)
   wait (0.1) secs
   change y by (-10)
   wait (0.1) secs
  end 
end
```

\--- /task \---