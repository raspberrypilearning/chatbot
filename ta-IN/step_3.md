## பேசும் சாட்பாட்

இப்போது நீங்கள் ஆளுமையுடன் கூடிய ஒரு சாட்பாட் வைத்திருக்கிறீர்கள், உங்களுடன் பேச அதை நிரல் செய்யப் போகிறீர்கள்.

--- task ---

உங்கள் சாட்பாட் sprite-ஐக் கிளிக் செய்து, அதனுடன் இந்த குறியீட்டைச் சேர்க்கவும். இதனால், அது கிளிக் செய்யப்படும்போது(`when it's clicked`{:class="block3events"}), உங்கள் பெயரைக் கேட்கும்(`asks for your name`{:class="block3sensing"}). அதன் பின்னர், "என்ன ஒரு அழகான பெயர்!" என்று பதில் அளிக்கும்(`says "What a lovely name!"`{:class="block3looks"}).

![நானோ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say [What a lovely name!] for (2) seconds
```

--- /task ---

--- task ---

உங்கள் குறியீட்டைச் சோதிக்க உங்கள் சாட்பாட்டைக் கிளிக் செய்க. சாட்பாட், உங்கள் பெயரைக் கேட்கும்போது, மேடையின்(stage) அடிப்பகுதியில் தோன்றும் பெட்டியில் தட்டச்சு செய்து, பின்னர் நீல நிறக் குறியைக் கிளிக் செய்யவும் அல்லது <kbd>Enter</kbd>ஐ அழுத்தவும்.

![சாட்பாட் பதிலைச் சோதித்தல்](images/chatbot-ask-test1.png)

![சாட்பாட் பதிலைச் சோதித்தல்](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

இப்போது, உங்கள் சாட்பாட் "என்ன ஒரு அழகான பெயர்!" என ஒவ்வொரு முறையும் பதிலளிக்கும். நீங்கள் சாட்பாட்டின் பதிலை மிகவும் தனிப்பட்டதாக மாற்றலாம், இதன்மூலம் ஒவ்வொரு முறையும் வேறு பெயர் தட்டச்சு செய்யும் போது, வெவ்வேறு பதில் கிடைக்கும்.

சாட்பாட் sprite-இன் குறியீட்டை பின்வருமாறு மாற்றவும். "உங்கள் பெயர் என்ன?" என்ற கேள்வியின் பதிலுடன்(`answer`{:class="block3sensing"}) "Hi"(ஹாய்) என்று இணைக்கவும்(`join`{:class="block3operators"}). இதனால், உங்கள் குறியீடு பின்வருமாறு இருக்கும்:

![நானோ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
say (join [Hi ] (answer) :: +) for (2) seconds
```

![தனிப்பயனாக்கப்பட்ட பதிலைச் சோதித்தல்](images/chatbot-answer-test.png)

--- /task ---

--- task ---

பதிலை ஒரு மாறியில்( **variable**) சேமிப்பதன் மூலம், அதனை திட்டத்தில் எங்கு வேண்டுமானாலும் பயன்படுத்தலாம்.

`Name`{:class="block3variables"} (பெயர்) எனப்படும் புதிய மாறியை உருவாக்கவும்.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

இப்போது, உங்கள் சாட்பாட் sprite-இன் குறியீட்டை, `name`{:class="block3variables"} மாறியில் பதிலை(`answer`{:class="block3sensing"}) அமைக்குமாறு(set) மாற்றம் செய்யவும். 

![நானோ sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait

+ set [name v] to (answer)
say (join [Hi ] (name :: variables +)) for (2) seconds
```

உங்கள் குறியீடு முன்பு போலவே செயல்பட வேண்டும்: நீங்கள் தட்டச்சு செய்யும் பெயரைப் பயன்படுத்தி உங்கள் சாட்பாட் ஹாய் சொல்ல வேண்டும்.

![தனிப்பயனாக்கப்பட்ட பதிலைச் சோதித்தல்](images/chatbot-answer-test.png)

--- /task ---

உங்கள் நிரலை மீண்டும் சோதிக்கவும். நீங்கள் தட்டச்சு செய்யும் பதில் `name`{:class="block3variables"} மாறியில் சேமிக்கப்படுவதைக் கவனியுங்கள், மேலும் இது மேடையின் மேல் இடது மூலையிலும் காட்டப்படுகிறது. இது மேடையிலிருந்து மறைந்து போக,`Variables`{:class="block3variables"} தொகுதிகள் பகுதிக்கு செல்லவும், பிறகு `name`{:class="block3variables"}-க்கு அடுத்துள்ள பெட்டியைக் கிளிக் செய்க. இதனால் அந்த பெட்டி குறிக்கப்படாமல் இருக்கும்.