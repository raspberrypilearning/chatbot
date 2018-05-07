## おしゃべりチャットボット

チャットボットのせいかくが決まったので、おしゃべりができるようにプログラムしましょう。

\--- task \---

クリックされた時に、チャットボットが名前を聞いたら「すてきな名前だね！」と答えるように、コードを入れてみましょう。

![Testing a ChatBot response](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- チャットボットが **クリックされた時**に、名前を**聞く** ようにしましょう。 チャットボットは「すてきな名前だね！」と**言います**。 \--- /hint \--- \--- hint \--- 使うブロックはこちらです。 ![Blocks for a ChatBot reply](images/chatbot-ask-blocks.png) \--- /hint \--- \--- hint \--- コードの見本はこちらです。 ![Code for a ChatBot reply](images/chatbot-ask-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

チャットボットは毎回「すてきな名前だね!」と答えます。チャットボットの返答を個性的に変えることができますか？

![Testing a personalised reply](images/chatbot-answer-test.png)

\--- hints \--- \--- hint \--- チャットボットが **クリックされた時**に、名前を**聞く** ようにしましょう。 チャットボットは「やあ！」と**言います**。その後に、自分の**答え**が続きます。 \--- /hint \--- \--- hint \--- 使うブロックはこちらです。 ![Blocks for a personalised reply](images/chatbot-answer-blocks.png) \--- /hint \--- \--- hint \--- コードの見本はこちらです。 ![Code for a personalised reply](images/chatbot-answer-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

答えを**変数（へんすう）**に入れると、後でも使うことができます。`名前`という変数を新しく作りましょう。

[[[generic-scratch-add-variable]]]

\--- /task \---

\--- task \---

自分の答えを`名前` 変数に入れて、チャットボットの答えに使ってみましょう。

前と同じようにコードは動きます。チャットボットは入力された名前を使って話します。

![Testing a 'name' variable](images/chatbot-ask-test.png)

\--- hints \--- \--- hint \--- チャットボットが **クリックされた時**に、名前を**聞く** ようにしましょう。 You should then **set** the `name` variable to your **answer**. The chatbot should then **say** "Hi", followed by your **name**. \--- /hint \--- \--- hint \--- Here are the code blocks you'll need: ![Blocks for a 'name' variable](images/chatbot-variable-blocks.png) \--- /hint \--- \--- hint \--- Here's how your code should look: ![Code for a 'name' variable](images/chatbot-variable-code.png) \--- /hint \--- \--- /hints \---

\--- /task \---

\--- challenge \---

## チャレンジ：質問（しつもん）をふやす

Program your chatbot to ask another question. Can you store the answer in a new variable?

![More questions](images/chatbot-question.png) \--- /challenge \---