## Spreminjanje lokacije

Klepetalni robot lahko programiraš tudi tako, da bo spremenil lokacijo!

![Testiranje spreminjanja ozadja](images/chatbot-backdrop-moon.png)

--- task ---

Ali lahko sprogramiraš svojega klepetalnega robota, da vpraša "Ali želite iti na luno" in se nato zamenja ozadje, če je odgovor "da"?

--- hints ---

--- hint ---

Tvoj klepetalni robot mora `vprašati "Ali želiš iti na luno?"`{:class="block3sensing"}, in `če`{:class="block3control"} je tvoj `odgovor`{:class="block3sensing"} "da", mora `zamenjati ozadje na luno`{:class="block3looks"}.

--- /hint ---

--- hint ---

Tukaj so kodni bloki, ki jih moraš dodati kodi klepetalnega robota.

![nano figura](images/nano-sprite.png)

```blocks3
zamenjaj ozadje na (mesec v)

vprašaj [Ali želiš iti na luno?] in počakaj

če <(odgovor) = [da]> potem

konec
```

--- /hint ---

--- hint ---

Tvoja koda mora izgledati tako:

```blocks3
vprašaj [Ali hočeš iti na luno?] in počakaj
če <(odgovor) = [da]> potem
  zamenjaj ozadje na (moon v)
konec
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Zdaj moraš poskrbeti, da se bo tvoj klepetalni robot na začetku, ko boš kliknil nanj in govoril z njim, pojavil na pravi lokaciji. Dodaj ta blok na vrh kode robota:

![nano figura](images/nano-sprite.png)

```blocks3
ko kliknemo to figuro

+ zamenjaj ozadje na (vesolje v)
```

--- /task ---

--- task ---

Preizkusi program in odgovori "da", ko te robot vpraša, če želiš iti na luno. Videti bi moral, da se lokacija klepeta spremeni.

--- /task ---

--- task ---

Naslednjo kodo lahko dodaš tudi v novi blok `če`:

![nano figura](images/nano-sprite.png)

```blocks3
če <(odgovor) = [da]> potem 
  zamenjaj ozadje na (moon v)
  + ponovi (4) krat 
  +   spremeni y za (10)
  +   počakaj (0.1) sekund
  +   spremeni y za (-10)
  +   počakaj (0.1) sekund
  + end
end
```

--- /task ---