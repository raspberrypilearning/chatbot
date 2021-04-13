## ನಿರ್ಧಾರಗಳನ್ನು ತೆಗೆದುಕೊಳ್ಳುವುದು

ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ ಸ್ವೀಕರಿಸುವ ಉತ್ತರಗಳ ಆಧಾರದ ಮೇಲೆ ಏನು ಮಾಡಬೇಕೆಂದು ನಿರ್ಧರಿಸಲು ನೀವು ಅದನ್ನು ಪ್ರೋಗ್ರಾಂ ಮಾಡಬಹುದು.

ಮೊದಲಿಗೆ, ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ ಅನ್ನು "ಹೌದು" ಅಥವಾ "ಇಲ್ಲ" ಎಂದು ಉತ್ತರಿಸಬಹುದಾದ ಪ್ರಶ್ನೆಯನ್ನು ಕೇಳುವಂತೆ ಮಾಡಲಿದ್ದೀರಿ.

\--- task \---

ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ಕೋಡ್ ಬದಲಾಯಿಸಿ. ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ `name`{:class="block3variables"} ವೇರಿಯಬಲ್ ಬಳಸಿಕೊಂಡು "Are you OK name" ಎಂಬ ಪ್ರಶ್ನೆಯನ್ನು ಕೇಳಬೇಕು. ನಂತರ ಅದು ಪಡೆಯುವ ಉತ್ತರ "ಹೌದು"`ಎಂದಾದರೆ`{:class="block3control"} "ಬಹಳ ಸಂತೋಷ!" ಎಂಬ ಪ್ರತಿಕ್ರಿಯೆಯನ್ನು ನೀಡಬಹುದು, ಉತ್ತರ "ಇಲ್ಲ" ಎಂದಾದರೆ ಏನನ್ನೂ ಹೇಳದಿರಬಹುದು.

![ಚಾಟ್‌ಬಾಟ್ ಉತ್ತರವನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-if-test1-annotated.png)

![ಚಾಟ್‌ಬಾಟ್ ಉತ್ತರವನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-if-test2.png)

![ನ್ಯಾನೋ ಸ್ಪ್ರೈಟ್](images/nano-sprite.png)

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

ನಿಮ್ಮ ಹೊಸ ಕೋಡ್ ಅನ್ನು ಸರಿಯಾಗಿ ಪರೀಕ್ಷಿಸಲು, ನೀವು ಅದನ್ನು **ಎರಡು ಬಾರಿ** ಪರೀಕ್ಷಿಸಬೇಕು: ಒಮ್ಮೆ "ಹೌದು" ಎಂಬ ಉತ್ತರದೊಂದಿಗೆ, ಮತ್ತು ಒಮ್ಮೆ "ಇಲ್ಲ" ಎಂಬ ಉತ್ತರದೊಂದಿಗೆ.

\--- /task \---

ಈ ಸಮಯದಲ್ಲಿ, ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ "ಇಲ್ಲ" ಎಂಬ ಉತ್ತರಕ್ಕೆ ಏನನ್ನೂ ಹೇಳುವುದಿಲ್ಲ.

\--- task \---

"Are you OK name" ಎಂಬ ಪ್ರಶ್ನೆಗೆ ಉತ್ತರ "ಇಲ್ಲ" ಎಂದಿದ್ದಲ್ಲಿ ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ಕೋಡ್ ಅನ್ನು "ಓಹ್ ಇಲ್ಲ!" ಎಂದು ಉತ್ತರಿಸುವಂತೆ ಬದಲಾಯಿಸಿ.

ಚಾಟ್‌ಬಾಟ್ `"ಓಹ್ ಇಲ್ಲ!"` {:class = "block3looks"} ಎಂದು ಉತ್ತರಿಸಲು `if, then`{:class="block3control"}` ಬ್ಲಾಕನ್ನು <0>if, then, else`{:class="block3control"} ಬ್ಲಾಕ್ನಿಂದ ಬದಲಾಯಿಸಿ, ಮತ್ತು ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ.

![ನ್ಯಾನೋ ಸ್ಪ್ರೈಟ್](images/nano-sprite.png)

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

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಿ. ನೀವು "ಇಲ್ಲ" ಎಂದು ಉತ್ತರಿಸುವಾಗ ಮತ್ತು "ಹೌದು" ಎಂದು ಉತ್ತರಿಸುವಾಗ ನೀವು ವಿಭಿನ್ನ ಪ್ರತಿಕ್ರಿಯೆಯನ್ನು ಪಡೆಯಬೇಕು: ನೀವು "ಹೌದು" (ಅದು ಕೇಸ್ ಸೆನ್ಸಿಟಿವ್ ಆಗಿರುವುದಿಲ್ಲ) ಎಂದು ಉತ್ತರಿಸಿದಾಗ ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ "That’s great to hear!", ಮತ್ತು ನೀವು ** ಬೇರೆ ಯಾವುದೇ ಉತ್ತರ ನೀಡಿದಾಗ ** "Oh no!" ಎಂದು ಪ್ರತಿಕ್ರಿಯೆ ನೀಡುತ್ತದೆ.

