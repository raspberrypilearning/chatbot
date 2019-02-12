## Thay đổi vị trí

Bạn cũng có thể lập trình chatbot của mình để thay đổi vị trí của nó!

![Thử nghiệm thay đổi phông nền](images/chatbot-backdrop-moon.png)

\--- task \---

Bạn có thể lập trình chatbot của mình để hỏi "Bạn có muốn lên mặt trăng" không, và sau đó thay đổi phông nền khi câu trả lời là "có"?

\--- gợi ý \---

\--- hint \---

Chatbot của bạn nên `hỏi "Bạn có muốn đi lên mặt trăng không?"`{: class = "block3sensing"} và `if`{: class = "block3control"} bạn `câu trả lời`{: class = "block3sensing"} "có", nên chuyển `phông nền sang mặt trăng`{: class = "block3looks"}.

\--- /hint \---

\--- hint \---

Dưới đây là các khối mã bạn cần thêm vào mã chatbot của mình.

![nano sprite](images/nano-sprite.png)

```blocks3
chuyển backdrop sang (moon v)

hỏi [Bạn có muốn lên mặt trăng không?] và đợi

nếu <(trả lời) = [yes]> rồi 

kết thúc
```

\--- /hint \---

\--- hint \---

Đây là mã của bạn sẽ trông như thế nào:

```blocks3
hỏi [Bạn có muốn đi lên mặt trăng không?] và đợi
nếu <(câu trả lời) = [yes]> sau đó chuyển 
  phông nền sang (mặt trăng v)
kết thúc
```

\--- /hint \---

\--- / gợi ý \---

\--- /task \---

\--- task \---

Bây giờ bạn cần đảm bảo rằng chatbot của bạn bắt đầu ở đúng vị trí khi bạn nhấp vào nó để nói chuyện với nó. Thêm khối này vào đầu mã chatbot của bạn:

![nano sprite](images/nano-sprite.png)

```blocks3
khi sprite này nhấp

+ chuyển backdrop sang (dấu cách v)
```

\--- /bài tập \---

\--- task \---

Kiểm tra chương trình của bạn và trả lời "có" khi chatbot hỏi bạn có muốn lên mặt trăng không. Bạn sẽ thấy rằng vị trí của chatbot thay đổi.

\--- /bài tập \---

\--- task \---

Bạn cũng có thể thêm mã sau vào khối `if`{: class = "block3control"} mới để làm cho chatbot nhảy lên xuống bốn lần nếu bạn trả lời "có":

![nano sprite](images/nano-sprite.png)

```blocks3
if <(answer) = [yes]> thì 
  chuyển backdrop thành (moon v)

+ lặp lại (4) 
    thay đổi y bằng (10)
    chờ (0.1) giây
    thay đổi y bằng (-10)
    chờ (0.1) giây
  kết thúc
kết thúc
```

\--- /bài tập \---