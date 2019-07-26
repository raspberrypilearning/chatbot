## 말하는 로봇

챗봇의 성격을 정했으니, 챗봇이 당신에게 말할 수 있도록 프로그램을 만들어 봅시다.

\--- task \---

챗봇 스프라이트를 클릭한 경우 다음과 같은 코드가 실행되도록 하세요. `챗봇 스프라이트를 클릭했을 때`{:class="block3events"} `이름을 묻고`{:class="block3sensing"} ` "정말 예쁜 이름이구나!" 를 말하게 하세요. `{:class="block3looks"}.

![나노 스프라이트](images/nano-sprite.png)

```blocks3
이 스프라이트를 클릭했을 때
[너 이름이 뭐니?] 라고 묻고 기다리기
[정말 예쁜 이름이구나!] 을(를) (2) 초 동안 말하기
```

\--- /task \---

\--- task \---

코드를 테스트하려면 챗봇을 클릭하십시오. 대화방에서 이름을 묻는 메시지가 표시되면 스테이지 하단에있는 상자에 입력 한 다음 파란색 아이콘을 클릭하거나 <kbd>Enter</kbd>를 클릭합니다.

![ChatBot 응답 테스트](images/chatbot-ask-test1.png)

![ChatBot 응답 테스트](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

지금, 여러분의 챗봇은 "정말 예쁜 이름이구나!" 라고만 대답합니다. 챗봇의 답변을 개인화하여 다른 이름을 입력하면 답변이 달라지도록 설계할 수 있나요?

챗봇의 스프라이트 코드에 `결합하기`{:class="block3operators"}를 사용하여, `답변`{:class="block3sensing"} 에 사용자 이름을 추가하세요. 아래와 같이 프로그래밍할 수 있습니다:

![나노 스프라이트](images/nano-sprite.png)

```blocks3
이 스프라이트를 클릭했을 때
[너 이름이 뭐니?] 라고 묻고 기다리기
[결합하기[Hi ] (답변) :: +] 을(를) (2) 초 동안 말하기
```

![개별화된 답변 테스트](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

**변수**에 응답을 저장함으로써 프로젝트 어디에서든 사용할 수 있습니다.

`name`{:class="block3variables"}이라는 이름의 새 변수를 추가 해 보세요.

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

이제, 챗봇의 스프라이트 코드를 변경하여 `이름`{:class="block3variables"} 변수를 `답변`{:class="block3sensing"}에 저장할 수 있도록 하세요:

![나노 스프라이트](images/nano-sprite.png)

```blocks3
이 스프라이트를 클릭했을 때
[너 이름이 뭐니?] 라고 묻고 기다리기

+ [이름 v]을(를) (답변)로 정하기
 (결합하기 [안녕 ] (name :: variables +)) 을(를) (2) 초 동안 말하기
```

코드는 이전과 같이 작동해야 합니다: 당신의 챗봇은 당신의 이름을 사용해서 인사해야 합니다.

![개별화된 답변 테스트](images/chatbot-answer-test.png)

\--- /task \---

프로젝트를 다시 테스트해 보세요. 입력 한 응답은 `이름` {:class="block3variables"} 변수에 저장되며 스테이지의 왼쪽 상단 모서리에도 표시됩니다. 스테이지에서 사라지게하려면 ` 데이터` {: class = "block3variables"} 로 이동하여, 섹션을 차단하고 ` 이름  ` {: class = "block3variables"}옆의 상자를 클릭하세요.