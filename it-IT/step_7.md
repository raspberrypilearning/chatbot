## Cambiare posizione

Puoi anche programmare il tuo ChiacchieRobot a cambiare la sua posizione!

![Testare un cambio di sfondo](images/chatbot-backdrop-moon.png)

\--- task \---

Puoi programmare il tuo chatbot per chiedere "Vuoi andare sulla luna", e quindi cambiare lo sfondo quando la risposta è "sì"?

\--- hint \---

\--- hint \---

Il tuo chatbot dovrebbe `chiedere "Vuoi andare alla luna?"`{:class="block3sensitive"}, e `se`{:class="block3control"} tu `rispondi`{:class="block3sensitive"} "sì", dovrebbe `cambiare lo sfondo`{:class="block3look"}.

\--- /hint \---

\--- hint \---

Ecco i blocchi di codice che devi aggiungere al tuo codice chiacchierobot.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [Vuoi andare sulla luna?] and wait

if <(answer) = [si]> then 

end
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il risultato:

```blocks3
ask [Vuoi andare sulla luna?] and wait
if <(answer) = [si]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ora devi assicurarti che il tuo chatbot si avvii nella posizione giusta quando fai clic su di esso per parlarci. Aggiungi questo blocco all'inizio del tuo codice:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Metti alla prova il tuo programma e rispondi "sì" quando il chatbot ti chiede se vuoi andare sulla luna. Dovresti vedere che lo sfondo cambia.

\--- /task \---

\--- task \---

Puoi anche aggiungere il seguente codice all'interno del nuovo blocco `se`{:class="block3control"} per far saltare il chatbot quattro volte se rispondi "sì":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [si]> then 
  switch backdrop to (moon v)

+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

\--- /task \---