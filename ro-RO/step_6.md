## Schimbarea poziției

Poți programa chatbot-ul să-și schimbe pozitia.

\--- task \---

Adăugați un alt fundal în scenă, de exemplu fundalul "lună".

![Adăugarea unui fundal ‘lună’](images/chatbot-moon.png)

\--- /task \---

\--- task \---

Poți programa chatbot-ul să intrebe “Vrei să mergi pe lună?” și să își schimbe pozitia dacă răspunsul este”da”?

Testează și salvează. Dacă răspunsul este”da”, chatbot-ul schimbă poziția. Acum chatbot-ul ar trebui să arate supărat și să zică “OK..pa!” dacă e orice alt răspuns.

![Testeaza un fundal care se schimbă](images/chatbot-backdrop-test.png)

\--- hints \--- \--- hint \--- Chatbot-ul **cere** "Vrei să mergi pe lună?”. **If** **answer** este "da", atunci chatbot-ul schimbă deghizarea cu**change costume** cea vesela iar fundalul de scenă **backdrop** ar trebui să se schimbe.

Dacă răspunsul e "nu", atunci chatbot-ul **change costume** și va arăta supărat și va **say** "OK...pa!"

Va trebui să adăugați un cod astfel chatbot-ul pornește din locul potrivit **when clicked**. \--- /hint \--- \--- hint \--- Acestea sunt blocurile de comenzi necesare: ![Blocks for changing the backdrop](images/chatbot-backdrop-blocks.png) \--- /hint \--- \--- hint \--- Asa ar trebui sa arate: ![Code for changing the backdrop](images/chatbot-backdrop-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Poți adăuga un cod astfel încât chatbot-ul să sară de bucurie dacă vrei să mergi pe lună?

Testează și salvează. Dacă răspunsul este ”da”, chatbotul sare de bucurie. Dacă alt răspuns este dat chatbot-ul nu ar trebui să sară.

![Testează un ChatBot săritor](images/chatbot-jump-test.png)

\--- hints \--- \--- hint \--- Chatbot-ul sare **changing** **y position** cu mici incremente, revenind la poziția inițială dupa un timp de **wait**. Va trebui să **repeat** asta de mai multe ori. \--- /hint \--- \--- hint \--- Acestea sunt blocurile de comenzi necesare: ![Blocks for a jumping ChatBot](images/chatbot-jump-blocks.png) \--- /hint \--- \--- hint \--- Asa ar trebui sa arate: ![Code for a jumping ChatBot](images/chatbot-jump-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---