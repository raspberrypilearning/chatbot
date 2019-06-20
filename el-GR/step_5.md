## Λαμβάνοντας αποφάσεις

Μπορείς να προγραμματίσεις το chatbot για να αποφασίσει τι να κάνει με βάση τις απαντήσεις που λαμβάνει.

Αρχικά, θα κάνεις το chatbot να ρωτήσει μία ερώτηση που μπορεί να απαντηθεί με "ναι" ή "όχι".

\--- task \---

Άλλαξε τον κώδικα του chatbot. Το chatbot θα πρέπει να ρωτήσει την ερώτηση "Είσαι καλά όνομα", χρησιμοποιώντας τη μεταβλητή `όνομα`{:class="block3variables"}. Μετά θα πρέπει να απαντήσει "Χαίρομαι που το ακούω!" `αν`{:class="block3control"} η απάντηση που λαμβάνει είναι "ναι", αλλά να μην πει τίποτα αν η απάντηση είναι "όχι".

![Δοκιμή απάντησης chatbot](images/chatbot-if-test1-annotated.png)

![Δοκιμή απάντησης chatbot](images/chatbot-if-test2.png)

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
+ask (join [Are you OK ] (name)) and wait
+if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
end
```

Για να δοκιμάσεις κατάλληλα το νέο σου κώδικα, πρέπει να το δοκιμάσεις **δύο φορές**, μία φορά με την απάντηση "ναι" και μία φορά με την απάντηση "όχι".

\--- /task \---

Προς το παρόν, το chatbot σου δεν λέει τίποτα στην απάντηση "όχι".

\--- task \---

Αλλάξτε τον κώδικα του chatbot σου έτσι ώστε να απαντά "Ωχ όχι!" εάν λάβει "όχι" ως απάντηση στην ερώτηση "Είστε OK όνομα".

Replace the `if, then`{:class="block3control"} block with an `if, then, else`{:class="block3control"} block, and include code so the chatbot can `say "Oh no!"`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait

+ if <(answer) = [yes]> then 
  say [That's great to hear!] for (2) seconds
else 
+  say [Oh no!] for (2) seconds
end
```

\--- /task \---

\--- task \---

Δοκίμασε τον κώδικά σοτ Θα λάβεις μία διαφορετική απάντηση όταν απαντάς "όχι" και όταν απαντάς "ναι": το chatbot σου θα απαντάει "Χαίρομαι που το ακούω" όταν απαντάς "ναι" (έχουν σημασία τα μικρά γράμματα) και θα απαντάει "Ωχ όχι!" όταν απαντάς **ο,τιδήποτε άλλο**.

![Δοκιμή απάντησης chatbot](images/chatbot-if-test2.png)

![Δοκιμάζοντας μια απάντηση ναι/όχι](images/chatbot-if-else-test.png)

\--- /task \---

Μπορείς να τοποθετήσεις οποιονδήποτε κώδικα μέσα σε ένα `εάν, τότε αλλιώς`{:class="block3control"} block, όχι μόνο κώδικα για να κάνεις το chatbot να μιλά!

Αν κάνεις κλικ στην καρτέλα **Ενδυμασία** του chatbot, θα δεις ότι έχει περισσότερες από μία ενδυμασίες.

![chatbot ενδυμασίες](images/chatbot-costume-view-annotated.png)

\--- task \---

Άλλαξε τον κώδικα του chatbot σου έτσι ώστε το chatbot να αλλάζει ενδυμασίες όταν πληκτρολογείς την απάντησή σου.

![Δοκιμάζοντας μία μεταβαλλόμενη ενδυμασία](images/chatbot-costume-test1.png)

![Δοκιμάζοντας μία μεταβαλλόμενη ενδυμασία](images/chatbot-costume-test2.png)

Αλλάξτε τον κώδικα μέσα στο `αν, τότε, αλλιώς`{:class="block3control"} μπλοκ σε `αλλαγή ενδυμασίας`{:class="block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [What's your name?] and wait
set [name v] to (answer)
say (join [Hi ] (name)) for (2) seconds
ask (join [Are you OK ] (name)) and wait
if <(answer) = [yes]> then 

+  switch costume to (nano-c v)
  say [That's great to hear!] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [Oh no!] for (2) seconds
end
```

Δοκίμασε και αποθήκευσε τον κώδικά σου. Θα πρέπει να δεις το πρόσωπο του chatbot να αλλάζει ανάλογα με την απάντησή σου.

\--- /task \---

Παρατήρησες ότι μετά την αλλαγή της ενδυμασίας του chatbot, παραμένει έτσι και δεν αλλάζει πίσω σε αυτή που ήταν στην αρχή;

Μπορείς να το δοκιμάσεις: εκτέλεσε τον κωδικό σου και απάντησε "όχι" έτσι ώστε το πρόσωπο του chatbot να αλλάξει σε μια δυστυχισμένη εμφάνιση. Στη συνέχεια, εκτέλεσε τον κωδικά σου και παρατήρησε ότι το chatbot σου δεν αλλάζει ξανά στην χαρούμενη εμφάνιση πριν ζητήσει το όνομά σου.

![Σφάλμα ενδυμασίας](images/chatbot-costume-bug-test.png)

\--- task \---

Για να διορθώσεις αυτό το πρόβλημα, πρόσθεσε στον κώδικα του chatbot το `αλλαγή ενδυμασίας `{:class="block3looks"} στην αρχή `όταν πατηθεί`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Δοκιμάζοντας μία λύση στο σφάλμα ενδυμασίας](images/chatbot-costume-fix-test.png)

\--- /task \---