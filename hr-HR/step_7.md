## Promjena lokacije

Možeš programirati svog chatbota da mijenja lokaciju!

![Testing a changing backdrop](images/chatbot-backdrop-moon.png)

\--- task \---

Možeš li programirati svog chatbota da pita „Želiš li ići na Mjesec?“, a zatim promijeni pozadinu kad je odgovor „da“?

\--- hints \---

\--- hint \---

Chatbot bi trebao `ask „Želiš li ići na Mjesec?“`{:class="block3sensing"} i `if`{:class="block3control"} je `answer`{:class="block3sensing"} „da“, neka `switch the backdrop to the moon`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Trebat ćeš ove blokove kôda:

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Želiš li ići na Mjesec?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

Ovako bi tvoj kôd trebao izgledati:

```blocks3
ask [Želiš li ići na mjesec?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Sada se moraš pobrinuti da tvoj chatbot kreće sa odgovarajuće lokacije kada klikneš na njega. Dodaj ovaj blok na početak svog kôda: 

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Testiraj program i odgovori sa „da“ kada te chatbot pita želiš li ići na Mjesec. Chatbotova lokacija trebala bi se promijeniti.

\--- /task \---

\--- task \---

Možeš dodati i sljedeći kôd unutar novog `if`{:class="block3control"} bloka kako bi chatbot skočio četiri puta ako odgovoriš sa „da“:

![nano sprite](images/nano-sprite.png)

```blocks3
ako <(odgovor) = [da]> onda 
  promijeni pozadinu na (Mjesecv)
  
+  ponovi (4) 
    promijeni y za (10)
    čekaj (0.1) sekundi
    promijeni y za (-10)
    čekaj (0.1) sekundi
  end
end
```

\--- /task \---