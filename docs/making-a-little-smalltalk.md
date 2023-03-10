# 闲聊几句

> 原文：<https://hackaday.com/2020/12/20/making-a-little-smalltalk/>

虽然像面向对象计算和模型-视图-控制器这样的东西现在已经过时了，但是当 Smalltalk 突然出现时，许多人从来没有听说过这些新思想。虽然这种源于施乐并基于 Simula 的小语言从未火起来，但它在许多方面都非常有影响力。现在 Smalltalk luminary [Dan Ingalls]有了 [Smalltalk Zoo](https://smalltalkzoo.thechm.org) ，这是一个 Smalltalk 相关项目的集合，包括几个你可以在浏览器中运行的历史模拟。

altosmaltalk-72 模拟给我们留下了特别深刻的印象，因为我们运行真正的 Alto 的机会非常小。它背后的 JavaScript 实际上实现了 Alto 的 Nova 指令集。模拟器然后从一个真实的 Alto 运行一个 45 年前的内存转储。据[Dan]说，没有文件系统，微编码音乐和动画指令也不见了，但他希望有人能把它们作为业余项目添加进来。

对于任何有足够勇气钻研这个老软件的人来说，还有一些其他的项目建议。我们发现 Smalltalk-72 Javascript 解释器的运行速度是原来的 500 多倍，并且具有“几乎无限”的对象存储，这很有趣。

在 Smalltalk 中，一切都是对象。比如乌龟图形对象(@)，你可以这样说:

```
@ go 50 turn 90 go 50 turn 90 go 50 turn 90 go 50\
```

当有人告诉你他们向 3 对象发送+消息是为了给 3 添加一些东西时，这就不那么有趣了，但是对你来说这就是面向对象。如果您不知道 Smalltalk，请尝试您可以在模拟器右侧找到的代码片段。