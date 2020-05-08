## Changing location

உங்கள் சாட்போட்டின் இருப்பிடத்தை மாற்ற நீங்கள் அதை ப்ரொக்ராம் செய்யலாம்!

![Costume மாறுதலை சோதித்தல்](images/chatbot-backdrop-moon.png)

\--- task \---

"நீங்கள் சந்திரனுக்குச் செல்ல விரும்புகிறீர்களா" என்று கேட்க உங்கள் சாட்போட்டை ப்ரொக்ராம் செய்ய முடியுமா, பின்னர் பதில் "ஆம்" என்று இருக்கும்போது பின்னணியை மாற்ற முடியுமா?

\--- hints \---

\--- hint \---

உங்கள் சாட்போட் `"நீங்கள் சந்திரனுக்கு செல்ல விரும்புகிறீர்களா?"`{:class=block3sensing"} என்று கேட்க வேண்டும், அதன்பின் நீங்கள் "ஆம்" என்று `பதில்`{:class="block3sensing"} `கூறினால்`{:class="block3control"}, அது `பின்னணியை நிலவுக்கு மாற்ற வேண்டும்`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

உங்கள் சாட்போட் Code-இல் நீங்கள் சேர்க்க வேண்டிய Code பிளாக்ஸ் இங்கே.

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

உங்கள் Code எப்படி இருக்க வேண்டும்:

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

இப்போது உங்கள் சாட்போட் பேசுவதற்கு அதைக் கிளிக் செய்யும் போது சரியான இடத்தில் தொடங்குகிறது என்பதை உறுதிப்படுத்த வேண்டும். உங்கள் சாட்போட் Code-இன் மேலே இந்த தொகுதியைச் சேர்க்கவும்:

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

உங்கள் ப்ரொக்ராமை சோதித்துப் பாருங்கள், நீங்கள் சந்திரனுக்குச் செல்ல விரும்புகிறீர்களா என்று சாட்போட் கேட்கும்போது "ஆம்" என்று பதிலளிக்கவும். சாட்போட்டின் இருப்பிடம் மாறுவதை நீங்கள் பார்க்க வேண்டும்.

\--- /task \---

\--- task \---

நீங்கள் "ஆம்" என்று பதிலளித்தால் சாட்போட் நான்கு முறை மேல்,கீழ் செல்லுமாறு, புதிய `if`{:class="block3control"} பகுதிக்குள் பின்வரும் Codeஐ சேர்க்கலாம்:

![நானோ ஸ்பிரிட்](images/nano-sprite.png)

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