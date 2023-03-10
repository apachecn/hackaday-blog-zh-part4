# 自动 Trickler 温柔地分发粉末，以协助重新加载

> 原文：<https://hackaday.com/2019/05/02/auto-trickler-gently-doles-out-powder-to-assist-reloading/>

你会滴吗？

[Eric]是的，就像其他关于重新加载的事情一样，涓滴是一件严肃的事情。获得要添加到弹药筒中的准确火药量不是一项简单的任务，并且当手动完成时非常乏味。这款由智能手机控制的自动驾驶仪旨在让这项工作变得更简单、更安全、更精确。

对于射手来说，重新装填弹药是一个省钱的好方法，也是一天结束时堆积在靶场的黄铜弹壳回收利用的好方法。这可能是一个相当简单的过程，清洗弹壳，更换用过的底火，添加正确的火药，并安装新的子弹。这一切都很简单，但问题在于细节，尤其是火药的问题。有点太多可能是一个大问题，所以发明了 tricklers，允许重新加载器偷偷进行适当的充电。[Eric]的 auto-trickler 接口到一个数字粉末秤，并使用一个标准的手机振动马达轻轻地从料斗中哄出单粒粉末，直到积累了适当的电荷。看下面的视频更容易理解。

trickler 背后的硬件是非常标准的——只有一个树莓 Pi Zero，可以通过蓝牙与智能手机 UI 对话，并通过 USB 监控和控制秤。[Eric]已经将所有代码开源，这样任何人都可以构建自己的 auto-trickler，我们对此表示赞赏；他用装在步枪上的加速度计做了同样的事情。这个项目的应用可能远远超出需要精确分配的重新装载。

 [https://www.youtube.com/embed/1BODqGHfVtk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1BODqGHfVtk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

