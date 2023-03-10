# 用于检测 Z 轴高度的四个 SMD 电阻

> 原文：<https://hackaday.com/2019/01/27/quartet-of-smd-resistors-used-to-sense-z-axis-height/>

这里有一个为你的下一个 3D 打印机制造或改造的巧妙技巧:[一个 Z 轴传感器，使用由 SMD 电阻制成的 DIY 应变仪](https://github.com/IvDm/Z-probe-on-smd-resistors-2512)。我们打赌它还可以有很多其他的应用。

传统的称重传感器，至少是那些你可以从普通来源廉价买到的或者从旧厨房或浴室秤中收获的称重传感器，通常都太大了，无法在 3D 打印机的挤压机上使用。[IvDm]想要为他的 [Hybercube 打印机](https://www.thingiverse.com/thing:1752766)制造一个触摸传感器，所以他制造了自己的称重传感器来完成这项工作。它由四个 1000 ohm SMD 电阻组成，采用大 2512 器件尺寸。他将它们安装在一个 X 形 PCB 上，并以经典的惠斯通电桥配置连接，电路板的一侧有两个电阻，另一侧有两个电阻。

挤压机安装在板中心的一个孔中，并浮在上面。通过 HX711 称重传感器驱动芯片，当挤出机降至底部时，电桥会感应到板的轻微弯曲，ATtiny85 会将限位开关输入拉至接地。[IvDm]甚至用这种传感器做了一些重复性测试，结果令人惊讶地一致。下面视频的第一分钟左右显示了它在 Hypercube 上的运行。

我们发现使用 SMD 电阻器作为应变仪非常聪明，但现成的称重传感器还有很多事情要做:[测量一卷上还剩多少细丝](https://hackaday.com/2018/08/10/3d-printers-get-a-fuel-gauge-adding-a-filament-scale-to-octoprint/)，[检查模型火箭发动机的推力](https://hackaday.com/2018/12/14/arduino-powered-rocket-test-stand/)，甚至[计算你是否正确撒尿](https://hackaday.com/2018/04/01/assess-your-output-with-a-cheap-diy-urine-flowmeter/)。

 [https://www.youtube.com/embed/x-7hq27BdUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x-7hq27BdUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[jschoch]的提示。