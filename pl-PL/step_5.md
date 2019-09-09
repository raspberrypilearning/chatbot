## Podejmowanie decyzji

Możesz zaprogramować swojego robota gadułę tak, aby decydował, co robić na podstawie otrzymanych odpowiedzi.

Najpierw zmusisz swojego robota gadułę do zadania pytania, na które można odpowiedzieć „tak” lub „nie”.

\--- task \---

Zmień kod swojego robota. Twój robot gaduła powinien zadać pytanie „Czy wszystko w porządku imię”, używając zmiennej `imię`{:class="block3variables"}. Następnie powinien odpowiedzieć „To super!” `jeśli`{:class="block3control"} odpowiedź, którą otrzymuje brzmi „tak”, ale nie powinien nic powiedzieć, jeśli odpowiedź brzmi „nie”.

![Testowanie odpowiedzi robota](images/chatbot-if-test1-annotated.png)

![Testowanie odpowiedzi robota](images/chatbot-if-test2.png)

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy ten duszek kliknięty
zapytaj [Jak masz na imię?] i czekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekund
+zapytaj (połącz [Czy wszystko OK ] (imię)) i czekaj
+jeżeli <(odpowiedź) = [tak]> to 
  powiedz [To super!] przez (2) sekund
koniec
```

Aby dokładnie przetestować swój program, musisz sprawdzić go **dwa razy** - raz wpisując odpowiedź "tak "i drugi raz wpisując "nie".

\--- /task \---

W tej chwili twój robot gaduła nic nie mówi na odpowiedź „nie”.

\--- task \---

Zmień kod robota, aby odpowiadał „O nie!” jeśli otrzyma „nie” jako odpowiedź na „Czy wszystko w porządku imię”.

Zastąp blok `jeżeli...to`{:class="block3control"} na blok `jeżeli...to, w przeciwnym razie`{:class="block3control"} i dołącz kod, aby robot gaduła mógł powiedzieć `"O nie!"`{:class="block3looks"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy ten duszek kliknięty
zapytaj [Jak masz na imię?] i czekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekund
zapytaj (połącz [Czy wszystko OK ] (imię)) i czekaj

+ jeżeli <(odpowiedź) = [tak]> to 
  powiedz [To super!] przez (2) sekund
w przeciwnym razie
+ powiedz [O nie!] przez (2) sekund
koniec
```

\--- /task \---

\--- task \---

Przetestuj swój kod. Powinnaś otrzymać inną odpowiedź, gdy odpowiesz „nie” i kiedy odpowiesz „tak”: twój robot gaduła powinien odpowiedzieć „To super!” kiedy odpowiesz „tak” (wielkość liter nie ma znaczenia) i odpowiedz „O nie!” kiedy odpowiesz **cokolwiek innego**.

![Testowanie odpowiedzi robota](images/chatbot-if-test2.png)

![Testowanie odpowiedzi "tak / nie"](images/chatbot-if-else-test.png)

\--- /task \---

Możesz wstawić dowolny kod do bloku `jeżeli...to, w przeciwnym razie`{:class="block3control"}, a nie tylko kod, aby twój robot mówił!

Jeśli klikniesz zakładkę **Kostium** swojego robota gaduły, zobaczysz że jest więcej niż jeden kostium.

![kostiumy robota](images/chatbot-costume-view-annotated.png)

\--- task \---

Zmień kod robota gaduły taj, aby robot zmieniał kostiumy kiedy wpiszesz odpowiedź.

![Testowanie zmieniającego się kostiumu](images/chatbot-costume-test1.png)

![Testowanie zmieniającego się kostiumu](images/chatbot-costume-test2.png)

Zmień kod wewnątrz bloku `jeżeli...to, w przeciwnym razie`{:class="block3control"} na `zmień kostium`{:class="block3looks"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy ten duszek kliknięty
zapytaj [Jak masz na imię?] i czekaj
ustaw [imię v] na (odpowiedź)
powiedz (połącz [Cześć ] (imię)) przez (2) sekund
zapytaj (połącz [Czy wszystko OK ] (imię)) i czekaj
jeżeli <(odpowiedź) = [tak]> to 

+ przełącz kostium na (nano-c v)
  powiedz [To super!] przez (2) sekund
w przeciwnym razie
+ przełącz kostium na (nano-d v)
powiedz [O nie!] przez (2) sekund
koniec
```

Przetestuj i zapisz swój kod. Powinnaś zauważyć zmianę na twarzy robota gaduły w zależności od Twojej odpowiedzi.

\--- /task \---

Czy zauważyłaś, że po zmianie kostiumu robota pozostaje on taki i nie wraca do tego, jaki był na początku?

Możesz spróbować sama: uruchom swój kod i odpowiedz „nie”, aby twarz robota zmieniła się w nieszczęśliwe spojrzenie. Następnie uruchom ponownie kod i zauważ, że Twój robot nie zmienia się z powrotem w wyglądającego na szczęśliwego, zanim nie zapyta o twoje imię.

![Błąd kostiumu](images/chatbot-costume-bug-test.png)

\--- task \---

Aby rozwiązać ten problem, dodaj kod robota do bloku `zmień kostium`{:class="block3looks"} na początku bloku `kiedy ten duszek kliknięty`{:class="block3events"}.

![nano duszek](images/nano-sprite.png)

```blocks3
kiedy ten duszek kliknięty

+ przełącz kostium na (nano-a v)
zapytaj [Jak masz na imię?] i czekaj
```

![Testowanie poprawki kostiumu](images/chatbot-costume-fix-test.png)

\--- /task \---