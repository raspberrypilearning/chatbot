## 改变位置

您还可以对聊天机器人进行编程以更改其位置！

![测试修改背景](images/chatbot-backdrop-moon.png)

--- task ---

你可以设置你的聊天机器人问“你想去月球”，然后当答案是“是”时改变背景吗？

--- hints ---

--- hint ---

你的聊天机器人应该 `问“你想去月亮？”`{:class="block3sensing"}，和 `如果`{:class="block3control"}你 `答案`{:class="block3sensing"} “是”，就应该 `的背景下切换到月亮`{:class="block3looks"}。

--- /hint ---

--- hint ---

以下是您需要添加到聊天机器人代码的代码块。

![纳米精灵](images/nano-sprite.png)

```blocks3
换成 (moon v) 背景

询问 [你想去月球吗？] 并等待

如果 <(回答) = [是]> 那么
end
```

--- /hint ---

--- hint ---

这是你的代码应该是这样的：

```blocks3
询问 [你想去月球吗？] 并等待
如果 <(回答) = [是]> 那么 
  换成 (moon v) 背景
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

现在，您需要确保当您点击聊天机会与其通话时，您的聊天机器人就会在正确的位置启动。将此块添加到聊天机器人代码的顶部：

![纳米精灵](images/nano-sprite.png)

```blocks3
当角色被点击
+ 换成 (space v) 背景
```

--- /task ---

--- task ---

测试您的程序，并在聊天机器人询问您是否想登月时回答“是”。您应该看到聊天机器人的位置发生了变化。

--- /task ---

--- task ---

您还可以添加以下代码新内 `，如果`{:class="block3control"}块，使聊天机器人上下跳跃四次，如果你回答“是”：

![纳米精灵](images/nano-sprite.png)

```blocks3
如果 <(回答) = [是]> 那么 
  换成 (moon v) 背景
+ 重复执行 (4) 次 
    将y坐标增加 (10)
    等待 (0.1) 秒
    将y坐标增加 (-10)
    等待 (0.1) 秒
  end
end
```

--- /task ---