## முடிவுகளை எடுத்தல்

உங்கள் சாட்பாட்டை, அது பெறும் பதில்களின் அடிப்படையில், என்ன செய்ய வேண்டும் என்பதைத் தீர்மானிக்குமாறு நீங்கள் அதை நிரல் செய்யலாம்.

முதலில், உங்கள் சாட்பாட்டை "yes"(ஆம்) அல்லது "no"(இல்லை) என்று பதிலளிக்கக்கூடிய ஒரு கேள்வியைக் கேட்க வைக்கப் போகிறீர்கள்.

\--- task \---

உங்கள் சாட்பாட்டின் குறியீட்டை மாற்றவும். உங்கள் சாட்பாட் `name`{:class="block3variables"} மாறியை பயன்படுத்தி "நீங்கள் நன்றாக இருக்கிறீர்களா name"("Are you OK name") என்ற கேள்வியைக் கேட்க வேண்டும். பின்னர், அதற்கு "ஆம்" என்று பதில் வந்தால் (`if`{:class="block3control"}), "கேட்க மிகவும் நன்றாக உள்ளது!"("That's great to hear!") என்று திரும்ப பதில் சொல்ல வேண்டும். அதற்கு "இல்லை" என்று பதில் வந்தால், எதுவும் சொல்லக் கூடாது.

![சாட்பாட் பதிலைச் சோதித்தல்](images/chatbot-if-test1-annotated.png)

![சாட்பாட் பதிலைச் சோதித்தல்](images/chatbot-if-test2.png)

![நானோ sprite](images/nano-sprite.png)

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

உங்கள் புதிய குறியீட்டை சரியாக சோதிக்க, நீங்கள் அதை **இரண்டு முறை** சோதிக்க வேண்டும்: ஒருமுறை "yes"(ஆம்) என்ற பதிலுடனும், மற்றொருமுறை "no "(இல்லை) என்ற பதிலுடனும்.

\--- /task \---

இந்த நேரத்தில், உங்கள் சாட்பாட் "no" என்ற பதிலுக்கு எதுவும் சொல்லவில்லை.

\--- task \---

உங்கள் சாட்பாட்டின் குறியீட்டை பின்வருமாறு மாற்றவும், அது "Are you OK name" என்ற கேள்விக்கு "no" என்று பதிலாக பெற்றால் , "Oh no!"(ஓ இல்லை!) என்று பதில் சொல்ல வேண்டும்.

`If, then`{:class="block3control"} தொகுதியை `if, then, else`{:class="block3control"} தொகுதியாக மாற்றவும். மேலும், உங்கள் சாட்பாட் "Oh no!" என்று பதிலளிக்குமாறு(`say "Oh no!"`{:class="block3looks"}) குறியீட்டைச் சேர்க்கவும். 

![நானோ sprite](images/nano-sprite.png)

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

உங்கள் குறியீட்டை சோதிக்கவும். நீங்கள் "இல்லை"(no) என்று பதிலளிக்கும் போதும், "ஆம்"(yes) என்று பதிலளிக்கும் போதும் உங்கள் சாட்பாட்டிடம் இருந்து வெவ்வேறு பதிலைப் பெற வேண்டும்: நீங்கள் "ஆம்"(yes - இது கேப்பிடல்/ஸ்மால் லெட்டராக இருக்கலாம்) என்று பதிலளிக்கும் போது, உங்கள் சாட்பாட் "That’s great to hear!" என்றும், **வேறு எந்த பதிலுக்கும்** "Oh no!" என்றும் கூற வேண்டும்.

![சாட்பாட் பதிலைச் சோதித்தல்](images/chatbot-if-test2.png)

![சாட்பாட்டின் ஆம்/இல்லை பதிலைச் சோதித்தல்](images/chatbot-if-else-test.png)

\--- /task \---

உங்கள் சாட்பாட் பேசுவதற்கான குறியீடு மட்டுமல்லாமல், நீங்கள் வேறு எந்த குறியீட்டையும் `if, then, else`{:class="block3control"} தொகுதியினுள் வைக்கலாம்!

உங்கள் சாட்பாட்டின் **Costumes** என்று இருக்கும் பகுதியைக் கிளிக் செய்தால், ஒன்றுக்கு மேற்பட்ட costume இருப்பதை நீங்கள் காண்பீர்கள்.

![சாட்பாட் Costume-கள்](images/chatbot-costume-view-annotated.png)

\--- task \---

உங்கள் பதிலைத் தட்டச்சு செய்யும் போது, சாட்பாட் costume-களை மாற்றுமாறு(switch), உங்கள் சாட்பாட்டின் குறியீட்டை மாற்றவும்.

![Costume மாறுதலை சோதித்தல்](images/chatbot-costume-test1.png)

![Costume மாறுதலை சோதித்தல்](images/chatbot-costume-test2.png)

`If, then, else`{:class="block3control"} தொகுதியின் உள்ளே உள்ள குறியீட்டை, `switch costume`{:class="block3looks"} தொகுதிக்கு மாற்றவும்.

![நானோ sprite](images/nano-sprite.png)

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

உங்கள் குறியீட்டை சோதித்து, பின் சேமிக்கவும். உங்கள் பதிலைப் பொறுத்து, உங்கள் சாட்பாட்டின் முகம் மாறுவதைக் காணலாம்.

\--- /task \---

உங்கள் சாட்பாட்டின் costume மாறிய பிறகு, அது தொடர்ந்து அப்படியே இருக்கும், ஆரம்பத்தில் இருந்ததை போல் மாறாது என்பதை நீங்கள் கவனித்தீர்களா?

நீங்கள் இதை முயற்சி செய்யலாம்: உங்கள் குறியீட்டை இயக்கி "இல்லை"(no) என்று பதிலளிக்கவும், இதனால் உங்கள் சாட்பாட்டின் முகம் மகிழ்ச்சியற்ற தோற்றத்திற்கு மாறுகிறது. உங்கள் குறியீட்டை மீண்டும் இயக்கவும், உங்கள் சாட்பாட், உங்கள் பெயரைக் கேட்பதற்கு முன்பு, மகிழ்ச்சியான முகமாக மாறாது என்பதைக் கவனியுங்கள்.

![Costume பிழை](images/chatbot-costume-bug-test.png)

\--- task \---

இந்த சிக்கலை சரிசெய்ய, தொடக்கத்தில் sprite கிளிக் செய்யப்படும்போது(`when the sprite is clicked`{:class="block3events"}), உங்கள் சாட்பாட் குறியீட்டுடன் `switch costume`{:class="block3looks"} தொகுதியைச் சேர்க்கவும்.

![நானோ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Costume சரிசெய்தல் சோதனை](images/chatbot-costume-fix-test.png)

\--- /task \---