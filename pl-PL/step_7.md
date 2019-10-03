## Zmiana lokalizacji

Możesz również zaprogramować swojego robota tak, żeby zmienił swoje położenie!

![Testowanie zmieniającego się tła](images/chatbot-backdrop-moon.png)

--- task ---

Czy potrafisz zakodować swojego robota tak, by zapytał "Chcesz polecieć na księżyc?" a następnie zmienił tło, jeśli odpowiesz "tak"?

--- hints ---

--- hint ---

Twój robot powinien `zapytać: „Chcesz polecieć na księżyc?”`{:class="block3sensing"} i `jeżeli`{:class="block3control"} `odpowiedź`{:class="block3sensing"} brzmi „tak”, to powinien `przełączyć tło na księżyc`{:class="block3looks"}.

--- /hint ---

--- hint ---

Oto bloki kodu, które musisz dodać do kodu swojego robota.

![nano duszek](images/nano-sprite.png)

```blocks3
zmień tło na (księżyc v)

zapytaj [Czy chcesz polecieć na księżyc?] i czekaj

jeżeli <(odpowiedź) = [yes]> to 

koniec
```

--- /hint ---

--- hint ---

Tak powinien wyglądać Twój kod:

```blocks3
zapytaj [Czy chcesz polecieć na księżyc?] i czekaj
jeżeli <(odpowiedź) = [yes]> to 
  zmień tło na (księżyc v)
koniec
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Teraz musisz się upewnić, że robot gaduła znajduje się w odpowiednim miejscu, gdy na niego klikniesz, żeby z nim porozmawiać. Dodaj ten bloczek na górze swojego kodu robota:

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy ten duszek kliknięty
+ zmień tło na (kosmos v)
```

--- /task ---

--- task ---

Przetestuj swój program i odpowiedz „tak”, gdy robot zapyta, czy chcesz udać się na księżyc. Powinieneś zobaczyć, że położenie robota się zmienia.

--- /task ---

--- task ---

Możesz również dodać następujący kod do nowego bloku `jeżeli`{:class="block3control"}, żeby robot gaduła podskoczył cztery razy, jeśli odpowiesz „tak”:

![nano duszek](images/nano-sprite.png)

```blocks3
jeżeli <(odpowiedź) = [yes]> to 
  zmień tło na (księżyc v)
+ powtarzaj (4) 
    zmień y o (10)
    czekaj (0.1) sekund
    zmień y o (-10)
    czekaj (0.1) sekund
  koniec
koniec
```

--- /task ---