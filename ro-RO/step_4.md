## Un chatbot vorbitor

Acum, dacă aveți un chatbot cu personalitate, haideți să-l programăm să vorbească.

\--- task \---

Adaugă un cod, chatbot-ului tău, ca atunci când e apăsat, să te întrebe numele și să-ți răspundă cu “Ce nume drăguț!”

![Testează răspunsul ChatBot-ului](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- Când chatbot-ul **sprite is clicked**, el va **cere**numele tău. Atunci chatbot-ul va răspunde **say** "Ce nume drăguț!" \--- /hint \--- \--- hint \--- Acesta e codul de blocuri, de care ai nevoie: ![Blocks for a ChatBot reply](images/chatbot-ask-blocks.png) \--- /hint \--- \--- hint \--- Așa ar trebui să arate: ![Code for a ChatBot reply](images/chatbot-ask-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Acum chatbot-ul răspunde de fiecare dată cu “Ce nume drăguț!” Poți să personalizezi chatbot-ul astfel încât să folosească răspunsul tău?

![Testează un răspuns personalizat](images/chatbot-answer-test.png)

\--- hints \--- \--- hint \--- Atunci când chatbot **sprite is clicked**, el **cere** numele tău. Chatbot-ul răspunde cu **say** “Bună", utmat de **answer** tău. \--- /hint \--- \--- hint \--- Acestea sunt blocurile de comenzi necesare: ![Blocks for a personalised reply](images/chatbot-answer-blocks.png) \--- /hint \--- \--- hint \--- Asa ar trebui sa arate: ![Code for a personalised reply](images/chatbot-answer-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Dacă stochezi răspunsul tau într-o **variable**, atunci acesta poate fi folosit mai târziu. Creează o nouă variabilă numită `name` pentru a memora numele tău.

[[[generic-scratch-add-variable]]]

\--- /task \---

\--- task \---

Poți salva răspunsul în variabila `name` pentru a-l folosi atunci când chatbot-ul răspunde?

Codul tău ar trebui să funcționeze ca înainte: chatbot-ul tău ar trebui să salute folosind numele tău.

![Testeaza o variabilă ‘name’](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- Atunci când chatbot-ul **sprite is clicked**, el **cere** numele tău. Atunci ar trebui **set** `name` variabilei **answer** tale. Atunci chatbot-ul va raspunde **say** "Bună", urmat de **name**. \--- /hint \--- \--- hint \--- Acestea sunt blocurile de comenzi necesare: ![Blocks for a 'name' variable](images/chatbot-variable-blocks.png) \--- /hint \--- \--- hint \--- Asa ar trebui sa arate: ![Code for a 'name' variable](images/chatbot-variable-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Provocarea: alte întrebări

Programați-vă chatbot-ul pentru a pune o altă întrebare. Puteți stoca răspunsul într-o nouă variabilă?

![Alte întrebări](images/chatbot-question.png) \--- /challenge \---