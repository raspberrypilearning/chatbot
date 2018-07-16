## Đưa ra quyết định

Bạn có thể lập trình chatbot của bạn để quyết định những gì để nói hoặc làm dựa trên câu trả lời của bạn cho các câu hỏi của nó.

\--- task \---

Bạn có thể làm cho chatbot đặt câu hỏi "Bạn có ổn không?" Và viết code để trả lời "Thật tuyệt vời!" **nếu** người dùng trả lời "có"?

Để kiểm tra code mới của bạn hoạt động đúng, bạn nên kiểm tra nó **hai lần**, một lần với câu trả lời "có" và một lần với câu trả lời "không".

Chatbot của bạn sẽ trả lời "Thật tuyệt vời!" nếu bạn trả lời "có", nhưng không nói gì nếu bạn trả lời "không".

![Kiểm tra trả lời của chatbot](images/chatbot-if-test.png)

\--- hints \--- \--- hint \--- Sau khi chatbot của bạn đã nói "Xin chào", bây giờ nó sẽ **hỏi** "Bạn có ổn không?". **Nếu** bạn trả lời "có", thì chatbot nên **nói** "Thật tuyệt vời!". \--- /hint \--- \--- hint \--- Dưới đây là các khối code bổ sung bạn sẽ cần: ![Blocks for a chatbot reply](images/chatbot-if-blocks.png) \--- /hint \--- \--- hint \--- Code của bạn sẽ giống như thế này: ![Code for a chatbot reply](images/chatbot-if-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Tại thời điểm này chatbot của bạn không nói bất cứ điều gì nếu bạn trả lời "không". Bạn có thể thay đổi chatbot của bạn để nó cũng trả lời "Ôi không!" nếu bạn trả lời "không" cho câu hỏi của nó?

Kiểm tra và lưu. Chatbot của bạn bây giờ sẽ nói "Ôi không!" nếu bạn trả lời "không". Trong thực tế, nó sẽ nói "Ôi không!" nếu bạn trả lời với bất cứ điều gì khác hơn là "có" ( **còn không thì** trong một khối `nếu/còn không thì` có nghĩa là **ngược lại**).

![Kiểm tra trả lời có/không](images/chatbot-if-else-test.png)

\--- hints \--- \--- hint \--- Chatbot của bạn bây giờ sẽ nói "Thật tuyệt vời!" **nếu** câu trả lời của bạn là "có", nhưng sẽ nói "Ôi không!" nếu bạn trả lời một cái gì đó **khác**. \--- /hint \--- \--- hint \--- Dưới đây là các khối code bạn sẽ cần phải sử dụng: ![Blocks for a yes/no reply](images/chatbot-if-else-blocks.png) \--- /hint \--- \--- hint \--- Code của bạn sẽ trông giống như thế này: ![Code for a yes/no reply](images/chatbot-if-else-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Bạn có thể đặt bất kỳ code nào bên trong khối `nếu/còn không thì`, không chỉ riêng code để làm cho chatbot của bạn nói. Nếu bạn nhấp vào mục **Hóa trang**, bạn sẽ thấy rằng nó có rất nhiều trang phục.

![trang phục chatbot](images/chatbot-costume-view.png)

\--- /task \---

\--- task \---

Bạn có thể thay đổi trang phục của chatbot để phù hợp với câu trả lời của bạn không?

Kiểm tra và lưu. Bạn sẽ thấy thay đổi khuôn mặt của chatbot tùy thuộc vào câu trả lời của bạn.

![Kiểm tra trang phục thay đổi](images/chatbot-costume-test.png)

\--- hints \--- \--- hint \--- Chatbot của bạn bây giờ cũng **đổi hình dạng** tùy thuộc vào câu trả lời nhất định. \--- /hint \--- \--- hint \--- Dưới đây là các khối code bạn sẽ cần phải sử dụng: ![Blocks for a changing costume](images/chatbot-costume-blocks.png) \--- /hint \--- \--- hint \--- Code của bạn sẽ trông giống như thế này: ![Code for a changing costume](images/chatbot-costume-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Bạn có nhận thấy rằng trang phục của chatbot vẫn giữ nguyên như lần cuối cùng bạn nói chuyện với nó? Bạn có thể khắc phục vấn đề này không?

![Lỗi trang phục](images/chatbot-costume-bug-test.png)

Kiểm tra và lưu: Chạy code của bạn và nhập "không", để chatbot của bạn trông không vui. Khi bạn chạy lại code của mình, chatbot của bạn sẽ đổi lại thành một khuôn mặt tươi cười trước khi hỏi tên bạn.

![Kiểm tra sửa lỗi trang phục](images/chatbot-costume-fix-test.png)

\--- hints \--- \--- hint \--- **Khi đối tượng được nhấp**, chatbot của bạn nên **đổi hình dạng thành** một khuôn mặt tươi cười. \--- /hint \--- \--- hint \--- Đây là khối code bạn sẽ cần phải thêm: ![Blocks for a costume fix](images/chatbot-costume-fix-blocks.png) \--- /hint \--- \--- hint \--- Code của bạn sẽ trông giống như thế này: ![Code for a costume fix](images/chatbot-costume-fix-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## Thử thách: nhiều quyết định hơn

Lập trình chatbot của bạn để đặt một câu hỏi khác - một câu hỏi có câu trả lời "có" hoặc "không". Bạn có thể làm cho chatbot của bạn trả lời câu hỏi không?

![ảnh chụp màn hình](images/chatbot-joke.png) \--- /challenge \---