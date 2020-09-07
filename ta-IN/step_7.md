## இருப்பிடத்தை மாற்றுதல்

உங்கள் சாட்பாட்டின் இருப்பிடத்தை மாற்ற நீங்கள் அதை நிரல் செய்யலாம்!

![பின்னணி மாறுதலை சோதித்தல்](images/chatbot-backdrop-moon.png)

--- task ---

"நீங்கள் சந்திரனுக்குச் செல்ல விரும்புகிறீர்களா"("Do you want to go to the moon") என்று கேட்குமாறு உங்கள் சாட்பாட்டை நிரல் செய்ய முடியுமா, பின்னர் பதில் "ஆம்" என்று இருந்தால், பின்னணியை மாற்ற முடியுமா?

--- hints ---


--- hint ---

உங்கள் சாட்பாட் "நீங்கள் சந்திரனுக்கு செல்ல விரும்புகிறீர்களா?" என்று கேட்க வேண்டும்(`ask "Do you want to go to the moon?"`{:class="block3sensing"}), அதன்பின் ஒருவேளை(`if`{:class="block3control"}), நீங்கள் "ஆம்" என்று பதில்(`answer`{:class="block3sensing"}) கூறினால், அது பின்னணியை நிலவுக்கு மாற்ற வேண்டும் (`switch the backdrop to the moon`{:class="block3looks"}).

--- /hint ---

--- hint ---

உங்கள் சாட்பாட் குறியீட்டில் நீங்கள் சேர்க்க வேண்டிய குறியீட்டு தொகுதிகள் இங்கே.

![நானோ sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

--- /hint ---

--- hint ---

உங்கள் குறியீடு இவ்வாறு இருக்க வேண்டும்:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

இப்போது உங்கள் சாட்பாட்டுடன் பேசுவதற்காக அதைக் கிளிக் செய்யும் போது, சாட்பாட் சரியான இருப்பிடத்தில் இருந்து தொடங்குகிறதா என்பதை உறுதிப்படுத்த வேண்டும். உங்கள் சாட்பாட் குறியீட்டின் தொடக்கத்தில் இந்த தொகுதியைச் சேர்க்கவும்:

![நானோ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

--- /task ---

--- task ---

உங்கள் நிரலைச் சோதித்துப் பாருங்கள், நீங்கள் சந்திரனுக்குச் செல்ல விரும்புகிறீர்களா என்று சாட்பாட் கேட்கும்போது "ஆம்"(yes) என்று பதிலளிக்கவும். சாட்பாட்டின் இருப்பிடம் மாறுகிறது என்பதை நீங்கள் பார்க்கலாம்.

--- /task ---

--- task ---

நீங்கள் "ஆம்" என்று பதிலளித்தால் சாட்பாட்டை நான்கு முறை மேலும், கீழும் குதிக்குமாறு செய்ய, புதிய `if`{:class="block3control"} தொகுதிக்குள் பின்வரும் குறியீட்டையும் சேர்க்கலாம்:

![நானோ sprite](images/nano-sprite.png)

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