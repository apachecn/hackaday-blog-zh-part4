# 樱桃番茄计时器迫使你跟随

> 原文：<https://hackaday.com/2021/10/31/cherry-pomodoro-timer-forces-you-to-follow/>

如果你很难集中注意力完成工作，番茄工作法中的 25 分钟间隔和 5 分钟休息是很难被打败的。唯一的问题是，它需要用户的大量输入，所有的计时器设置都会妨碍实际的工作。绝对最糟糕的是当你发现自己在努力工作，却看到忘记设置该死的定时器(问我们怎么知道的)。本质上，番茄本身只能做这么多——你必须实际使用它，尊重计时器，投入工作，并相信系统。

[![A tiny Pomodor Timer that starts automatically when plugged into a USB port.](img/6091a5fba5be0777d36715f44818a3fd.png)](https://hackaday.com/wp-content/uploads/2021/10/tiny-pomodoro-inner.gif) 但是如果你不用做那么多呢？[有了【范二 Sn】的设计，你所要做的就是把它插入 USB 端口](https://github.com/ErfanSn/ES-Timer)，倒计时就自动开始了。这款 Pomodoro 定时器不仅可以强迫你完成程序，还可以让你在 25 分钟(或你在软件中设置的任何时间)结束时，通过将电脑置于睡眠模式，从屏幕上休息一下。这东西甚至能记录你的番茄数。

这一构建的核心是 Digispark ATtiny85 开发板，它有一个方便的板载 USB 插头。它可以有或没有有机发光二极管屏幕，如果你很容易被计时器本身分散注意力，这很好。这种樱桃番茄的制作成本只有 10 美元，它很小，你可以把它带到任何地方。

正如你将在 GitHub 上的 gif 中看到的，[范二 Sn]将其插入母 USB-A 到公 USB-C，这可能对计算机的长期使用更好，因为所有的插拔。当我们制作自己的产品时，我们可能会将它插入一个集线器，每个端口都有电源开关。

如果这一切听起来像是太多的工作，[看看这个能感知你是否坐在椅子上的构建](https://hackaday.com/2020/01/29/lazydoro-mothers-you-into-being-productive/)。