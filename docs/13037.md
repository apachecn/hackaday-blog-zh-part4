# 将 OpenSCAD 放入浏览器的崇高努力

> 原文：<https://hackaday.com/2022/03/14/the-noble-effort-to-put-openscad-in-the-browser/>

在一个界面晦涩难懂或不友好的 CAD 软件包的世界里，有一个引人注目的玩家，因为它没有界面。OpenSCAD 是一个面向编码人员的 CAD 软件包，其中所有的设计元素都是用脚本语言而不是图形语言创建的。它可能不适合所有人，但它有一个重要的追随者，而且它的影响范围已经进一步扩大，因为你现在可以在一个现代的网络浏览器中运行它。

这个项目的起源可以追溯到 2021 年 8 月，当时 Autodrop3D 的[mmiscool]为任何愿意将参数化 CAD 建模器移植到 web assembly 的人提供了一笔可观的奖金。开发者 Dominick Schroer 最终用 [openscad-wasm](https://github.com/DSchroer/openscad-wasm) 回应了这一号召，它将 openscad 的核心实现为一个 JavaScript ES6 模块。从那里开始，它只需要与用户界面配对，然后就可以进入云计算了。

打开它并试了一下，我们发现它是一个非常有用的 OpenSCAD 版本，尽管比普通笔记本电脑上的桌面版稍慢一些。我们没有尝试导出和打印 STL，但是到目前为止，我们没有理由相信它不会像你习惯的版本一样有用。

但是等等，还有呢！与此同时， [[Olivier Chafik]也在研究他自己的想法](https://ochafik.com/openscad/),即网络中的 OpenSCAD 应该是什么样的。他使用的是由[Dominick]开发的相同内核，但是结合了微软的 Monaco 编辑器和 Javascript STL 浏览器。尽管非常相似，我们很高兴地报告这里没有竞争；事实上，根据休息后的视频，听起来两个项目已经交换了一点代码。

近年来，桌面应用程序向浏览器和付费云迁移的趋势似乎一直在持续，所以很高兴看到一个罕见的开源浏览器迁移的例子。它可以方便地将 CAD 包带到平板电脑或 Chromebooks 等平台上，这些平台通常不是 OpenSCAD 平台，这是我们非常喜欢的。

 [https://www.youtube.com/embed/izXq3d_rB9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/izXq3d_rB9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

