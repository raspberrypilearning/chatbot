## Gwneud penderfyniadau

Mae modd rhaglenni dy SgwrsBot i ddewis beth i wneud, yn ddibynol ar ymateb y defnyddiwr.

+ Awn ati i wneud i dy SgwrsBot ofyn cwestiwn i'r defnyddiwr sydd ag ateb 'ydw' neu 'nac ydw'. Dyma enghraifft, ond mae modd i ti hefyd newid y cwestiwn:

	```blocks
		pan caiff y cymeriad ei glicio
		gofyn [Helo! Beth yw dy enw?] ac aros
		gosod [enw v] i (ateb)
		dweud <uno [Helo] (enw)> am (2) eiliad
		gofyn <uno [Wyt ti'n iawn] (enw)> ac aros
		os ((ateb) = [ydw]) wedyn
   		dweud [Mae'n dda i glywed!] am (2) eiliad
		end
	```

	Sylwa nawr dy fod di wedi arbed dy enw defnyddiwr fel amrywiad, mae modd i ti ei ddefnyddio cymaint a hoffet ti.

+ I brofi y rhaglen yma yn iawn, bydd angen i ti ei brofi ddwywaith - unwaith yn teipio 'nac ydw' fel dy ateb, ac unwaith yn teipio 'ydw'.  Fe ddyle ti ond gael ateb gan dy Sgwrsbot 'os' wyt ti'n ateb 'ydw'.

+ Y broblem gyda dy SgwrsBot yw nad yw e'n ateb os yw'r defnyddiwr yn ateb 'nac ydw'.  Mae modd trwsio hyn trwy newid y bloc {.blockcontrol} 'os' i floc 'os/wedyn' {.blockcontrol}, fel bod dy gôd yn edrych fel hyn:

	```blocks
		pan caiff y cymeriad ei glicio
		gofyn [Helo! Beth yw dy enw?] ac aros
		gosod [enw v] i (ateb)
		dweud <uno [Helo] (enw)> am (2) eiliad
		gofyn <uno [Wyt ti'n iawn?] (name)> ac aros
		os ((ateb) = [ydw]) wedyn
		dweud [Mae'n dda i glywed!] am (2) eiliad
			fel arall
   		dweud [O na!] am (2) eiliad
		end
	```

+ Os wyt ti'n profi dy gôd, fe wnei di nawr weld dy fod yn cal ymateb pan wyt ti'n ateb 'ie' neu 'na'.  Os yw dy sgwrsbot yn ymateb gyda 'Mae hynny'n wych i glywed!' pan wyt ti'n ateb 'ie', ond yn ymateb gyda 'O na!' os wyt ti'n teipio unrhywbeth heblaw 'ie' (`else` {.blockcontrol} means 'otherwise').

	![screenshot](images/chatbot-else.png)

+ Mae modd i ti roi unrhyw côd yn y bloc 'os' {.blockcontrol}  neu 'arall' {.blockcontrol}, nid dim ond y côd sy'n gwneud i dy Sgwrsbot siarad. Er enghraifft, mae modd i ti newid gwisg y SgwrsBot i fod yr un peth â'r ymateb.

	Os wyt ti'n edrych ar wisgoedd y SgwrsBot, mae'n bosib y byddi di'n gweld bod mwy nag un. (Os na, mae modd i ti ychwanegu mwy dy hunan!)

	![screenshot](images/chatbot-costumes.png)

	Mae modd i ti ddefnyddio'r gwisgoedd yma fel rhan o ymateb dy Sgwrsbot, trwy ychwanegu y côd yma:

	![screenshot](images/chatbot-costumes-code.png)

+ Profa dy raglen, ac fe ddyle ti weld gwyneb dy sgwrsbot yn newid yn dibynnu ar yr ateb rwyt ti'n ei roi.

	![screenshot](images/chatbot-face.png)

--- challenge ---
## Her: Mwy o benderfyniadau 

Rhaglena dy SgwrsBot i ofyn cwestiwn arall - rhywbeth gydag ateb 'ie' neu 'na'. Wyt ti'n gallu gwneud i dy SgwrsBot ymateb i dy ateb?

![screenshot](images/chatbot-joke.png)
--- /challenge ---
