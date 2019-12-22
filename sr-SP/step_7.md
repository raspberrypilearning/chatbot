## Промена локације

Можеш да програмираш робота да мења локацију!

![Испробавање промене позадине](images/chatbot-backdrop-moon.png)

\--- task \---

Can you program your chatbot to ask "Do you want to go to the moon", and then change the backdrop when the answer is "yes"?

\--- hints \---

\--- hint \---

Your chatbot should `ask "Do you want to go to the moon?"`{:class="block3sensing"}, and `if`{:class="block3control"} you `answer`{:class="block3sensing"} "yes", it should `switch the backdrop to the moon`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Here are the code blocks you need to add to your chatbot code.

![нано лик](images/nano-sprite.png)

```blocks3
промени позадину у (месец v)

питај [Да ли желиш да идеш на Месец?] и чекај

ако је <(одговор) = [да]> онда

end
```

\--- /hint \---

\--- hint \---

Овако би требао да изгледа твој код:

```blocks3
питај [Да ли желиш да идеш на Месец?] и чекај
ако је <(одговор) = [да]> онда 
  промени позадину у (месец v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Now you need to make sure that your chatbot starts in the right location when you click on it to talk to it. Add this block to the top of your chatbot code:

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик

+ промени позадину у (свемир v)
```

\--- /task \---

\--- task \---

Испробај програм и одговори "да" када те робот упита да ли желиш да идеш на Месец. Требало би да видиш да је робот променио локацију.

\--- /task \---

\--- task \---

Можеш да додаш следећи код унутар новог блока `ако је`{:class="block3control"} да би робот скочио четири пута ако одговориш са "да":

![нано лик](images/nano-sprite.png)

```blocks3
ако је <(одговор) = [да]> онда 
  промени позадину у (месец v)

+  понови (4) 
    промени y за (10)
    чекај (0.1) секунду
    промени y за (-10)
    чекај (0.1) секунду
  end
end
```

\--- /task \---