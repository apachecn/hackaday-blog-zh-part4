# 旧手机成为 MIDI 控制器

> 原文：<https://hackaday.com/2021/06/09/old-phone-becomes-midi-controller/>

MIDI 控制器有各种形状和大小。基于键盘或按钮矩阵的商业产品很受欢迎，但没有什么能阻止你根据自己的喜好创造出自己的作品。[凯文]已经做到了，把一部旧电话变成一个工作的 MIDI 设备。

问题中的电话是 Doro X20 有线固定电话。(凯文的)需求过剩使得黑客攻击时机成熟。一个树莓派微型计算机被连接到手机的键盘上，用钢锯将其变细，以便能够整齐地放入原来的外壳中。然后，很简单的事情就是编写一些代码来读取按钮，并通过 Pico 的串行输出输出 MIDI 数据。

后来，[Kevin]将这一设计带入了现代世界，[使用 Pico 的板载 USB 硬件设置它与 USB MIDI 对话。这使得在电脑上使用它变得轻而易举，并让[Kevin]使用手机控制器控制 DAW。](https://diyelectromusic.wordpress.com/2021/04/05/vintage-phone-usb-midi-controller/)

这是一个有趣的构建，它展示了如何使用烙铁、一些按钮和现代微控制器轻松构建自己的 MIDI 硬件。从那里，天空才是真正的极限。无论你是喜欢[大旋钮](https://hackaday.com/2019/12/09/diy-music-controllers-for-raging-with-machines/)、[易弹](https://hackaday.com/2020/10/10/starshine-is-a-midi-controller-for-the-musically-shy/)，还是有自己的个人品味，都可以打造自己喜欢的适合自己的风格。当你这样做的时候，[给我们写信！](http://hackaday.com/submit-a-tip)休息后的视频。

 [https://www.youtube.com/embed/oejkhRmy9j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=37&wmode=transparent](https://www.youtube.com/embed/oejkhRmy9j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=37&wmode=transparent)

