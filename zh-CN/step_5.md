## 决策

你可以对聊天机器人进行编程，以根据收到的答案决定做什么。

首先，你要让你的聊天机器人提出一个可以用“是”或“否”回答的问题。

\--- task \---

更改聊天机器人的代码。 你的聊天机器人应该使用 `名称`{：class =“block3variables”}变量来询问“你还好吗加你的名字”。 然后它应该回答“这听起来很棒！” `如果`{:class =“block3control”}它收到的答案是“是”，但如果答案为“否”则不说。

![测试聊天机器人回应](images/chatbot-if-test1-annotated.png)

![测试聊天机器人回应](images/chatbot-if-test2.png)

![纳米精灵](images/nano-sprite.png)

```blocks3
当角色被点击
询问[你的名字是什么？] 并等待
将[name v] 设为（回答）
说（连接[你好]（姓名））（2）秒
+询问（连接[你还好]（姓名））并等待
+如果 <（答案）= [yes]> 那么
  说[很高兴听到！]（2）秒
结束
```

要正确测试新代码，你应该测试它 **两次**：一次回答“是”，一次回答“否”。

\--- /task \---

At the moment, your chatbot doesn't say anything to the answer "no".

\--- task \---

更改聊天机器人的代码，以便回复“哦不！”如果它收到“否”作为“你还好吗加你的名字”的答案。

将 `如果，那么`{：class =“block3control”}块替换为 `如果，那么，否则`{：class =“block3control”}块，并包含代码，以便聊天机器人可以 `说“哦不！”`{：class =“block3looks”}。

![纳米精灵](images/nano-sprite.png)

```blocks3
当角色被点击
询问[你的名字是什么？]并等待
将[name v]设为（回答）
说（连接[你好]和（姓名））（2）秒
询问（连接[你还好]和（姓名））并等待

+如果 <（答案）= [yes]> 那么 
  说[很高兴听到！]为（2）秒
否则
+说[哦不！]为（2）秒
结束
```

\--- /task \---

\--- task \---

测试你的代码。 当你回答“否”和回答“是”时，你应该得到两个不同的回答：当你回答“是”（不区分大小写）时，你的聊天机器人应该回答“这听起来很棒！”，当你回答 **其他任何事情**回复“哦不！”。

![测试聊天机器人回应](images/chatbot-if-test2.png)

![测试是/否回复](images/chatbot-if-else-test.png)

\--- /task \---

你可以将任何代码放在 `如果，然后，`{:class=“block3control”}块中，而不仅仅是使聊天机器人说话的代码！

如果你单击聊天机器人的 **服装** 选项卡，你将看到有多个服装。

![聊天机器人造型](images/chatbot-costume-view-annotated.png)

\--- task \---

更改聊天机器人的代码，以便在你输入答案时聊天机器人切换服装。

![测试更换造型](images/chatbot-costume-test1.png)

![测试更换造型](images/chatbot-costume-test2.png)

将 `如果，然后，或者`{：class =“block3control”}块内的代码更改为 `换成服装/0>{：class =“block3looks”}。</p>

<p><img src="images/nano-sprite.png" alt="纳米精灵" /></p>

<pre><code class="blocks3">当角色被点击
询问[你的名字是什么？] 并等待
将[name v] 设为（回答）
说（连接[你好] 和（姓名））（2）秒
询问（连接[你还好]（名）），并等待
如果 <（回答）= [yes]> 那么

+换成（nano-c v）造型
  说[那真是太好了！]（2）秒
否则
+换成（nano-d v）造型
  说[哦不！]（2）秒
结束
`</pre> 

测试并保存你的代码。你应该看到聊天机器人的脸部会根据你的答案而改变。

\--- /task \---

你是否注意到，在你的聊天机器人的服装发生变化之后，它会保持这种状态并且不会改变回原来的状态？

你可以尝试这样做：运行你的代码并回答“否”，使你的聊天机器人变成不快乐的脸。 然后再次运行您的代码并注意您的聊天机器人在询问您的姓名之前不会变回看起来很开心。

![造型bug](images/chatbot-costume-bug-test.png)

\--- task \---

要解决此问题，请在点击精灵</code>{:class =“block3events”}时，在开始 `处将聊天机器人的代码添加到 <code>切换服装`{:class =“block3looks”}。

![纳米精灵](images/nano-sprite.png)

```blocks3
当这个精灵点击

+切换服装到（纳米-a v）
问[你叫什么名字？]并等待
```

![当角色被点击

+换成（nano-a v）造型
问[你叫什么名字？] 并等待](images/chatbot-costume-fix-test.png)

\--- /task \---