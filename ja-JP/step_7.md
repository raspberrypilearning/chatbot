## 背景（はいけい）をかえる

チャットボットのいるところの背景をかえることができます。

![背景をかえる](images/chatbot-backdrop-moon.png)

\--- task \---

チャットボットが「月に行きたい?」と聞いた後、答えが「はい」の時に背景を変えることができますか?

\--- ヒント \---

\--- hint \---

チャットボットが`「月に行きたいですか？」と聞いて`{:class="block3sensing"}、`もし`{:class="block3control"}あなたの`回答`{:class="block3sensing"}が「はい」ならば、`背景を月にする`{:class="block3looks"}ようにします。

\--- /ヒント \---

\--- hint \---

以下がチャットボットコードに追加するコードブロックです。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
switch backdrop to (moon v)

ask [月に行きたいですか？] and wait

if <(answer) = [はい]> then 

end
```

\--- /ヒント \---

\--- hint \---

コードは次のようになります。

```blocks3
ask [月に行きたいですか？] and wait
if <(answer) = [はい]> then 
  switch backdrop to (moon v)
end
```

\--- /hint \---

\--- /ヒント \---

\--- /task \---

\--- task \---

次に、チャットボットをクリックして話をするときに、チャットボットが正しい場所で開始することを確認する必要があります。このブロックをチャットボットコードの先頭に追加します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked

+ switch backdrop to (space v)
```

\--- /task \---

\--- task \---

プログラムをテストし、チャットボットが月に行きたいかどうかを尋ねるときに「はい」と答えます。チャットボットの場所が変わることがわかります。

\--- /task \---

\--- task \---

次のコードを含む新しい`もし`{:class="block3control"}ブロックを追加して、「はい」と答えた場合にチャットボットを4回上下にジャンプさせます。

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

\--- /task \---