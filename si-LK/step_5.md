## තීරණ ගැනීම

ඔබට ලැබෙන පිළිතුරු මත පදනම්ව කුමක් කළ යුතුද යන්න තීරණය කිරීම සඳහා ඔබේ චැට්බෝට්(chatbot) වැඩසටහන්ගත(program) කළ හැකිය.

පළමුව, ඔබ ඔබේ චැට්බෝට්(chatbot) එක මගින් "ඔව්(yes)" හෝ "නැත(no)" යනුවෙන් පිළිතුරු දිය හැකි ආකාරයේ ප්‍රශ්නයක් ඇසීමට සලස්වයි.

\--- task \---

ඔබගේ චැට්බෝට්(chatbot) එකේ කේතය(code එක) වෙනස් කරන්න. ඔබේ චැට්බෝට්(chatbot) එක විසින් `නාමය(name)`{:class="block3variables"} විචල්‍යය(variable එක) භාවිතා කරමින් <0>ඔබට කොහොමද නාමය("Are you OK name")</0> යන ප්‍රශ්නය ඇසිය යුතුය. එයට ලැබෙන පිළිතුර "ඔව්"("yes") `නම්(if)`{:class="block3control"} එවිට එය පිළිතුරු දිය යුත්තේ "එය ඇසීමත් සතුටක්!"("That's great to hear!") ලෙසටයි, නමුත් පිළිතුර "නැත"("no") නම් කිසිවක් නොකියා සිටියයුතුයි.

![චැට්බෝට්(chatbot ගේ) ප්‍රතිචාරයක් පරීක්ෂා(test) කිරීම](images/chatbot-if-test1-annotated.png)

