## Schimbarea locației

Poți, de asemenea, programa robotul tău vorbitor pentru a-și schimba locația!

![Testează un fundal care se schimbă](images/chatbot-backdrop-moon.png)

\--- task \---

Poți programa robotul tău vorbitor pentru a întreba „Vrei să mergi pe lună?”, iar apoi să schimbi decorul când răspunsul este „da”?

\--- hints \---

\--- hint \---

Robotul tău vorbitor ar trebui să `întrebe „Vrei să mergi pe lună?”`{:class="block3sensing"}, iar `dacă`{:class="block3control"} primește ca `răspuns`{:class="block3sensing"} „da”, ar trebui să `schimbe decorul la lună`{:class="block3looks"}.

\--- /hint \---

\--- hint \---

Aici sunt blocurile de cod pe care trebuie să le adaugi la codul robotului tău vorbitor.

![personaj nano](images/nano-sprite.png)

```blocks3
schimbă decorul la (lună v)

întreabă [Vrei să mergi pe lună?] și așteaptă

dacă <(răspuns) = [da]> atunci 

end
```

\--- /hint \---

\--- hint \---

Iată cum ar trebui să arate noul tău cod:

```blocks3
întreabă [Vrei să mergi pe lună?] și așteaptă
dacă <(răspuns) = [da]> atunci 
  schimbă decorul la (lună v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Acum, trebuie să te asiguri că robotul tău vorbitor începe în locația potrivită atunci când dai click pe el pentru a-i vorbi. Adaugă acest bloc în partea de sus a codului pentru robotul tău vorbitor:

![personaj nano](images/nano-sprite.png)

```blocks3
când se dă click pe personaj

+ schimbă decorul la (spațiu v)
```

\--- /task \---

\--- task \---

Testează-ți programul și răspunde cu „da” atunci când robotul tău vorbitor întreabă dacă vrei să mergi pe lună. Ar trebui să vezi că locația robotului vorbitor se schimbă.

\--- /task \---

\--- task \---

Poți, de asemenea, să adaugi următorul cod în interiorul blocului `dacă`{:class="block3control"} pentru a face robotul vorbitor să sară de patru ori dacă răspunzi cu „da”:

![personaj nano](images/nano-sprite.png)

```blocks3
dacă <(răspuns) = [da]> atunci 
  schimbă decorul la (lună v)

+ repetă (4) 
    modifică y cu (10)
    așteaptă (0.1) secunde
    modifică y cu (-10)
    așteaptă (0.1) secunde
  end
end
```

\--- /task \---