## Sgwrsfot sy'n siarad

Mae gen ti sgwrfot sydd â phersonoliaeth, y cam nesaf yw ei raglenni i siarad â thi.

\--- task \---

Clicia'r corlun sgwrsfot, ac ychwanegu'r côd yma fel ei fod {:class="block3events"} `pan gaiff ei glicio`, yn `gofyn dy enw`{:class="block3sensing"} ac yna `yn dweud "Am enw hyfryd!`{:class="block3looks"}.

![corlun nano](images/nano-sprite.png)

```blocks3
pan gaiff y ciplun yma ei glicio
gofyn [Beth yw dy enw?] ac aros
dweud [Am enw hyfryd!] am (2) eiliad
```

\--- /task \---

\--- task \---

Clicia dy sgwrsfot i brofi dy gôd. Pan mae'r sgwrsfot yn gofyn dy enw, teipia dy enw i'r bocs sy'n ymddangos ar waelod y Llwyfan, yna clicio'r marc glas neu gwasgu <kbd>Enter</kbd>.

![Profi ymateb sgwrsfot](images/chatbot-ask-test1.png)

![Profi ymateb sgwrsfot](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Mae dy sgwrsfot yn ateb ‘Am enw hyfryd!’ bob tro. Mae modd personoleiddio ymateb y sgwrsbot, fel fod yr ateb yn wahanol bob tro rwyt ti'n teipio dy enw.

Newida côd y sgwrsfot i `uno`{:class="block3operators"} "Helo" gydag `ateb` {:class="block3sensing"} i'r cwestiwn "Beth yw dy enw?", fel fod y côd yn edrych fel hyn:

![corlun nano](images/nano-sprite.png)

```blocks3
pan gaiff y ciplun yma ei glicio
gofyn [Beth yw dy enw?] ac aros
dweud (uno [Helo ] (ateb) :: +) am (2) eiliad
```

![Profi ateb personol](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

Trwy storio'r ateb fel ** newidyn**, mae modd ei ddefnyddio yn unrhyw le yn eich prosiect.

Creu newidyn newydd o'r enw `enw`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Nawr, newida côd dy sgwrsfot i osod y newidyn `enw` {: class = "block3variables}} i `ateb` {: class = "block3sensing"}:

![corlun nano](images/nano-sprite.png)

```blocks3
pan gaiff y ciplun yma ei glicio
gofyn [Beth yw dy enw?] ac aros

+ gosod [enw v] i (ateb)
dweud (uno [Helo ] (enw :: + variables)) am (2) eiliad
```

Fe ddylai dy gôd weithio fel o'r blaen: dy sgwrsfot yn dweud helo pan wyt ti'n teipio dy enw.

![Profi ateb personol](images/chatbot-answer-test.png)

\--- /task \---

Profa dy raglen eto. Sylwa pan wyt ti'n teipio dy ateb mae'n cael ei arbed yn y newidyn `enw`{:class="block3variables"}, ac hefyd yn ymddangos ar ochr top chwith y Llwyfan. I wneud iddo ddiflannu o'r Llwyfan, cer i adran flociau `Data`{:class="block3variables"} a clicio ar y blwch dros nesaf i `enw`{:class="block3variables"} fel nad yw wedi ei farcio.