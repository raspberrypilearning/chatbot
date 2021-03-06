## 장소 바꾸기

챗봇이 장소를 바꾸도록 코드를 만들 수 있습니다!

![변화하는 배경 테스트](images/chatbot-backdrop-moon.png)

--- task ---

"달에 가보고 싶니?" 라는 챗봇의 물음에 "응"이라고 대답하면 장소가 바뀌도록 코드를 만들 수 있습니까?

--- hints ---

--- hint ---

챗봇이 `"달에 가보고 싶니?"`{:class="block3sensing"}라고 물어봐야 합니다. `만약`{:class="block3control"} 사용자의 `대답`{:class="block3sensing"} 이 "예" 인 경우, `배경을 moon으로 바꾸기`{:class="block3looks"}가 실행되도록 해야 합니다.

--- /hint ---

--- hint ---

다음은 챗봇 코드에 추가해야하는 코드 블록입니다.

![나노 스프라이트](images/nano-sprite.png)

```blocks3
배경을 (moon v) \(으\)로 바꾸기

[달에 가보고 싶니?] 라고 묻고 기다리기

만약 <(대답) = [yes]> \(이\)라면
end
```

--- /hint ---

--- hint ---

다음과 같은 코드를 추가해야 합니다:

```blocks3
[달에 가보고 싶니?] 라고 묻고 기다리기
만약 <(대답) = [yes]> \(이\)라면 
  배경을 (moon v) \(으\)로 바꾸기
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

이제 챗봇을 클릭하면 챗봇이 올바른 위치에서 시작되는지 확인해야합니다. 다음 블록을 챗봇 코드 상단에 추가하십시오:

![나노 스프라이트](images/nano-sprite.png)

```blocks3
이 스프라이트를 클릭했을 때
+ 배경을 (space v) \(으\)로 바꾸기
```

--- /task ---

--- task ---

챗봇이 달에 가고 싶냐고 묻는다면 "예"라고 대답하십시오. 챗봇이 있는 위치가 변경된 것을 볼 수 있습니다.

--- /task ---

--- task ---

`만약`{:class="block3control"} 코드 안에 새로운 동작을 추가할 수도 있습니다. 챗봇의 물음에 "예"라고 대답하면 챗봇을 4 번 위아래로 점프하도록 할 수 있습니다:

![나노 스프라이트](images/nano-sprite.png)

```blocks3
만약 <(대답) = [yes]> \(이\)라면 
  배경을 (moon v) \(으\)로 바꾸기
+  (4) 번 반복하기 
     y 좌표를 (10) 만큼 바꾸기
     (0.1) 초 기다리기
     y 좌표를 (-10) 만큼 바꾸기
     (0.1) 초 기다리기
    end
end
```

--- /task ---