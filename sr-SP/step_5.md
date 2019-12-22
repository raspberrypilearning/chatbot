## Доношење одлука

Можеш да програмираш робота да одлучи шта ће урадити на основу одговора које добије.

Прво ћеш направити да твој робот постави питање на које се може одговорити са "да" или "не".

\--- task \---

Промени код свог робота. Твој робот би требао да постави питање "Јеси ли добро ", користећи променљиву `име`{:class="block3variables"}. Затим би требао одговорити "То је сјајно чути!" `ако`{:class="block3control"} добије одговор "да", али да не каже ништа ако је одговор "не".

![Испробавање роботовог одговора](images/chatbot-if-test1-annotated.png)

![Испробавање роботовог одговора](images/chatbot-if-test2.png)

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
нека [име v] буде (одговор)
изговори (споји [Здраво ] и (име)) током (2) секунде
+питај (споји [Јеси ли добро ] и (име)) и чекај
+ако је <(одговор) = [да]> онда 
  изговори [То је сјајно чути!] током (2) секунде
end
```

Да правилно испробаш свој нови код, мораћеш да га испробаш **двапут**: једном са одговором "да", а једном са одговором "не".

\--- /task \---

Тренутно твој робот не каже ништа на одговор "не".

\--- task \---

Промени код робота, тако да одговори "О, не!" ако на питање "Јеси ли добро " добије одговор "не".

Замени блок `ако је, онда`{:class="block3control"} са блоком `ако је, онда, у супротном`{:class="block3control"} и додај код како би робот могао `рећи "О. не!"`{:class="block3looks"}.

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
нека [име v] буде (одговор)
изговори (споји [Здраво ] и (име)) током (2) секунде
питај (споји [Јеси ли добро ] и (име)) и чекај

+ ако је <(одговор) = [да]> онда 
  изговори [То је сјајно чути!] током (2) секунде
у супротном 
+  изговори [О, не!] током (2) секунде
end
```

\--- /task \---

\--- task \---

Испробај свој код. You should get a different response when you answer "no" and when you answer "yes": your chatbot should reply with "That’s great to hear!" when you answer "yes" (which is not case-sensitive), and reply with "Oh no!" when you answer **anything else**.

![Испробавање роботовог одговора](images/chatbot-if-test2.png)

![Испробавање одговора да/не](images/chatbot-if-else-test.png)

\--- /task \---

Можеш ставити било који код унутар блока `ако је, онда, у супротном`{:class="block3control"}, не само код који омогућава твојем роботу да говори!

Ако кликнеш на свог робота, а затим на картицу **Костими**, видећеш да твој робот има више костима.

![костими робота](images/chatbot-costume-view-annotated.png)

\--- task \---

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Испробавање промене костима](images/chatbot-costume-test1.png)

![Испробавање промене костима](images/chatbot-costume-test2.png)

Change the code inside the `if, then, else`{:class="block3control"} block to `switch costume`{:class="block3looks"}.

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик
питај [Како се зовеш?] и чекај
нека [име v] буде (одговор)
изговори (споји [Здраво ] и (име)) током (2) секунде
питај (споји [Јеси ли добро ] и (име)) и чекај
ако је <(одговор) = [да]> онда 

+  замени костим са (нано-ц v)
  изговори [То је сјајно чути!] током (2) секунде
у супротном 
+  замени костим са (нано-д v)
  изговори [О, не!] током (2) секунде
end
```

Испробај и сачувај свој код. Лице твог робота би требало да се мења у зависности од твог одговора.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Костим грешка](images/chatbot-costume-bug-test.png)

\--- task \---

Да поправиш овај проблем, додај роботовом коду `замени костим са`{:class="block3looks"} на почетку `када је кликнуто на овај лик`{:class="block3events"}.

![нано лик](images/nano-sprite.png)

```blocks3
када је кликнуто на овај лик

+ замени костим са (нано-а v)
питај [Како се зовеш?] и чекај
```

![Испробавање поправке костима](images/chatbot-costume-fix-test.png)

\--- /task \---