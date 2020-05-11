## 場所をかえる

チャットボットのいる場所をかえることができます。

![背景 (はいけい) をかえる](images/chatbot-backdrop-moon.png)

--- task ---

チャットボットが「月に行きたい？」と聞いた後、答えが「はい」の時に背景 (はいけい) をかえることができますか？

--- hints ---

--- hint ---

チャットボットが`「月に行きたい？」と聞いて`{:class="block3sensing"}、`もし`{:class="block3control"}あなたの`答え`{:class="block3sensing"}が「はい」ならば、`背景を月にする`{:class="block3looks"}ようにします。

--- /hint ---

--- hint ---

こちらがチャットボットのコードに追加するコードブロックです。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [月に行きたい？] and wait

if <(answer) = [はい]> then 

end
```

--- /hint ---

--- hint ---

コードは次のようになります。

```blocks3
ask [月に行きたい？] and wait
if <(answer) = [はい]> then 
  switch backdrop to (moon v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

ここで、チャットボットをクリックして話しかけたときに、チャットボットが正しい場所で開始されることをたしかめる必要があります。このブロックをチャットボットのコードの先頭に追加します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch backdrop to (space v)
```

--- /task ---

--- task ---

プログラムをテストし、チャットボットが月に行きたいかどうかを聞いたら「はい」と答えます。チャットボットの場所がかわることがわかります。

--- /task ---

--- task ---

`もし`{:class="block3control"}ブロックに次のコードを追加して、「はい」と答えたときに、チャットボットを4回上下にジャンプさせます。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
if <(answer) = [はい]> then 
  switch backdrop to (moon v)
+  repeat (4) 
    change y by (10)
    wait (0.1) secs
    change y by (-10)
    wait (0.1) secs
  end
end
```

--- /task ---