## 「はい」か「いいえ」で答える

入力によって、チャットボットがちがう答え方をするようにプログラムできます。

まず、「はい」または「いいえ」で答えることができる質問をチャットボットにさせます。

--- task ---

チャットボットのコードをかえます。 `名前`{:class="block3variables"}変数を使い、チャットボットに「名前　元気？」という質問をさせます。 `もし`{:class="block3control"}「はい」という答えのときには「それはよかった！」と答えます。答えが「いいえ」の場合は何も言いません。

![チャットボットの答え](images/chatbot-if-test1-annotated.png)

![チャットボットの答え](images/chatbot-if-test2.png)

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
set [名前 v] to (answer)
say (join [やあ ] (名前)) for (2) seconds
+ask (join [元気] (名前)) and wait
+if <(answer) = [はい]> then 
  say [それはよかった！] for (2) seconds
end
```

新しいコードをきちんとテストするためには、**2回**テストする必要があります。答えが「はい」の時と「いいえ」の時です。

--- /task ---

今のところ、チャットボットは答えが「いいえ」のときには何も言いません。

--- task ---

チャットボットのコードをかえて、「名前　元気？」という質問への答えが「いいえ」のときには、「あらら！」と答えるようにしましょう。

`もし～なら`{:class="block3control"}ブロックを`もし～なら～でなければ`{:class="block3control"}ブロックにかえて、チャットボットが `「あらら！」と言う`{:class="block3looks"}コードを入れます。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
set [名前 v] to (answer)
say (join [やあ！] (名前)) for (2) seconds
ask (join [元気？] (名前)) and wait
+ if <(answer) = [はい]> then 
  say [それはよかった！] for (2) seconds
else 
+  say [あらら！] for (2) seconds
end
```

--- /task ---

--- task ---

コードをテストしましょう。 あなたの答えが「いいえ」のときと「はい」のときではちがう答えが返ってくるはずです。「はい」と答えたときには、チャットボットは「それはよかった！」と答え、**他の答え**のときには「あらら！」と答えます 。

![チャットボットの答え](images/chatbot-if-test2.png)

![「はい」または「いいえ」と入力した時の答え](images/chatbot-if-else-test.png)

--- /task ---

`もし～なら～でなければ`{:class="block3control"}ブロックの中には、チャットボットの言葉だけではなく、ほかのコードも入れることができます。

チャットボットの**コスチューム**を見てみると、いくつかあるのがわかると思います。

![チャットボットのコスチューム](images/chatbot-costume-view-annotated.png)

--- task ---

チャットボットのコードをかえて、答えを入力したときにチャットボットがコスチュームを切りかえるようにします。

![コスチュームをかえる](images/chatbot-costume-test1.png)

![コスチュームをかえる](images/chatbot-costume-test2.png)

`もし～なら～でなければ`{:class="block3control"}ブロックの中のコードをかえて、`コスチュームを～にする`{:class="block3looks"}を追加します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
set [名前 v] to (answer)
say (join [やあ！] (名前)) for (2) seconds
ask (join [元気？] (名前)) and wait
if <(answer) = [はい]> then 
+  switch costume to (nano-c v)
  say [それはよかった！] for (2) seconds
else 
+  switch costume to (nano-d v)
  say [あらら！] for (2) seconds
end
```

コードをテストして保存しましょう。あなたの答えによってチャットボットの顔がかわります。

--- /task ---

チャットボットのコスチュームが変わった後、はじめのコスチュームにもどらないことに気づきましたか？

コードを実行して「いいえ」と答えると、チャットボットがおこった顔になります。 次にコードをもう一度実行して、チャットボットが名前を聞く前に、わらった顔にもどっていないことをたしかめます。

![コスチュームのバグ](images/chatbot-costume-bug-test.png)

--- task ---

この問題をかいけつするには、チャットボットのコードの`スプライトが押されたとき`{:class="block3events"}の先頭に`コスチュームを～にする`{:class="block3looks"}を追加します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
+ switch costume to (nano-a v)
ask [きみの名前は？] and wait
```

![コスチュームを直す](images/chatbot-costume-fix-test.png)

--- /task ---