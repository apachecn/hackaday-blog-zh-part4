# 像飞驰的子弹一样快

> 原文：<https://hackaday.com/2022/02/14/as-fast-as-a-speeding-bullet/>

[Electronoobs]造了一个线圈炮，一个明显的问题是:弹丸有多快？为了回答这个问题，他制作了一个适合为子弹计时的[计时器](https://www.youtube.com/watch?v=oe99JtUOR7U)。原理很简单。一束激光和一个光传感器将在已知的距离上标记投射物的进入和退出。事实证明，有一些问题需要解决。

首先，激光太窄，可能会错过抛射体。第一次尝试使用镜子来纠正这一点，但损失太大了——我们怀疑他使用了第二面镜子。最终的答案是使用探测器阵列，并移除激光器的准直透镜，以覆盖更大的区域。

这很有效，所以剩下的就是一个很好的机械设计，允许改变传感器的高度和传感器之间的距离。之后，Arduino 就可以接管了。

我们喜欢它的机械设计，以及他在 3D 打印外壳中管理按钮的方式。我们不禁想知道第一面镜子是否会工作得更好。我们还认为添加某种编码器会很好，因为它是可调的，所以可以让设备自动测量传感器之间的距离。我们还认为光敏电阻的响应时间和波长灵敏度可能有点差。似乎光电二极管或晶体管会更精确，对激光或甚至只是传统光源有更好的灵敏度。但这似乎确实有效。

线圈炮有多快？超过每秒 100 米。作为参考，一发 0.22 口径的子弹的初速会超过每秒 300 米，但是，每秒 120 到 130 米也是不容忽视的。

如果你需要一个卷发器，我们总是[喜欢这个](https://hackaday.com/2012/09/14/coilgun-with-laser-sights-built-in-an-airsoft-rifle-housing/)的样子。或者，你可能更喜欢[更具未来感的外观](https://hackaday.com/2010/09/23/youll-shoot-your-eye-out-another-coilgun/)。

 [https://www.youtube.com/embed/oe99JtUOR7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oe99JtUOR7U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

