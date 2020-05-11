## おしゃべりチャットボット

チャットボットのせいかくが決まったので、おしゃべりできるようにプログラムしましょう。

--- task ---

チャットボットのスプライトをクリックしてこのコードを追加 (ついか) し、`スプライトが押された (おされた) とき`{:class="block3events"}に`あなたの名前を聞いて`{:class="block3sensing"}、`「すてきな名前だね！」`{:class="block3looks"}と言うようにします。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
say [すてきな名前だね！] for (2) seconds
```

--- /task ---

--- task ---

チャットボットをクリックしてコードをテストします。チャットボットが名前を聞いたら、ステージの下部に表示されるボックスに名前を入力し、青いマークをクリックするか<kbd>Enter</kbd>を押します。

![チャットボットの答え](images/chatbot-ask-test1.png)

![チャットボットの答え](images/chatbot-ask-test2.png)

--- /task ---

--- task ---

今のところ、チャットボットは毎回「すてきな名前だね！」と答えます。ちがう名前が入力されるたびに返事をかえるようにすることで、もっと親しみやすくできます。

チャットボットのスプライトのコードを`～と～`{:class="block3operators"}に書きかえて、「やあ！」と「きみの名前は？」という質問 (しつもん) への`答え`{:class="block3sensing"}をつなげます。コードは次のようになります。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
say (join [やあ！ ] (answer) :: +) for (2) seconds
```

![答えをかえてみる](images/chatbot-answer-test.png)

--- /task ---

--- task ---

**変数** (へんすう) に答えを入れることで、プロジェクトのどの部分でも答えを使うことができます。

`名前`{:class="block3variables"}という新しい変数を作成 (さくせい) します。

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

次に、チャットボットのスプライトのコードをかえて`名前`{:class="block3variables"}変数を`答え`{:class="block3sensing"}に設定 (せってい) します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [きみの名前は？] and wait
+ set [名前 v] to (answer)
say (join [やあ！ ] (名前 :: variables +)) for (2) seconds
```

前と同じようにコードは動きますが、チャットボットは入力された名前を使ってあいさつするはずです。

![答えをかえてみる](images/chatbot-answer-test.png)

--- /task ---

もう一度テストしてみましょう。 入力した答えは`名前`{:class="block3variables"}変数に保存 (ほぞん) されていて、ステージの左上すみにも表示されていることに注意してください。 ステージに表示されないようにするには、`変数`{:class="block3variables"}ブロックセクションから、`名前`{:class="block3variables"}のとなりにあるボックスをクリックしてチェックを外します。