![ಚಾಟ್‌ಬಾಟ್ ಉತ್ತರವನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-if-test2.png)

![ಹೌದು / ಇಲ್ಲ ಉತ್ತರವನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-if-else-test.png)

\--- /task \---

ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ ಮಾತನಾಡಲು ಕೋಡ್ ಮಾತ್ರವಲ್ಲದೆ, ನೀವು ಯಾವುದೇ ಕೋಡ್ ಅನ್ನು `if, then, else`{:class="block3control"} ಬ್ಲಾಕ್ನಲ್ಲಿ ಹಾಕಬಹುದು.

ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ** ವೇಷಭೂಷಣಗಳು** ಎಂಬ ಟ್ಯಾಬನ್ನು ನೀವು ಕ್ಲಿಕ್ ಮಾಡಿದರೆ, ಒಂದಕ್ಕಿಂತ ಹೆಚ್ಚು ವೇಷಭೂಷಣಗಳಿರುವುದನ್ನು ಎಂದು ನೀವು ನೋಡುತ್ತೀರಿ.

![ಚಾಟ್‌ಬಾಟ್ ವೇಷಭೂಷಣಗಳು](images/chatbot-costume-view-annotated.png)

\--- task \---

ನಿಮ್ಮ ಉತ್ತರವನ್ನು ಟೈಪ್ ಮಾಡಿದಾಗ ಚಾಟ್‌ಬಾಟ್ ವೇಷಭೂಷಣಗಳನ್ನು ಬದಲಾಯಿಸುವಂತೆ ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಿ.

![ಬದಲಾಗುತ್ತಿರುವ ಉಡುಪನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-costume-test1.png)

![ಬದಲಾಗುತ್ತಿರುವ ಉಡುಪನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-costume-test2.png)

`ವೇಷಭೂಷಣ ಬದಲಿ` {:class = "block3looks"} ಮಾಡಲು `if, then, else`{:class="block3control"} ಒಳಗೆ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಿ.

![ನ್ಯಾನೋ ಸ್ಪ್ರೈಟ್](images/nano-sprite.png)

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

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಿ ಮತ್ತು ಉಳಿಸಿ. ನಿಮ್ಮ ಉತ್ತರವನ್ನು ಅವಲಂಬಿಸಿ ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ಮುಖ ಬದಲಾವಣೆಯನ್ನು ನೀವು ನೋಡಬೇಕು.

\--- /task \---

ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ವೇಷಭೂಷಣ ಬದಲಾದ ನಂತರ, ಅದು ಹಾಗೇ ಇರುತ್ತದೆ ಮತ್ತು ಆರಂಭದಲ್ಲಿ ಇದ್ದದ್ದಕ್ಕೆ ಬದಲಾಗುವುದಿಲ್ಲ ಎಂದು ನೀವು ಗಮನಿಸಿದ್ದೀರಾ?

ನೀವು ಇದನ್ನು ಪ್ರಯತ್ನಿಸಬಹುದು: ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಚಲಾಯಿಸಿ ಮತ್ತು "ಇಲ್ಲ" ಎಂದು ಉತ್ತರಿಸಿ ಇದರಿಂದ ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್‌ನ ಮುಖವು ಅತೃಪ್ತಿಕರ ನೋಟಕ್ಕೆ ಬದಲಾಗುತ್ತದೆ. ನಂತರ ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಮತ್ತೆ ಚಲಾಯಿಸಿ ಮತ್ತು ನಿಮ್ಮ ಹೆಸರನ್ನು ಕೇಳುವ ಮೊದಲು ನಿಮ್ಮ ಚಾಟ್‌ಬಾಟ್ ಸಂತೋಷವಾಗಿ ಕಾಣುವಂತೆ ಬದಲಾಗುವುದಿಲ್ಲ ಎಂಬುದನ್ನು ಗಮನಿಸಿ.

![ವೇಷಭೂಷಣ ದೋಷ](images/chatbot-costume-bug-test.png)

\--- task \---

ಈ ಸಮಸ್ಯೆಯನ್ನು ಪರಿಹರಿಸಲು, ಚಾಟ್‌ಬಾಟ್‌ನ `when the sprite is clicked`{:class="block3events"}ನ ಪ್ರಾರಂಭದಲ್ಲಿ `switch costume`{:class="block3looks"} ಕೋಡ್ ಸೇರಿಸಿ.

![ನ್ಯಾನೋ ಸ್ಪ್ರೈಟ್](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch costume to (nano-a v)
ask [What's your name?] and wait
```

![ವೇಷಭೂಷಣ ಫಿಕ್ಸ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಲಾಗುತ್ತಿದೆ](images/chatbot-costume-fix-test.png)

\--- /task \---