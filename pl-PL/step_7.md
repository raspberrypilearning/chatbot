## Zmiana lokalizacji

Możesz również zaprogramować swojego robota tak, żeby zmienił swoje położenie!

![Testowanie zmieniającego się tła](images/chatbot-backdrop-moon.png)

\--- task \---

Czy potrafisz zakodować swojego robota tak, by zapytał "Chcesz polecieć na księżyc?" a następnie zmienił tło, jeśli odpowiesz "tak"?

\--- wskazówka \---

\--- hint \---

Twój robot powinien `zapytać: „Chcesz polecieć na księżyc?”`{:class="block3sensing"} i `jeśli`{:class="block3control"} `Twoja odpowiedź`{:class="block3sensing"} brzmi „tak”, to powinien `przełączyć tło na księżyc`{:class="block3looks"}.

\--- /wskazówka \---

\--- hint \---

Oto bloczki kodu, które musisz dodać do kodu swojego robota.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /wskazówka \---

\--- hint \---

Tak powinien wyglądać Twój kod:

```blocks3
ask [Do you want to go to the moon?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /wskazówka \---

\--- /wskazówka \---

\--- /task \---

\--- task \---

Now you need to make sure that your chatbot starts in the right location when you click on it to talk to it. Add this block to the top of your chatbot code:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Test your program, and answer "yes" when the chatbot asks if you want to go to the moon. You should see that the chatbot’s location changes.

\--- /task \---

\--- task \---

You can also add the following code inside the new `if`{:class="block3control"} block to make the chatbot jump up and down four times if you answer "yes":

![nano sprite](images/nano-sprite.png)

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