## Bước 3: Ra quyết định

Bạn có thể lập trình chatbot của bạn để quyết định những gì để nói hoặc làm dựa trên câu trả lời của bạn cho các câu hỏi của nó.

\--- bài tập \---

Bạn có thể làm cho chatbot đặt câu hỏi "Bạn có OK không?" Và viết mã để trả lời "Thật tuyệt vời khi nghe!" chỉ **nếu** người dùng trả lời "có"?

Để kiểm tra mã mới của bạn đúng cách, bạn nên kiểm tra nó **hai lần**, một lần với câu trả lời "có" và một lần với câu trả lời "không".

Chatbot của bạn sẽ trả lời "Thật tuyệt vời khi nghe!" nếu bạn trả lời "có", nhưng không nói gì nếu bạn trả lời "không".

![Kiểm tra trả lời của chatbot](images/chatbot-if-test.png)

\--- gợi ý \--- \--- gợi ý \--- Sau khi chatbot của bạn đã nói "Xin chào", bây giờ cũng nên **hỏi** "Bạn có ổn không?". **Nếu** bạn trả lời "có", thì chatbot nên **nói** "Thật tuyệt vời khi nghe!". \--- / hint \--- \--- hint \--- Dưới đây là các khối mã bổ sung bạn sẽ cần: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- / hint \--- \--- hint \--- Dưới đây là cách mã của bạn nên xem xét: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- / gợi ý \--- \--- / gợi ý \---

\--- /bài tập \---

\--- bài tập \---

Tại thời điểm này chatbot của bạn không nói bất cứ điều gì nếu bạn trả lời "không". Bạn có thể thay đổi chatbot của bạn để nó cũng trả lời "Ồ không!" nếu bạn trả lời "không" cho câu hỏi của nó?

Kiểm tra và lưu. Chatbot của bạn bây giờ sẽ nói "Ồ không!" nếu bạn trả lời "không". Trong thực tế, nó sẽ nói "On no!" nếu bạn trả lời với bất cứ điều gì khác hơn là "có" ( **khác** trong một `nếu / else` khối có nghĩa là **nếu không**).

![Kiểm tra trả lời có / không](images/chatbot-if-else-test.png)

\--- gợi ý \--- \--- gợi ý \--- Chatbot của bạn bây giờ nên nói "Thật tuyệt vời khi nghe!" **nếu** câu trả lời của bạn là "có", nhưng phải nói "Ồ không!" nếu bạn trả lời một cái gì đó **khác**. \--- / hint \--- \--- hint \--- Dưới đây là các khối mã bạn sẽ cần phải sử dụng: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- / hint \--- \--- hint \--- Dưới đây là cách mã của bạn nên xem xét: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- / gợi ý \--- \--- / gợi ý \---

\--- /bài tập \---

\--- bài tập \---

Bạn có thể đặt bất kỳ mã nào bên trong khối `if / else` , không chỉ là mã để làm cho chatbot của bạn nói. Nếu bạn nhấp vào tab **Trang phục của** , bạn sẽ thấy rằng nó có nhiều hơn một trang phục.

![trang phục chatbot](images/chatbot-costume-view.png)

\--- /bài tập \---

\--- bài tập \---

Bạn có thể thay đổi trang phục của chatbot để phù hợp với câu trả lời của bạn không?

Kiểm tra và lưu. Bạn sẽ thấy thay đổi khuôn mặt của chatbot tùy thuộc vào câu trả lời của bạn.

![Kiểm tra trang phục đang thay đổi](images/chatbot-costume-test.png)

\--- gợi ý \--- \--- gợi ý \--- chatbot của bạn bây giờ cũng **chuyển trang phục** tùy thuộc vào câu trả lời nhất định. \--- / hint \--- \--- hint \--- Dưới đây là các khối mã bạn sẽ cần phải sử dụng: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- / hint \--- \--- hint \--- Dưới đây là cách mã của bạn nên xem xét: ![Code for a changing costume](images/chatbot-costume-code.png) \--- / gợi ý \--- \--- / gợi ý \---

\--- /bài tập \---

\--- bài tập \---

Bạn có nhận thấy rằng trang phục của chatbot vẫn giữ nguyên như vậy mà nó đã thay đổi đến lần cuối cùng bạn nói chuyện với nó? Bạn có thể khắc phục vấn đề này không?

![Lỗi trang phục](images/chatbot-costume-bug-test.png)

Kiểm tra và lưu: Chạy mã của bạn và nhập "không", để chatbot của bạn trông không vui. Khi bạn chạy lại mã của mình, chatbot của bạn sẽ đổi lại thành một khuôn mặt tươi cười trước khi hỏi tên bạn.

![Thử nghiệm sửa trang phục](images/chatbot-costume-fix-test.png)

\--- gợi ý \--- \--- gợi ý \--- Khi **sprite được nhấp**, chatbot của bạn nên đầu tiên **chuyển trang phục** sang một khuôn mặt tươi cười. \--- / hint \--- \--- hint \--- Đây là khối mã bạn sẽ cần phải thêm: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- / hint \--- \--- hint \--- Dưới đây là cách mã của bạn nên xem xét: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- / gợi ý \--- \--- / gợi ý \---

\--- /bài tập \---

\--- thử thách \---

## Thách thức: quyết định khác

Lập trình chatbot của bạn để đặt một câu hỏi khác - một câu hỏi có câu trả lời "có" hoặc "không". Bạn có thể làm cho chatbot của bạn trả lời câu trả lời không?

![ảnh chụp màn hình](images/chatbot-joke.png) \--- /thử thách \---