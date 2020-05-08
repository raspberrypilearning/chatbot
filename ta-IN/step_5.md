## முடிவுகளை எடுத்தல்

உங்கள் சாட்போட்டைப் பெறும் பதில்களின் அடிப்படையில் என்ன செய்ய வேண்டும் என்பதைத் தீர்மானிக்க நீங்கள் அதை ப்ரொக்ராம் செய்யலாம்.

முதலில், உங்கள் சாட்போட் "ஆம்" அல்லது "இல்லை" என்று பதிலளிக்கக்கூடிய கேள்வியைக் கேட்க வைக்கப் போகிறீர்கள்.

\--- task \---

உங்கள் சாட்போட்டின் Codeஐ மாற்றவும். உங்கள் சாட்போட் `name`{:class="block3variables"} variable-ஐ பயன்படுத்தி "நீங்கள் நன்றாக இருக்கிறீர்களா name" என்ற கேள்வியைக் கேட்க வேண்டும். பின்னர், அதற்க்கு "ஆம்"(yes) என்று பதில் `வந்தால்0>{:class="block3control"}, "கேட்க மிகவும் நன்றாக உள்ளது!" என்ற திரும்ப சொல்ல வேண்டும். அதற்கு "இல்லை" என்று பதில் வந்தால் எதுவும் சொல்லக் கூடாது.</p>

<p><img src="images/chatbot-if-test1-annotated.png" alt="சாட்போட் பதிலைச் சோதித்தல்" /></p>

<p><img src="images/chatbot-if-test2.png" alt="சாட்போட் பதிலைச் சோதித்தல்" /></p>

<p><img src="images/nano-sprite.png" alt="நானோ ஸ்பிரிட்" /></p>

<pre><code class="blocks3">when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
end
`</pre> 

உங்கள் புதிய Codeஐ சரியாக சோதிக்க, நீங்கள் அதை "ஆம்"(yes) என்ற பதிலுடனும், "இல்லை"(no) என்ற பதிலுடனும் **இரண்டு முறை**: சோதிக்க வேண்டும்.

\--- /task \---

இந்த நேரத்தில், உங்கள் சாட்போட் "இல்லை" என்ற பதிலுக்கு எதுவும் சொல்லக் கூடாது.

\--- task \---

உங்கள் சாட்போட்டின் Codeஐ பின் கொண்டவாறு மாற்றவும், அது "நீங்கள் நன்றாக இருக்கிறீர்களா name" என்ற கேள்விக்கு "இல்லை(no)" என்று பதிலாக பெற்றால் , "Oh no!" என்று திரும்ப சொல்ல வேண்டும்.

`if, then`{:class="block3control"} என்ற பகுதியை `if, then, else`{:class="block3control"} பகுதியாக மாற்றவும். மேலும்,உங்கள் சாட்போட் "Oh no!"</code>{:class="block3looks"} என்று பதிலளிக்குமாறு Code செய்யவும். 

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
else 
+  say [Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

Test your code. நீங்கள் "இல்லை"(no) என்று பதிலளிக்கும் போது "ஆம்"(yes) என்று பதிலளிக்கும் போது உங்கள் சாட்போடிடம் இருந்து வெவ்வேறு பதிலைப் பெற வேண்டும்: நீங்கள் "ஆம்"((yes - இது கேப்பிடல்/ஸ்மால் கேஸாக இருக்கலாம்) என்று பதிலளிக்கும் போது, உங்கள் சாட்போட் "கேட்க மிகவும் நல்லது!" என்றும், மற்ற பதிலுக்கு "Oh no!" என்றும் கூற வேண்டும்.

![சாட்போட் பதிலைச் சோதித்தல்](images/chatbot-if-test2.png)

![சாட்போட்டின் ஆம்/இல்லை பதிலைச் சோதித்தல்](images/chatbot-if-else-test.png)

\--- /task \---

உங்கள் சாட்போட் பேசுவதற்கான Code மட்டுமல்லாமல்,நீங்கள் வேறு எந்த Codeயும் `if, then, else`{:class="block3control"} பகுதியினுள் வைக்கலாம்!

உங்கள் சாட்போட்டின் **Costumes** என்று இருக்கும் பகுதியைக் கிளிக் செய்தால், ஒன்றுக்கு மேற்பட்ட costume இருப்பதை நீங்கள் காண்பீர்கள்.

![சாட்போட் Costume-கள்](images/chatbot-costume-view-annotated.png)

\--- task \---

உங்கள் பதிலைத் டைப் செய்யும் போது சாட்போட் costume-களை மாற்றுமாறு, உங்கள் சாட்போட்டின் Codeஐ மாற்றவும்.

![Costume மாறுதலை சோதித்தல்](images/chatbot-costume-test1.png)

![Costume மாறுதலை சோதித்தல்](images/chatbot-costume-test2.png)

`if, then, else`{:class="block3control"} பகுதியில் உள்ள Codeஐ `switch costume`{:class="block3looks"} பகுதிக்கு மாற்றவும் 

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

உங்கள் Codeஐ சோதித்து சேவ் செய்யவும். உங்கள் பதிலைப் பொறுத்து உங்கள் சாட்போட்டின் முகம் மாற வேண்டும்.

\--- /task \---

உங்கள் சாட்போட்டின் costume மாறிய பிறகு, அது அப்படியே இருக்கும், ஆரம்பத்தில் இருந்ததை போல் மாறாது என்பதை நீங்கள் கவனித்தீர்களா?

நீங்கள் இதை முயற்சி செய்யலாம்: உங்கள் Codeஐ ரன் செய்து "இல்லை"(no) என்று பதிலளிக்கவும், இதனால் உங்கள் சாட்போட்டின் முகம் மகிழ்ச்சியற்ற தோற்றத்திற்கு மாறுகிறது. உங்கள் Codeஐ மீண்டும் ரன் செய்யவும், உங்கள் சாட்போட் உங்கள் பெயரைக் கேட்பதற்கு முன்பு மகிழ்ச்சியான முகமாக மாறாது என்பதைக் கவனியுங்கள்.

![Costume பிழை](images/chatbot-costume-bug-test.png)

\--- task \---

இந்த சிக்கலை சரிசெய்ய, `ஸ்பிரிட்டை க்ளிக் செய்யும்பொது`{:class="block3events"}, உங்கள் சாட்போட் Codeஐ `switch costume`{:class="block3looks"} தொடக்கத்தில் சேர்க்கவும்.

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Costume சரிசெய்தல் சோதனை](images/chatbot-costume-fix-test.png)

\--- /task \---