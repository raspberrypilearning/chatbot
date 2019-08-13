## Promjena lokacije

Možeš programirati svog chatbota da mijenja lokaciju!

![Ispitivanje promjene pozadine](images/chatbot-backdrop-moon.png)

\--- task \---

Možeš li programirati svog chatbota da pita „Želiš li ići na Mjesec?“, a zatim promijeni pozadinu kad je odgovor „da“?

\--- hints \---

\--- hint \---

Chatbot bi trebao `pitati „Želiš li ići na Mjesec?“`{:class="block3sensing"} - `ako`{:class="block3control"} je `odgovor`{:class="block3sensing"} „da“, neka `promijeni pozadinu na Mjesec`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Trebat ćeš ove blokove kôda:

![nano lik](images/nano-sprite.png)

```blocks3
promijeni pozadinu na (Mjesec v)

pitaj [Želiš li ići na Mjesec?] i čekaj

ako <(odgovor) = [da]> onda

end

```

\--- /hint \---

\--- hint \---

Ovako bi tvoj kôd trebao izgledati:

```blocks3
pitaj [Želiš li ići na Mjesec?] i čekaj
ako <(odgovor) = [da]> onda 
  promijeni pozadinu na (Mjesec v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Sada se moraš pobrinuti da tvoj chatbot kreće sa odgovarajuće lokacije kada klikneš na njega. Dodaj ovaj blok na početak svog kôda: 

![nano lik](images/nano-sprite.png)

```blocks3
Kada je lik kliknut

+ promijeni pozadinu na (svemir v)
```

\--- /task \---

\--- task \---

Testiraj program i odgovori sa „da“ kada te chatbot pita želiš li ići na Mjesec. Chatbotova lokacija trebala bi se promijeniti.

\--- /task \---

\--- task \---

Možeš dodati i sljedeći kôd unutar novog `ako`{:class="block3control"} bloka kako bi chatbot skočio četiri puta ako odgovoriš sa „da“:

![nano lik](images/nano-sprite.png)

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