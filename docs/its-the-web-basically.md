# 基本上是网络

> 原文：<https://hackaday.com/2018/09/17/its-the-web-basically/>

如果你到了一定的年龄，你可能已经学会了用 Basic 编程。即使你不是，许多微控制器爱好者已经开始学习基本的印记，还有许多其他地方仍然隐藏着古老的语言。但是要想写出很酷的浏览器应用，就得写 JavaScript 吧？谷歌现在可以让你用 Basic 语言对网页进行编码。这就是所谓的 WWWBasic，当然，这是一个 Javascript 黑客，你可以远程加载到一个网页中，然后让你的页面使用 Basic 进行定制。您甚至可以将它导入 Node.js，并在您的 JavaScript 中使用 Basic，尽管很难想象您为什么要这样做。

根据该项目的文档——恐怕到目前为止还很少——基本程序在页面加载时被编译成 JavaScript。这里有几个例子，所以你通常可以找到有用的东西。还有[图形](https://google.github.io/wwwbasic/examples/circles.html)，读取键盘按键的能力，以及处理鼠标的方法。

如果你在想老派游戏，显然谷歌也是如此。翻出一些充满基本游戏的旧书，在浏览器中获得《星际迷航》、《Wumpus》和那个时代的所有其他游戏，会很有趣。然而，看起来有些困难的事情还没有实现(例如，INPUT 语句)。我们假设你可以用 INKEY 写你自己的准输入函数，但是那会很痛苦。

我们找不到任何方法让基本代码直接与浏览器数据交互，这是一个遗憾，因为这意味着你的输出被限制在一个虚拟的基本“屏幕”上对于图形来说，它看起来相当不错，但文本输出[看起来像一台老派的计算机](https://google.github.io/wwwbasic/examples/primes.html)，它很迷人，但不太实用。例如，微软的 VBScript 技术可以像 JavaScript 一样写入页面，这在 WWWBasic 中会很好。

实用吗？可能不会，但我们很高兴看到我们的老朋友 Basic 再次出现在浏览器中。与 VBScript 不同的是，它有点复古，这让它变得更加有趣。

如果想要更传统的基础体验， [Quickbasic 还是在](https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/)左右。或者，如果你想让[停留在浏览器](https://hackaday.com/2016/02/05/a-dos-education-in-your-browser/)中，你也可以这样做。顺便说一句，在这篇文章的制作过程中，没有真正的驴子受到伤害。