## Αλλάζοντας τοποθεσία

Μπορείς επίσης να προγραμματίσεις το chatbot να αλλάζει τοποθεσία!

![Δοκιμάζοντας ένα μεταβαλλόμενο υπόβαθρο](images/chatbot-backdrop-moon.png)

\--- task \---

Μπορείς να προγραμματίσεις το chatbot να ρωτά "Θα ήθελες να πας στο φεγγάρι;" και στη συνέχεια να αλλάζει τοποθεσία αν απαντήσεις "ναι";

\--- hints \---

\--- hint \---

Το chatbot σου πρέπει να `ρωτήσει "Θέλεις να πας στο διάστημα;"`{:class="block3sensing"} και `εάν`{:class="block3control"} `απαντήσεις`{:class="block3sensing"} "ναι", θα πρέπει `να αλλάξει το σκηνικό στο διάστημα`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Ακολουθούν τα μπλοκ κώδικα που πρέπει να προσθέσεις στον κώδικα του chatbot.

![nano sprite](images/nano-sprite.png)

```blocks3
switch backdrop to (Galaxy v)

ask [Do you want to go to the Galaxy?] and wait

if <(answer) = [yes]> then 

end
```

\--- /hint \---

\--- hint \---

Έτσι πρέπει να μοιάζει ο κώδικας σου:

```blocks3
ask [Do you want to go to the Galaxy?] and wait
if <(answer) = [yes]> then 
  switch backdrop to (Galaxy v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Τώρα χρειάζεται να βεβαιωθείς ότι το chatbot σου ξεκινά στη σωστή τοποθεσία όταν κάνεις κλικ σε αυτό για να του μιλήσεις. Πρόσθεσε αυτό το μπλοκ στην αρχή του κώδικα του chatbot:

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

Δοκίμασε το πρόγραμμά σου και απάντησε "ναι" όταν το chatbot σου ρωτήσει εάν θέλεις να πας στο φεγγάρι. Θα δεις ότι η τοποθεσία του chatbot αλλάζει.

\--- /task \---

\--- task \---

Μπορείς επίσης να προσθέσεις τον ακόλουθο κώδικα στο νέο μπλοκ `εάν`{:class="block3control"} για να κάνεις το chatbot να χοροπηδήξει τέσσερις φορές αν απαντήσεις "ναι":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> then 
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