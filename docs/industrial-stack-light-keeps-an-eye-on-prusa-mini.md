# 工业堆栈灯关注 Prusa Mini

> 原文：<https://hackaday.com/2021/01/09/industrial-stack-light-keeps-an-eye-on-prusa-mini/>

当大多数人想在外出时随时了解他们的 3D 打印机在做什么时，他们会在 Pi 上安装 OctoPrint 并完成它。但是如果你只是在房间的另一边呢？受到工厂车间使用的烟囱灯的启发， [[Jeff Glass]决定在他的 Prusa Mini](https://github.com/JeffersGlass/prusa-usb-andon) 上安装一个类似的系统，这样他就能一眼看出它在做什么。

[![](img/f10a0fa0864288419080eaf861bf5989.png)](https://hackaday.com/wp-content/uploads/2020/12/3dpstatus_detail.jpg) 事实证明，你可以在网上以非常便宜的价格从普通零售商那里买到这些灯，正如[杰夫]在广告之后的视频中解释的那样，驾驶它们几乎是再容易不过了。它们不是某种可寻址的设备，通常每种颜色都有一根 12 或 24 伏的 DC 线和地线。有了 USB 控制的继电器板，从您选择的操作系统启动适当的灯是简单的。

最终变得有点困难的是发现普鲁萨 Mini 在做什么。打印机提供了一个简单的状态网页，但是它有一些奇怪的地方，很难抓取；比如显示一个小小的弹出消息，每次加载页面时都必须手动关闭它。但是在花了一些时间使用 Python 的强大的 Selenium 库之后，他能够创建一个通过 UI 运行的脚本，并提取相关的状态消息。显然，产生的代码是特定于 Prusa 的，但一般概念也适用于其他打印机，前提是您能找到一种可靠的方法来获取设备的当前状态。

在为电子设备设计了一个壁挂式外壳，同时也是灯本身的支架后，[Jeff]现在可以从房间的另一端清楚地看到他的打印机是否需要关注。当打印机[被扣在外壳](https://hackaday.com/2016/08/02/3d-printer-enclosure-is-pleasant-on-the-eyes-and-ears/)内时，这是一个特别好的功能。

 [https://www.youtube.com/embed/QZUyAC2vlHU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QZUyAC2vlHU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

