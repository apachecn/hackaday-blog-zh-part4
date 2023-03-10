# 一个可热插拔的电池手柄让相机保持运转

> 原文：<https://hackaday.com/2021/04/21/a-hot-swappable-battery-grip-keeps-the-camera-rolling/>

没有什么比正在拍摄一个重要的镜头，却发现相机的电池没电了更糟糕的了。损失可能非常真实，所以最好完全避免。为了做到这一点，[【funk ster】为自己的佳能 EOS M](http://funkster.org/e/hack/hotswapgrip) 造了一个电池手柄。

黑客是基于古老的 18650 电池，将 3.6V 的锂离子电池装入一个紧凑的金属罐中。[funkster]的构建有两个这样的电池插槽，关闭其中一个电池的电源，保留另一个电池备用。电池由 STM32 微控制器监控，当电池耗尽或被移除时，它会从一个电池切换到另一个电池。这允许在相机打开时更换电池，这是一个非常有用的功能。甚至还有一个有机发光二极管显示器来监视每个电池的充电状态。

电源连接到照相机的方式相当有趣。一个原来的佳能电池滑入相机内部被挖空，变成了一个简单的电池端口适配器。包裹在相机机身周围的电池手柄通过穿过相机外壳上钻孔的插头连接到机身。这是一个永久的 mod，但一个[funkster]对增加的可用性感到满意——特别是这样做仍然提供了对 SD 卡插槽的轻松访问。

没有合适的装备，让相机在旅途中保持充足的电量是一件令人头疼的事情。[funkster]论证了如果你买不到，你总是可以自己建造。如果你的问题不是电池电量，而是你的相机过热，你当然也可以解决这个问题。休息后的视频。

 [https://www.youtube.com/embed/-LdBVMd4dAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-LdBVMd4dAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