![චැට්බෝට්(chatbot ගේ) ප්‍රතිචාරයක් පරීක්ෂා(test) කිරීම](images/chatbot-if-test2.png)

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then
  say [That's great to hear!] for (2) seconds
end
```

ඔබගේ නව කේතය නිසියාකාරව පරීක්ෂා(test) කිරීමට, ඔබ එය **දෙවරක්(twice)** පරීක්ෂා කළ යුතුය: වරක් "ඔව්"("yes") යන පිළිතුර යොදමින් හා, එක් වරක් "නැත"("No") යන පිළිතුර යොදමින් පරීක්ෂා කිරීම වඩා සුදුසු වේ.

\--- /task \---

මේ මොහොතේ, ඔබගේ චැට්බෝට්(chatbot එක) "නැත"("no") යන පිළිතුරට කිසිවක් නොකියයි.

\--- task \---

"ඔබට කොහොමද නාමය" ("Are you OK name") යන ප්‍රශ්නයට "නැත"("no") යන්න පිළිතුර ලෙස ලැබෙන්නේ නම්, එවිට එය "අහො ඛේදයකි!"("Oh no!") ලෙස පිළිවදන් දෙන පරිදි ඔබගේ චැට්බෝට්(chatbot) එකේ කේතය(code එක) වෙනස් කරන්න.

`එසේ නම් මෙසේ(if, then)`{:class="block3control"} කේතය `එසේ නම් මෙසේ නැත්නම්(if, then, else)` {:class="block3control"} කේතය මගින් ප්‍රතිස්ථාපනය කර, චැට්බොට්(chatbot එක) `"අහො ඛේදයකි!"("Oh no!") ලෙස පිළිවදන් දෙන පරිදි`{:class="block3looks"} සකසන්න.

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then
  say [That's great to hear!] for (2) seconds
else 
+ say [Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

ඔබේ කේතය(code එක) පරීක්ෂා(test) කරන්න. ඔබ "නැත(no)" යනුවෙන් පිළිතුරු දෙන විට සහ "ඔව්(yes)" යනුවෙන් පිළිතුරු දෙන විට ඔබට වෙනස් ප්‍රතිචාරයක් ලැබිය යුතුය: ඔබ "ඔව්(yes)" යනුවෙන් පිළිතුරු දෙන විට ඔබේ චැට්බෝට්(chatbot) පිළිතුරු දිය යුත්තේ "එය ඇසීමත් සතුටක්!"("That’s great to hear!") [එය විෂය සංවේදී(case sensitive) නොවේ], සහ **වෙනත් ඕනෑම පිළිතුරකට(anything else)** "අහො ඛේදයකි!"("Oh no!") ලෙස පිළිවදන් දියයුතුය. 

![චැට්බෝට්(chatbot ගේ) ප්‍රතිචාරයක් පරීක්ෂා(test) කිරීම](images/chatbot-if-test2.png)

![ඔව් / නැත පිළිතුරක් පරීක්ෂා කිරීම](images/chatbot-if-else-test.png)

\--- /task \---

ඔබේ චැට්බෝට්(chatbot එක) කතා කරවන කේතය(code එක) පමණක් නොව!, ඔබට ඕනෑම කේතයක්(code එකක්) `එසේ නම් මෙසේ නැත්නම්(if, then, else)`{:class="block3control"} කට්ටිය(block එක) ඇතුළත යෙදිය හැකිය, 

ඔබ ඔබේ චැට්බෝට්(chatbot's) හි **ඇඳුම්(Costume)** පටිත්ත(tab එක) ක්ලික් කළහොත්, එහි එක් ඇඳුමකට(costume එකකට) වඩා ඇති බව ඔබට පෙනෙනු ඇත.

![චැට්බෝට්(chatbot) ඇඳුම්(costumes)](images/chatbot-costume-view-annotated.png)

\--- task \---

ඔබේ පිළිතුර ටයිප් කරන විට චැට්බෝට්ගේ(chatbot's) ඇඳුම්(costume එක) මාරු වන පරිදි ඔබේ චැට්බෝට්ගේ(chatbot's ) කේතය වෙනස් කරන්න.

![වෙනස්වන ඇඳුම්(costume) පරීක්ෂා(test) කිරීම](images/chatbot-costume-test1.png)

![වෙනස්වන ඇඳුම්(costume) පරීක්ෂා(test) කිරීම](images/chatbot-costume-test2.png)

`එසේ නම් මෙසේ නැත්නම් (if, then, else)` {:class="block3control"} කට්ටිය(block එක) ඇතුළත ඇති කේතය `ඇඳුම් මාරු කරන්න(switch costume`{:class="block3looks"} ලෙසට වෙනස් කරන්න.

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then

+ switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+ switch costume to (nano-d v)
  say [Oh no!] for (2) seconds 
end
```

ඔබේ කේතය(code එක) පරීක්ෂා(test) කර සුරකින්න(save කරන්න). ඔබ දෙන පිළිතුර අනුව ඔබේ චැට්බෝට්ගේ(chatbot's) මුහුණ(face එක) වෙනස් වීම ඔබට දැකගත හැකිවේ.

\--- /task \---

ඔබේ චැට්බෝට්ගේ(chatbot ගේ) ඇඳුම(costume එක) වෙනස් වූ පසු, එය එලෙසම පවතින අතර ආරම්භයේ තිබූ තත්වයට එය වෙනස් නොවන බව ඔබ දුටුවාද?

ඔබට මෙය අත්හදා බැලිය හැකිය: ඔබේ කේතය(code එක) ධාවනය(run) කර "නැත(no)" යනුවෙන් පිළිතුරු දෙන්න එවිට ඔබගේ චැට්බෝට්ගේ(chatbot's) මුහුණ(face) අසතුටු(unhappy) පෙනුමකට වෙනස් වේ. ඉන්පසු ඔබේ කේතය(code එක) නැවත ධාවනය(run) කර ඔබගේ නම විමසීමට පෙර, ඔබේ චැට්බෝට්ගේ(chatbot's) මුහුණ සතුටු එකක් බවට නැවත පරිවර්තනය නොවන බව සැලකිල්ලට ගන්න.

![ඇඳුම්(costume) දෝෂය(bug)](images/chatbot-costume-bug-test.png)

\--- task \---

මෙම ගැටළුව විසඳීම සඳහා, ආරම්භයේ දී `sprite එක ක්ලික් කළ විට `{:class="block3events"}.`ඇඳුම් මාරු කරන(switch costume)`{:class="block3looks"} පරිදි චැට්බෝට්ගේ(chatbot's) කේතය(code එක) සකස් කරන්න. 

![නැනෝ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![ඇඳුම්(costume) නිවැරදි(fix) කිරීමක් පරීක්ෂා(test) කිරීම](images/chatbot-costume-fix-test.png)

\--- /task \---