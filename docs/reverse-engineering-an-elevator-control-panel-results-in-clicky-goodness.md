# 对电梯控制面板进行逆向工程会产生良好的点击效果

> 原文：<https://hackaday.com/2021/02/04/reverse-engineering-an-elevator-control-panel-results-in-clicky-goodness/>

我们不得不承认，在硬件黑客世界里，一般没有太多机会黑电梯。嗯，至少没有不包括入狱风险的机会。但是财富偏爱勇敢的人，当他在一个废弃的克罗地亚度假酒店发现电梯控制面板的残骸时，[Davor Cihlar]对面板进行了广泛而有益的逆向工程。

下面的视频突出了他的努力，考虑到专家组的年龄和状态，这些努力是相当大的。毕竟，这是一个只有继电器的控制面板，大部分继电器都不见了，连接插座的电线像老鼠窝一样。因此[Davor]将他的[【RevIng】](https://bitbucket.org/dcihlar/reving/src/master/)概念付诸实践。它使用一个带有微控制器的定制 PCB，插入每个继电器插座，并探测它与其他插座之间的连接。非常聪明的东西，在一些定制软件的帮助下，它为他提供了开发电路板梯形逻辑图所需的数据。

有了原始逻辑，[Davor]开始为面板构建模拟器。这是一件可爱的作品，按钮和灯光模仿了电梯车厢内的控制面板，以及酒店每个大厅的呼叫站。有趣的是，他发现了阻止电梯从除了轿厢内的任何地方被呼叫到某些楼层的逻辑。原因仍然是个谜，但我们猜想由《阁楼》出版商[鲍勃·古乔内]建造的酒店会有很多秘密。

我们喜欢这种构建令人极其满意的点击感，以及展示的逆向工程能力，但我们找不到像这样的东西有多少实际用途。话说回来， [DIY 电梯是个东西](https://hackaday.com/2020/12/28/build-your-own-custom-elevator/)。

 [https://www.youtube.com/embed/TJmAQJqro_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TJmAQJqro_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

