# 克隆门遥控器做得(稍微)好一点

> 原文：<https://hackaday.com/2019/12/11/cloned-gate-remote-does-it-slightly-better/>

有没有做过一些东西只是为了看看你能不能做？是啊，我们也这么想。[serverframework] [想看看他是否能克隆一个遥控器来打开他的邻居大门](https://pseudo-server.com/blog/gate-remote-reverse-engineered-and-ported-to-an-attiny85/)，这是受[Samy Kamkar]的长距离叮咚沟努力的启发。

这个复制品使用一个 ATtiny85 和一个 RF 模块来模拟和发送 gate 正在等待的频率。为了实现这一点，[serverframework]必须计算出遥控器使用的操作频率和时间。里面的晶体似乎显示 295 MHz，快速检查该设备的 FCC 注册确认了这一点。然后，他使用 SDR 加密狗来观察他按下按钮时传来的数据，并通过 Audacity 来计算时间。

不幸的是，295 MHz 晶体是一种罕见的野兽，所以[serverframework]不得不将原件移植到施主 RF 模块。然后，只需对 ATtiny85 进行编程，使其在正确的时间发送频率。它实际上做得更好，因为原来的没有计时晶体，而“微小的”是由标准的 16 千赫振荡器计时。代码可以在[serverframework]的精彩文章中找到，休息之后你可以看到一个小演示。

克隆星门遥控器的方法不止一种。这个利用 MQTT 将朋友的手机变成遥控器。

 [https://www.youtube.com/embed/SlIowuft5LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SlIowuft5LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

