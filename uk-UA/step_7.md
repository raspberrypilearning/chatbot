## Зміна розташування

Також ти можеш запрограмувати свого чат-бота, щоб він змінював своє розташування!

![Тестування зміни тла](images/chatbot-backdrop-moon.png)

\--- task \---

Чи можеш ти запрограмувати свого чат-бота запитувати "Хочеш полетіти на Місяць?" і після відповіді "так" змінювати тло?

\--- hints \---

\--- hint \---

Твій чат-бот має `запитати "Хочеш полетіти на Місяць?"`{:class="block3sensing"}, і `якщо`{:class="block3control"} твоя `відповідь`{:class="block3sensing"} — "так", він має `змінити тло на moon`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Ось блоки, які тобі треба буде додати до коду свого чат-бота.

![спрайт nano](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Do you want to go to the moon?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

Ось як має виглядати твій код:

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

Тепер тобі треба переконатися, що твій чат-бот розпочинає в правильному місці, коли ти клацаєш на нього для початку розмови. Додай цей блок вгорі коду для чат-бота:

![спрайт nano](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Протестуй свою програму і скажи "так", коли чат-бот запитає, чи хочеш ти полетіти на Місяць. Ти маєш побачити, як змінюється розташування чат-бота.

\--- /task \---

\--- task \---

Ти також можеш додати наступний код всередині блоку `якщо`{:class="block3control"}, щоб твій чат-бот підстрибував чотири рази, коли ти відповідаєш "так":

![спрайт nano](images/nano-sprite.png)

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