# 洗衣监视器不会与室友产生静电

> 原文：<https://hackaday.com/2020/05/15/laundry-monitor-wont-generate-static-with-roommates/>

洗衣服。这是生命不可避免的循环之一，但至少我们现在有了机器。这项创新的缺点是，由于我们不再监控每一个步骤——敲打岩石、冲洗河流、晾衣绳和收回——洗衣的痛苦已经演变成监控机器人工作的单调乏味。

[Adam]与室友分享他的清洗机器人，他们没有足够的距离将他们的明暗结合起来，并将其变成一项集体活动。他们需要一种简单的方法来判断机器何时运行完毕，以及谁的东西还在里面，所以[【Adam】建造了一个洗衣机监控器，它使用电流感应来检测机器何时运行完毕，并向适当的人发送文本](http://hackaday.io/project/169990-easy-laundry-monitor)。

每台机器都有一个小小的霍尔效应感应模块，小心地用拉链系在电源线上。当机器运行时，来自这些三线板的信号变高，当机器不运行时，信号变低。在开始装载时，洗衣工只需按下控制盒上分配给他们的按钮，里面的 ESP32 就会处理剩下的事情。

当你的抽屉干净的时候收到短信是最隐私的了。干净内衣，不在乎？把它放在滚动字幕上。