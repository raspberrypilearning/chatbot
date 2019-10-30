## Robot biết trò chuyện

Bây giờ bạn có một chatbot có cá tính, bạn sẽ lập trình nó để nói chuyện với bạn.

\--- task \---

Nhấp vào spbot chatbot của bạn và thêm mã này vào mã `khi nó nhấp vào`{: class = "block3events"}, nó `hỏi tên của bạn`{: class = "block3sensing"} và sau đó `nói "Thật là một tên đáng yêu! "`{: class = "block3looks"}.

![nano sprite](images/nano-sprite.png)

```blocks3
khi sprite này nhấp
hỏi [Tên của bạn là gì?] và đợi
nói [Thật là một cái tên đáng yêu!] trong (2) giây
```

\--- /bài tập \---

\--- task \---

Nhấp vào chatbot của bạn để kiểm tra mã của bạn. Khi chatbot hỏi tên của bạn, hãy nhập nó vào ô xuất hiện ở cuối Giai đoạn, sau đó bấm vào dấu màu xanh hoặc nhấn <kbd>Enter</kbd>.

![Kiểm tra phản hồi ChatBot](images/chatbot-ask-test1.png)

![Kiểm tra phản hồi ChatBot](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

Ngay bây giờ, chatbot của bạn trả lời "Thật là một cái tên đáng yêu!" mỗi khi bạn trả lời Bạn có thể làm cho câu trả lời của chatbot trở nên cá nhân hơn, để câu trả lời khác nhau mỗi khi nhập tên khác.

Thay đổi mã của chatbot sprite thành `tham gia`{: class = "block3operators"} "Hi" với `câu trả lời`{: class = "block3sensing"} thành "Tên bạn là gì?" câu hỏi, để mã trông như thế này:

![nano sprite](images/nano-sprite.png)

```blocks3
khi sprite này nhấp
hỏi [Tên bạn là gì?] và đợi
nói (tham gia [Hi] (trả lời) :: +) trong (2) giây
```

![Kiểm tra câu trả lời được cá nhân hóa](images/chatbot-answer-test.png)

\--- /bài tập \---

\--- task \---

Bằng cách lưu trữ các câu trả lời trong một **biến**, bạn có thể sử dụng nó bất cứ nơi nào dự án của bạn.

Tạo một biến mới có tên `name`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Bây giờ, hãy thay đổi mã của chatbot của bạn để đặt biến `name`{: class = "block3variables"} thành `câu trả lời`{: class = "block3sensing"}:

![nano sprite](images/nano-sprite.png)

```blocks3
khi sprite này nhấp
hỏi [Tên của bạn là gì?] và đợi

+ đặt [name v] thành (answer)
nói (tham gia [Hi] (name :: biến +)) trong (2) giây
```

Mã của bạn sẽ hoạt động như trước: chatbot của bạn sẽ nói xin chào bằng cách sử dụng tên bạn nhập.

![Kiểm tra câu trả lời được cá nhân hóa](images/chatbot-answer-test.png)

\--- /task \---

Kiểm tra chương trình của bạn một lần nữa. Lưu ý rằng câu trả lời bạn nhập được lưu trữ trong biến `name`{: class = "block3variables"} và cũng được hiển thị ở góc trên cùng bên trái của Giai đoạn. To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.