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

To test your new code properly, you should test it **twice**: once with the answer "yes", and once with the answer "no".

\--- /task \---

At the moment, your chatbot doesn't doesn't say anything to the answer "no".

\--- task --

Change your chatbot's code so that it replies "Oh no!" if it receives "no" as the answer to "Are you OK name".

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

\--- task --

Test your code. You should get a different response when you answer "no" and when you answer "yes": your chatbot should reply with "That’s great to hear!" when you answer "yes" (which is not case-sensitive), and reply with "Oh no!" when you answer **anything else**.

![Δοκιμή απάντησης chatbot](images/chatbot-if-test2.png)

![Δοκιμάζοντας μια απάντηση ναι/όχι](images/chatbot-if-else-test.png)

\--- /task \---

You can put any code inside an `if, then, else`{:class="block3control"} block, not just code to make your chatbot speak!

If you click your chatbot's **Costumes** tab, you'll see that there is more than one costume.

![chatbot ενδυμασίες](images/chatbot-costume-view-annotated.png)

\--- task --

Change your chatbot's code so that the chatbot switches costumes when you type in your answer.

![Δοκιμάζοντας μία μεταβαλλόμενη ενδυμασία](images/chatbot-costume-test1.png)

![Δοκιμάζοντας μία μεταβαλλόμενη ενδυμασία](images/chatbot-costume-test2.png)

Change the code inside the `if, then, else`{:class="block3control"} block to `switch costume`{:class="block3looks"}.

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

Test and save your code. You should see your chatbot's face change depending on your answer.

\--- /task \---

Have you noticed that, after your chatbot's costume has changed, it stays like that and doesn't change back to what it was at the beginning?

You can try this out: run your code and answer "no" so that your chatbot's face changes to an unhappy look. Then run your code again and notice that your chatbot does not change back to looking happy before it asks your name.

![Σφάλμα ενδυμασίας](images/chatbot-costume-bug-test.png)

\--- task --

To fix this problem, add to the chatbot's code to `switch costume`{:class="block3looks"} at the start `when the sprite is clicked`{:class="block3events"}.

![nano sprite](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![Δοκιμάζοντας μία λύση στο σφάλμα ενδυμασίας](images/chatbot-costume-fix-test.png)

\--- /task \---