## 会说话的机器人

既然你有一个有个性的聊天机器人，你就要编程让它跟你说话。

\--- task \---

点击你的聊天机器人精灵，这个代码添加到它，以便 `时，它被点击`{:class=“block3events”}，这 `询问你的姓名`{:class=“block3sensing”}，然后 `说：“什么可爱的名字！“`{:class =“block3looks”}。

![纳米精灵](images/nano-sprite.png)

```blocks3
当这个精灵点击
问[你的名字是什么？]并等待
说[多么可爱的名字！]为（2）秒
```

\--- /task \---

\--- task \---

单击您的聊天机器人以测试您的代码。当聊天机器人询问您的姓名时，请在舞台底部显示的框中键入，然后单击蓝色标记，或按 <kbd>输入</kbd>。

![测试聊天机器人回复](images/chatbot-ask-test1.png)

![测试聊天机器人回复](images/chatbot-ask-test2.png)

\--- /task \---

\--- task \---

现在，您的聊天机器人回复“多么可爱的名字！”每次你回答。您可以使聊天机器人的回复更加个性化，以便每次输入其他名称时回复都不同。

将聊天机器人精灵的代码更改为 `加入`{:class =“block3operators”}“嗨”， `回答`{:class =“block3sensing”}改为“你叫什么名字？”问题，所以代码看起来像这样：

![纳米精灵](images/nano-sprite.png)

```blocks3
当这个精灵点击
问[你的名字是什么？]并等待
说（加入[Hi]（回答）:: +）（2）秒
```

![测试个性化回复](images/chatbot-answer-test.png)

\--- /task \---

\--- task \---

通过将答案存储在 **变量**，您可以在项目的任何位置使用它。

创建一个名为 `name`{：class =“block3variables”}的新变量。

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

现在，改变你的聊天机器人精灵的代码所设置的 `名`{：类=“block3variables”}变量 `回答`{：类=“block3sensing”}：

![纳米精灵](images/nano-sprite.png)

```blocks3
当这个精灵点击
询问[你的名字是什么？]并等待

+设置[name v]到（回答）
说（加入[Hi]（名称::变量+））（2）秒
```

您的代码应该像以前一样工作：您的聊天机器人应该使用您输入的名称打招呼。

![测试个性化回复](images/chatbot-answer-test.png)

\--- /task \---

再次测试你的程序。 请注意，您键入的答案存储在 `名称`{：class =“block3variables”}变量中，并且还显示在舞台的左上角。 To make it disappear from the Stage, go to the `Variables`{:class="block3variables"} blocks section and click on the box next to `name`{:class="block3variables"} so that it is not marked.