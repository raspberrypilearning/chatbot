## Donošenje odluka

Možeš programirati svog chatbota da sam odluči što će reći ili napraviti ovisno o tome kakav odgovor dobije.

Prvo ćeš programirati svog chatbota da postavi pitanje na koje je moguće odgovoriti sa „da“ ili „ne“.

\--- task \---

Izmijeni kôd svog chatbota. Tvoj chatbot trebao bi postaviti pitanje „Jesi li dobro ime“, koristeći se varijablom `ime`{:class="block3variables"}. Zatim bi trebao odgovoriti „To je sjajno čuti!“ `ako`{:class="block3control"} dobije odgovor „da“, ali ne reći ništa ako je odgovor „ne“.

![Testiranje ChatBot odgovora](images/chatbot-if-test1-annotated.png)

![Testiranje ChatBot odgovora](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
Kada je lik kliknut
pitaj [Kako se zoveš?] i čekaj
postavi [ime v] na (odgovor)
govori (spoji [Bok] (ime)) (2) sekundi
+pitaj (spoji [Jesi li dobro] (ime)) i čekaj
+ako <(odgovor) = [da]> onda 
  govori [To je sjajno čuti!] (2) sekundi
end
```

Provjeri radil li tvoj novi kôd, tako da ga testiraš **dva puta**: jednom s odgovorom „da“ i jednom s odgovorom „ne“.

\--- /task \---

Trenutno tvoj chatbot ništa ne kaže kada je odgovor „ne“.

\--- task \---

Izmijeni kôd tako da chatbot kaže „Oh, ne!“ ako na pitanje „Jesi li dobro ime“ dobije odgovor „ne“.

Zamijeni blok `ako, inače`{:class="block3control"} sa blokom `ako, onda, inače`{:class="block3control"} i ne zaboravi kôd kako bi chatbot mogao `reći „Oh, ne!“`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
Kada je lik kliknut
pitaj [Kako se zoveš?] i čekaj
postavi [ime v] na (odgovor)
govori (spoji [Bok] (ime)) (2) sekundi
pitaj (spoji [Jesi li dobro] (ime)) i čekaj

+ ako <(odgovor) = [yes]> onda 
  govori [To je sjajno čuti!] (2) sekundi
inače 
+  govori [Oh, ne!] (2) sekundi
end
```

\--- /task \---

\--- task \---

Testiraj svoj kôd. Trebaš dobiti drugačiji odgovor kad odgovoriš sa „ne“ i kad odgovoriš sa „da“. Kada je odgovor „da“, chatbot bi trebao reći „To je sjajno čuti!“ (zapamti da chatbot nije osjetljiv na velika i mala slova). Kada je odgovor **bilo što drugo**, chatbot bi trebao reći „Oh, ne!“

![Testiranje ChatBot odgovora](images/chatbot-if-test2.png)

![Ispitivanje da / ne odgovor](images/chatbot-if-else-test.png)

\--- /task \---

Možeš staviti bilo koji kôd unutar bloka `ako, onda, inače`{:class="block3control"}, a ne samo kôd zbog kojeg će tvoj chatbot pričati!

Ako klikeš na svog chatbota, a zatim na karticu **Kostimi**, vidjet ćeš da chatbot ima više od jednog kostima. 

![kostimi za chatbot](images/chatbot-costume-view-annotated.png)

\--- task \---

Promijeni kôd svog chatbota tako da chatbot mijenja kostime kad upišeš svoj odgovor.

![Ispitivanje mijenjanja kostima](images/chatbot-costume-test1.png)

![Ispitivanje mijenjanja kostima](images/chatbot-costume-test2.png)

Promijeni kôd unutar bloka `ako, onda, inače`{:class="block3control"} kako bi chatbot `mijenjao kostime`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
Kada je lik kliknut
pitaj [Kako se zoveš?] i čekaj
postavi [ime v] na (odgovor)
govori (spoji [Bok] (ime)) (2) sekundi
pitaj (spoji [Jesi li dobro] (ime)) i čekaj
ako <(odgovor) = [da]> onda
end

+ promijeni kostim u (nano-c v)
 govori [To je sjajno čuti!] (2) sekundi
inače
+ promijeni kostim u (nano-d v)
 govori [Oh, ne!] (2) sekundi
end
```

Testiraj i spremi svoj kôd. Lice tvog chatbota trebalo bi se mijenjati ovisno o tvom odgovoru.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Kostim bug](images/chatbot-costume-bug-test.png)

\--- task \---

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Ispitivanje popravka kostima](images/chatbot-costume-fix-test.png)

\--- /task \---