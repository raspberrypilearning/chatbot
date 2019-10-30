## おしゃべりチャットボット

チャットボットの性格が決まったので、おしゃべりできるようにプログラムしましょう。

\--- task \---

チャットボットのスプライトをクリックしてこのコードを追加し、`クリックされたときに`{:class="block3events"}`あなたの名前を尋ねて`{:class="block3sensing"}、`「素敵な名前ですね！」` {:class="block3looks"}と言うようにします。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [あなたの名前は何ですか？] and wait
say [素敵な名前ですね！] for (2) seconds
```

\--- /task \---

\--- task \---

チャットボットをクリックしてコードをテストします。チャットボットが名前を尋ねたら、ステージの下部に表示されるボックスに名前を入力し、青いマークをクリックするか<kbd>Enter</kbd>を押します。

![チャットボットの答え](images/chatbot-ask-test1.png)

![チャットボットの答え](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

すると、質問に答えるたびにチャットボットが「素敵な名前ですね！」と返答します。チャットボットの返答がより個人的なものになるように、異なる名前が入力されたら返答を変えるようにできます。

チャットボットのスプライトのコードを`～と～`{:class="block3operators"}に書き換えて、「こんにちは」と「あなたの名前は何ですか？」という質問への`回答`{:class="block3sensing"}をつなげます。コードは次のようになります。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [あなたの名前は何ですか？] and wait
say (join [こんにちは ] (answer) :: +) for (2) seconds
```

![答えをかえてみる](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

**変数**に回答を保存することにより、プロジェクトのどこでも使うことができます。

`名前`{:class="block3variables"}という新しい変数を作成します。

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

次に、チャットボットスプライトのコードを変更して`名前`{:class="block3variables"}変数を`回答`{:class="block3sensing"}に設定します。

![ナノ スプライト](images/nano-sprite.png)

```blocks3
when this sprite clicked
ask [あなたの名前は何ですか？] and wait

+ set [名前 v] to (answer)
say (join [こんにちは ] (名前 :: variables +)) for (2) seconds
```

前と同じようにコードは動きますが、チャットボットは入力された名前を使ってあいさつするはずです。

![答えをかえてみる](images/chatbot-answer-test.png)

\--- /task \---

もう一度テストしてみましょう。 入力した回答は`名前`{:class="block3variables"}変数に保存されていて、ステージの左上隅にも表示されていることに注意してください。 ステージに表示されないようにするには、`変数`{:class="block3variables"}ブロックセクションに移動して、`名前`{:class="block3variables"}の隣にあるボックスをクリックしてマークを外します。