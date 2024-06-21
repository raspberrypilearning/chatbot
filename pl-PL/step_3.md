## Gadający robot

Teraz, gdy masz już czatbota z osobowością, zaprogramujesz go tak, aby z Tobą rozmawiał.

--- task ---

Kliknij na swoim duszku czatbocie i dodaj do niego ten kod, aby `po kliknięciu`{:class="block3events"}, `zapytał o Twoje imię`{:class="block3sensing"}, a następnie `powiedział "Co za piękne imię!"`{:class="block3looks"}.

![nano duszek](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Jak masz na imię?] and wait
say [Co za piękne imię!] for (2) seconds
```

--- /task ---

--- task ---

Kliknij na swojego czatbota, aby przetestować swój kod. Gdy czatbot zapyta o Twoje imię, wpisz je w polu, które pojawi się na dole sceny, a następnie kliknij niebieski znak lub naciśnij <kbd>Enter</kbd>.

![Testowanie odpowiedzi robota gaduły](images/chatbot-ask-test1.png)

![Testowanie odpowiedzi Robota Gaduły](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

Teraz Twój czatbot stwierdza „Co za piękne imię!” za każdym razem, gdy odpowiadasz na jego pytanie. Możesz sprawić, aby odpowiedź czatbota była bardziej osobista i inna za każdym razem, gdy wpisywane jest kolejne imię.

Zmień kod duszka czatbota na `połącz`{:class="block3operators"} "Witaj" z `odpowiedzią`{:class="block3sensing"} do pytania "Jak masz na imię?", aby kod wyglądał tak:

![nano duszek](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Jak masz na imię?] and wait
+ say (join [Cześć ] (odpowiedź) ) for (2) seconds
```

![Testowanie spersonalizowanej odpowiedzi](images/chatbot-answer-test.png)

--- /task ---

--- task ---

Zapisując odpowiedź w **zmiennej**, możesz jej używać w dowolnym miejscu swojego projektu.

Utwórz nową zmienną o nazwie `imię`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Teraz zmień kod duszka chatbota, aby ustawić zmienną `imię`{:class="block3variables"} na `odpowiedź`{:class="block3sensing"}:

![nano duszek](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [Jak masz na imię?] and wait
+ set [imię v] to (answer)
+ say (join [Cześć ] (odpowiedź)) for (2) seconds
```

Twój kod powinien działać, jak wcześniej: robot powinien powiedzieć "cześć" i użyć wprowadzonego imienia.

![Testowanie spersonalizowanej odpowiedzi](images/chatbot-answer-test.png)

--- /task ---

Przetestuj swój program ponownie. Zwróć uwagę, że wpisana odpowiedź jest zapisana w zmiennej `imię`{:class="block3variables"} i jest również wyświetlana w lewym górnym rogu sceny. Aby spowodować, że odpowiedź zniknie ze sceny, przejdź do sekcji bloczków `Dane`{:class="block3variables"} i kliknij pole obok `imię`{:class="block3variables"} tak, aby nie było zaznaczone.