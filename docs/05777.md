# 对抗重力的水滴喷泉升级了

> 原文：<https://hackaday.com/2020/02/25/gravity-defying-water-droplet-fountain-gets-an-upgrade/>

当我们最后一次看到[isaac879]的[悬浮 RGB 时间喷泉](https://hackaday.com/2018/03/14/led-illusion-makes-colorful-water-drops-defy-gravity/)时，它是由木头制成的，这意味着它会吸水，并没有很好地展示效果。他的新版本通过丙烯酸外壳、新的 PCB 和更新的电路解决了这个问题。

像原来一样，这个项目将水滴通过频闪的 RGB LEDs，创造出漂浮、起伏的彩色水滴的幻觉。顶部的泵产生液滴，但时间会随着时间推移而漂移。因此，他实现了一个 PID 控制器来管理泵的滴速，这是通过让液滴经过一个连接到 ATTiny85 的红外二极管来实现的。’85 使用二极管和 PWM 来控制泵电机速度，并通过 I2C 与 Arduino 通信。

下面的视频展示了设计和建造新时间喷泉的全过程。从电路和 PCB 设计到 3D 打印再到组装，所有的东西都随着叙述一起展示，描述正在发生的事情，以防你想自己建造一个。如果你这样做，所有需要的文件和组件都列在视频的信息部分。

[isaac879]还想做更多来改进时间喷泉，但 V2 看起来很棒。它比原来的更时尚、更小巧，解决了第一款的一些设计问题。想要更多的灵感，看看这些年来发布的其他漂浮的水、T2、喷泉和 T3 项目。

 [https://www.youtube.com/embed/ambI007EriU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ambI007EriU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

