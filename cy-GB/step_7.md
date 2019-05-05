## Newid lleoliad

Galli di hefyd raglenni sy sgwrsfot i newid lleoliad!

![Profi cefndir sy'n newid](images/chatbot-backdrop-moon.png)

\--- task \---

Alli di raglenni dy sgwrsfot i ofyn "Wyt ti eisiau mynd i'r lleuad", ac yna newid y cefndir pan mai'r ateb yw "ydw"?

\--- hints \---

\--- hint \---

Fe ddylai dy sgwrsfot `ofyn "Wyt ti eisiau mynd i'r lleuad?"`{:class="block3sensing"}, yna `os`{:class="block3control"} rwyt ti'n `ateb`{:class="block3sensing"} "ydw", fe ddylai `newid y cefndir i'r lleuad`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Dyma'r blociau côd fyddi di angen eu hychwanegu i gôd dy sgwrsfot.

![corlun nano](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

Dyma sut dylai dy gôd edrych:

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

Mae angen i ti sicrhau fod dy sgwrsfot yn cychwyn yn y lleoliad cywir pan wyt ti'n clicio i siarad ag e. Ychwanega'r bloc yma i dop côd dy sgwrsfot:

![corlun nano](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Profa dy raglen, ac ateb "ydw" pan mae'r sgwrsfot yn gofyn os wyt ti eisiau mynd i'r lleuad. Fe ddyli di weld fod lleoliad y sgwrsfot yn newid.

\--- /task \---

\--- task \---

Mae modd i ti ychwanegu'r côd canlynol o fewn y bloc newydd `os`{:class="block3control"} i wneud i'r sgwrsfot neidio fyny ac i lawr pedair gwaith os wyt ti'n ateb "ydw":

![corlun nano](images/nano-sprite.png)

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