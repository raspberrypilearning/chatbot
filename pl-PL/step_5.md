## Podejmowanie decyzji

Możesz zaprogramować swojego robota gadułę tak, aby decydował, co robić na podstawie otrzymanych odpowiedzi.

Najpierw zachęć swojego robota do zadawania pytania, na które można odpowiedzieć „tak” lub „nie”.

--- task ---

Zmień kod swojego robota. Twój robot gaduła powinien zadać pytanie „Czy wszystko w porządku imię”, używając zmiennej `imię`{:class="block3variables"}. Następnie powinien odpowiedzieć „To świetnie!” `jeśli`{:class="block3control"} odpowiedź, którą otrzymał brzmi „tak”, powinien milczeć, jeśli odpowiedź brzmi „nie”.

![Sprawdzanie odpowiedzi robota](images/chatbot-if-test1-annotated.png)

![Testowanie odpowiedzi robota](images/chatbot-if-test2.png)

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy duszek został kliknięty
zapytaj [Jak masz na imię?] i poczekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekundy
+zapytaj (połącz [Czy wszystko OK ] (imię)) i poczekaj
+jeżeli <(odpowiedź) = [tak]> to 
  powiedz [To świetnie!] przez (2) sekundy
koniec
```

Aby dokładnie przetestować swój program, musisz sprawdzić go **dwa razy** - raz wpisując odpowiedź "tak "i drugi raz wpisując "nie".

--- /task ---

Teraz Twój robot nic nie mówi na odpowiedź „nie”.

--- task ---

Zmień kod robota, aby odpowiadał „O nie!” jeśli otrzyma „nie” jako odpowiedź na pytanie„Czy wszystko w porządku imię”.

Zastąp blok `jeżeli...to`{:class="block3control"} na blok `jeżeli...to, w przeciwnym razie`{:class="block3control"} i dołącz kod, aby robot gaduła mógł powiedzieć `"O nie!"`{:class="block3looks"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy duszek został kliknięty
zapytaj [Jak masz na imię?] i poczekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekundy
zapytaj (połącz [Czy wszystko OK ] (imię)) i poczekaj

+ jeżeli <(odpowiedź) = [tak]> to 
  powiedz [To świetnie!] przez (2) sekundy
w przeciwnym razie
+ powiedz [O nie!] przez (2) sekundy
koniec
```

--- /task ---

--- task ---

Przetestuj swój kod. Powinno się otrzymać inną odpowiedź na „nie” i „tak”: Twój robot powinien odpowiedzieć „To świetnie!” kiedy odpowiesz „tak” (wielkość liter nie ma znaczenia) i odpowiedzieć „O nie!”, kiedy odpowiesz **cokolwiek innego**.

![Testowanie odpowiedzi robota](images/chatbot-if-test2.png)

![Testowanie odpowiedzi "tak / nie"](images/chatbot-if-else-test.png)

--- /task ---

Możesz wstawić dowolny kod do bloku `jeżeli...to, w przeciwnym razie`{:class="block3control"}, a nie tylko polecenie, aby Twój robot mówił!

Jeśli klikniesz zakładkę **Kostium** swojego robota, zobaczysz że jest więcej niż jedno przebranie.

![kostium robota](images/chatbot-costume-view-annotated.png)

--- task ---

Zmień kod robota tak, aby zmieniał kostiumy kiedy wpiszesz odpowiedź.

![Testowanie zmieniającego się kostiumu](images/chatbot-costume-test1.png)

![Testowanie zmieniającego się kostiumu](images/chatbot-costume-test2.png)

Zmień kod wewnątrz bloku `jeżeli...to, w przeciwnym razie`{:class="block3control"} na `zmień kostium`{:class="block3looks"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy duszek został kliknięty
zapytaj [Jak masz na imię?] i poczekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekundy
zapytaj (połącz [Czy wszystko OK ] (imię)) i poczekaj
jeżeli <(odpowiedź) = [tak]> to 

+ przełącz kostium na (nano-c v)
  powiedz [To świetnie!] przez (2) sekundy
w przeciwnym razie
+ przełącz kostium na (nano-d v)
powiedz [O nie!] przez (2) sekundy
koniec
```

Przetestuj i zapisz swój kod. Zauważ zmianę na twarzy robota w zależności od Twojej odpowiedzi.

--- /task ---

Czy udało Ci się zauważyć, że po zmianie kostiumu robot pozostaje taki sam i nie wraca już do tego, jaki był na początku?

Przetestuj: uruchom swój kod i odpowiedz „nie”, aby twarz robota zmieniła się w nieszczęśliwe spojrzenie. Następnie uruchom ponownie kod i zauważ, że Twój robot nie zmienia się z powrotem w wyglądającego na szczęśliwego, zanim nie zapyta o Twoje imię.

![Błąd w zmianie kostiumu](images/chatbot-costume-bug-test.png)

--- task ---

Aby rozwiązać ten problem, dodaj kod robota do bloku `zmień kostium`{:class="block3looks"} na początku bloku `kiedy ten został duszek kliknięty`{:class="block3events"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy duszek został kliknięty

+ przełącz kostium na (nano-a v)
zapytaj [Jak masz na imię?] i poczekaj
```

![Testowanie poprawki kostiumu](images/chatbot-costume-fix-test.png)

--- /task ---