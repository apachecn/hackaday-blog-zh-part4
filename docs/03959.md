# 报警系统被 2 美元的无线加密狗打败，没人感到惊讶

> 原文：<https://hackaday.com/2019/08/23/alarm-system-defeated-by-2-wireless-dongle-nobody-surprised/>

在一个已经因安全漏洞而饱受批评的产品上做文章似乎有点不公平。但当这种产品表面上是用来保护家人和财产安全的设备时，这就相当公平了。当这个设备是一个可以被两美元的无线遥控器打败的警报系统时，这实际上是一种责任。

问题中的物品是 SimpliSafe 警报系统，这是一个完全无线的，自己安装的系统，可以在网上和各种大型零售商那里买到。我们之前已经讨论过[该系统有严重缺陷的安全模型](https://hackaday.com/2016/02/23/breaking-simplisafe-security-systems-with-software-defined-radio/)，由此 SDRs 可以被用来执行低强度的重放攻击。尽管这种利用很简单，但与[LockPickingLawyer]的暴力攻击相比，它看起来非常优雅，该攻击使用 2 美元的 RF 遥控器作为传感器和基本单元之间 433 MHz 无线信号的干扰器。

通过将遥控器放在系统附近，他演示了打开门或窗并进入由 SimpliSafe 保护的财产而不留下任何痕迹是多么容易。是的，一个小小的遥控器可能不会从远处干扰系统，但像 Baofeng 提供的那种便宜的可编程双频收发器肯定会达到目的。不是一个有执照的业余操作者，[LockPickingLawyer]没有测试这一点，但我们怀疑小偷会像法院官员那样尊重法律。

警报系统的底线是你得到你所支付的，或者可悲的是，少得多。向[LockPickingLawyer]致敬，他展示了这个漏洞，以及他的许多其他开锁视频，非常值得一看。

 [https://www.youtube.com/embed/UlNkQJzw4oA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UlNkQJzw4oA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[fede.tft]的提示。