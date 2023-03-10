# Arduino 心率监测器拥有星际旅行的时尚

> 原文：<https://hackaday.com/2018/12/23/arduino-heart-rate-monitor-has-star-trek-chic/>

自从麦考伊博士第一次抱怨被要求在他的工作范围之外工作以来，建造一个现实版的《星际迷航》三记录器一直是工程师和黑客们的目标。但是，尽管现代技术已经提供了功能非常相似的小工具，但在复制 24 世纪星际舰队的设计美学之前，我们还有很长的路要走。幸运的是，全世界都有乐于接受挑战的专业黑客。

[![](img/63349498519c8ab8e2d9ea9c2bfb7f10.png)](https://hackaday.com/wp-content/uploads/2018/12/arduheart_detail.jpg) 【品典】就是这样一个黑客。他想为自己打造一个实用的小工具[，看起来就像在皮卡德的*企业*](https://www.instructables.com/id/Arduino-Heart-Rate-Monitor-1/) 上一样，所以他收集了各种组件来构建一个手持式心率监测器，并开始寻找合适的外壳。由于我们在后 Arduino 世界中享有的高可用性和模块化，这些电子设备很容易组装起来，但正如你可能预期的那样，在保持功能性的同时，将它放入一个看起来很科幻的包装中有点困难。

在内部，他的心率监测器使用 Arduino Pro Mini、小有机发光二极管屏幕和交钥匙脉冲传感器，该传感器最初是由“世界著名电子公司”在 2011 年作为 Kickstarter 构想的。布线非常简单:显示器通过 I2C 连接到 Arduino，脉搏传感器连接到一个免费的模拟引脚。一切都由 3 节 4.5 伏的 AA 电池供电，所以他甚至不需要稳压器或可充电电池组所需的额外组件。

一旦在试验板上确认一切工作正常，[品尝代码]就开始将一个手持陀螺玩具转换成他的心率监测器的新家。他把电池盒放在底部，但其他所有东西都被拆下来腾出空间。一个孔是在手枪握柄上，这样指尖就可以放在脉搏传感器上，另一个孔是在有机发光二极管屏幕的侧面。这使得用户在获取读数时能够以自然的方式握住设备。他提到，传感器可能是一个棘手的问题，但总的来说，它给出了足够准确的读数来满足他的目的。

如果你对现实生活中的[实际方面更感兴趣的话*星际旅行*三录仪](https://hackaday.com/2014/01/05/the-berkeley-tricorder-is-now-open-source/)我们已经看过[这些年的几个项目](https://hackaday.com/2014/11/03/the-hackaday-prize-the-hacker-behind-the-first-tricorder/)，包括几个进入黑客日奖的[。](https://hackaday.com/2015/06/22/hackaday-prize-entry-a-medical-tricorder/)

 [https://www.youtube.com/embed/iVN3gXZ72P8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iVN3gXZ72P8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

