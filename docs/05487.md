# 闪烁探测器让你听到你看不到的东西

> 原文：<https://hackaday.com/2020/01/28/flicker-detector-lets-you-hear-what-you-cant-see/>

你有没有观察过现代的 LED 照明，并注意到，也许就在你感知的边缘，它们似乎在闪烁？嗯，那是因为他们可能是。电脑显示器或手机屏幕上的发光二极管也是如此。脉宽调制(PWM)广泛用于 led，以提供亮度控制，如果做得不好，可能会导致头痛和眼睛疲劳。

为了量化我们暴露在多少闪光灯下，[Faransky]发明了一个简单的小工具，基本上将闪光灯转换成人耳可以接收的音频。这些 led 闪烁的速度可能足以欺骗我们的眼睛，但你的耳朵可以听到比普通 PWM 解决方案中使用的频率高得多的频率。在休息后的视频中，你可以看到各种 LED 光源在使用设备时发出的声音是什么样的。

这里的电子设备非常简单。只需将一个小太阳能电池板连接到音频放大器，在这种情况下，PAM8403，并听取输出。为了更方便使用，它有一个内部电池，充电器电路和 USB-C 端口；但是如果你想用零件箱里已经有的东西做一个，你也可以很容易地用 9 V 的碱性电池来做。

谁知道呢？如果你随身携带这个东西足够长的时间，[你甚至可能听到远不常见的二进制编码调制](https://hackaday.com/2011/07/22/using-binary-code-modulation-to-control-led-brightness/)在起作用(但可能不会)。

 [https://www.youtube.com/embed/7xvkpSuqwq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7xvkpSuqwq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

