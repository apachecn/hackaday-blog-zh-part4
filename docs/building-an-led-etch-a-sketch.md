# 构建 LED 蚀刻草图

> 原文：<https://hackaday.com/2021/03/11/building-an-led-etch-a-sketch/>

蚀刻素描是一个需要掌握的玩具。一些人逐渐有能力创作出精湛的艺术作品，而另一些人则努力创作出更多愤怒、棱角分明的线条。当然，[和【gatoninja236】用现代的 LED 形式再现了这一点。](https://www.hackster.io/gatoninja236/pix-a-sketch-a-virtual-etch-a-sketch-on-an-led-matrix-dd3bae)

构建使用 Raspberry Pi 来运行显示，64×64 LED 矩阵连接到 GPIO 引脚作为显示器。由于可用的 GPIOs 有限，两个编码器用于重建著名的 Etch-A-Sketch 界面，连接到 Arduino Nano，然后通过 I2C 将编码器数据传输到 Pi。还有一个 MPU6050 加速度计板，用于实现直观的震动清零功能。

最终的结果是一个有趣的 LED 玩具，不像真正的蚀刻素描，你可以在黑暗中玩。我们以前也见过经典玩具上的其他偷偷摸摸的黑客——[像这款三星电视巧妙地隐藏在一个相似的外壳中](https://hackaday.com/2021/01/16/tv-turned-automatic-etch-a-sketch-with-raspberry-pi/)。休息后的视频。

 [https://www.youtube.com/embed/GAi95RBjf7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GAi95RBjf7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

