## Prendre decisions

Pots programar el teu xat bot per decidir què ha de dir o fer segons les teves respostes que rep.

En primer lloc, faràs que el teu xat bot faci una pregunta que pugui respondre amb "sí" o "no".

\--- task \---

Canvia el codi del teu xat bot. El teu xat bot hauria de fer la pregunta "Estàs bé nom", utilitzant la variable ` nom` {: class = "block3variables"}. Aleshores hauria de respondre "Que bé!". ` si ` {: class = "block3control"} la resposta que rep és "sí", però no dir res si la resposta és "no".

![S'està provant una resposta de xat bot](images / chatbot-if-test1-annotated.png)

![S'està provant una resposta de xat bot](images / chatbot-characters.png)

![nano sprite](images / nano-sprite.png)

```blocks3
quan es fa clic en aquest sprite
pregunta [Quin és el teu nom?] i espera
establir  [nom v] a (resposta)
dir (afegir [hola] (nom)) per (2) segons
+ preguntar (afegir [Estàs bé] (nom)) i esperar
+ si <(resposta) = [si]> llavors
  dir [Qué bé!] per (2) segons
fi
```

Per posar a prova el nou codi correctament, l'hauràs de provar **dues vegades**, una vegada amb la resposta "sí" i una vegada amb la resposta "no".

\--- /task \---

De moment, el vostre xat bot no diu reacciona a la resposta "no".

\--- task \---

Canvia el codi del xat bot perquè respongui "Oh no!" si rep "no" com la resposta a "Estàs bé nom".

Substitueix el bloc ` si, llavors ` {: class = "block3control"} amb un ` si, llavors, sino` {: class = "block3control"} i inclou el codi perquè el xat bot pugui ` dir "Oh no!" ` {: class = "block3looks"}.

![nano sprite](images / nano-sprite.png)

```blocks3
quan es fa clic en aquest sprite
pregunta [Quin és el teu nom?] i espera
establir  [nom v] a (resposta)
dir (afegir [hola] (nom)) per (2) segons
+ preguntar (afegir [Estàs bé] (nom)) i esperar
+ si <(resposta) = [si]> llavors
  dir [Qué bé!] per (2) segons
sino
+dir [Oh no!] per (2) segons
fi
```

\--- /task \---

\--- task \---

Prova el codi nou. Hauríes d'obtenir una resposta diferent quan respons "no" i quan respons "sí": el teu xat bot hauria de respondre amb "Que bé!". quan contestes "sí" (que no distingeix entre majúscules i minúscules), i contestar amb "Oh no!" quan respons ** qualsevol altra cosa **.

![S'està provant una resposta de xat bot](images / chatbot-characters.png)

![S'està provant una resposta si / no](images/chatbot-if-else-test.png)

\--- /task \---

Pots posar qualsevol codi dins d'un bloc de `si / si no`, no només codi, per fer que el teu xat bot parli!

Si fas clic a la pestanya **Disfressa** del xat bot, veuràs que té més d'un conjunt.

![vestits del xat bot](images / chatbot-costume-view-annotated.png)

\--- task \---

Canvia el codi del teu xat bot de manera que canvii de disfressa quan escrius la teva resposta.

![Provant un canvi de vestuari](images / chatbot-characters.png)

![Provant un canvi de vestuari](images / chatbot-characters.png)

Canvieu el codi dins del bloc ` si, llavors, sino` {: class = "block3control"} a ` canvia la disfressa ` {: class = "block3looks"}.

![nano sprite](images / nano-sprite.png)

```blocks3
quan es fa clic en aquest sprite
pregunta [Quin és el teu nom?] i espera
establir  [nom v] a (resposta)
dir (afegir [hola] (nom)) per (2) segons
+ preguntar (afegir [Estàs bé] (nom)) i esperar
+ si <(resposta) = [si]> llavors

+canvia la disfressa a (nano-c v)
  dir [Qué bé!] per (2) segons
sino
+canvia la disfressa a (nano-d v)
+dir [Oh no!] per (2) segons
fi
```

Prova i desa. Hauries de veure com canvia la cara del teu xat bot en funció de la teva resposta.

\--- /task \---

Has notat que, una vegada que la disfressa del xat bot ha canviat, es manté així i no canvia a la disfressa inicial?

Pots provar això: executa el teu codi i respon "no" perquè la cara del xat bot canviï a una aparená infeliç. A continuació, torna a executar el teu codi i observa que el xat bot no canvia de nou per semblar feliç abans de demanar-te el nom.

![Error de vestuari](images/chatbot-costume-bug-test.png)

\--- task \---

Per solucionar aquest problema, afegiu al codi del chatbot ` canviar de disfressa ` {: class = "block3looks"} a l'inici ` quan es fa clic al sprite ` {: class = "block3events"}.

![nano sprite](images / nano-sprite.png)

```blocks3
quan es clica aquest sprite

+ canviar de disfressa a (nano-a v)
preguntar [Quin és el teu nom?] i esperar
```

![Prova d'una solució de vestuari](images/chatbot-costume-fix-test.png)

\--- /task \---