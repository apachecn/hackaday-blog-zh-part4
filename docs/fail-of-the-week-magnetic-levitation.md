# 本周失败:磁悬浮

> 原文：<https://hackaday.com/2021/10/16/fail-of-the-week-magnetic-levitation/>

我们是小型桌面磁悬浮装置的忠实粉丝，这种装置可以将一个小物体悬浮在磁铁上。正如[3D 打印生活]指出的，它们看起来像魔术。他感到惊讶的是，商业单位使用模拟电子设备。他决定建造一个数字版本的 T1，但不知道他会遇到什么。他在下面的视频中详细描述了他的旅程。

除了定制的控制板，他决定给自己的电磁铁上发条。在发现这种单调乏味之后，他制作了一个简单的绕线机来自动完成一些工作。

如果你曾经努力寻找磁铁在其中一个上的最佳位置，他的第一个问题是完全可以预见的。他失去了对磁铁的控制，磁铁猛烈撞击 PCB，从物理上或电气上损坏了磁性传感器。之后，他安装了一个屏蔽罩，防止磁铁直接接触电路板。

第一次迭代没有像预期的那样工作，磁性平台不断翻转。他最终发现了一个商业单元的拆卸，这表明他需要更多的稳定磁铁在电磁铁的外面。他也没有设置电磁体来改变极性。

解决极性问题需要重新利用通常用于电机控制的 H 桥电路。一个新的电路板在经过一点测试后被烧坏了。然后出现了机械故障。

一旦硬件开始工作，软件就会出现问题。PID 控制器不够稳定。他还尝试过滤输入，并添加一些其他的修正。平台会浮动一点，但最终会撞上电磁铁。

他没有得到一个最终的工作版本，但他希望有人能给他一些建议，让它工作起来。我们认为某个阅读 Hackaday 的人以前肯定已经建立了一个这样的网站，也许能够提供帮助。

也许轴的[变化会更容易。有几个](https://hackaday.com/2021/09/05/building-a-levitating-turbine-desk-toy/)[老项目](https://hackaday.com/2011/02/21/arduino-levitation/)可能会提供一些灵感。

 [https://www.youtube.com/embed/IhG_qHAvJd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IhG_qHAvJd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

