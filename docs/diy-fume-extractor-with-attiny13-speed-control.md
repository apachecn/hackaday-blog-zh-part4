# 带 13 速控制的 DIY 油烟机

> 原文：<https://hackaday.com/2022/09/04/diy-fume-extractor-with-attiny13-speed-control/>

实话实说，市面上的除焊烟器非常便宜，你可能不需要自己做一个。但它仍然是一个很好的起步项目，特别是如果你真的想展示你的创造者肌肉，就像[【Arnov Sharma】用这个整洁的构建](https://www.instructables.com/Fume-Extractor-1/)所做的那样。

[![](img/9c10922f91c63b4a3f8de3da066d31c9.png)](https://hackaday.com/wp-content/uploads/2022/08/atfume_detail.jpg) 现代硬件制造的所有标志都在这里展示——你有 3D 打印的外壳，从廉价玩具四轴飞行器中回收的电机，以及使用 ATtiny13 和 AO4406 MOSFET 实现 PWM 速度控制的定制 PCB。

第一次按下按钮会以最大速度启动电机，但继续按下按钮，电机的速度会下降，直到完全关闭。当油烟机连接到 USB 电源时，甚至还有一个 TP4056 充电控制器来为内部的 18650 电池充电。

是不是工程过度了？也许吧。但是像这样的项目是练习你技能的好机会，[无论是 PCB 设计](https://hackaday.com/2019/07/29/a-new-kicad-tutorial-hits-the-scene/)还是[创造定制的 3D 打印外壳](https://hackaday.com/2020/07/07/designing-3d-printed-enclosures-for-kicad-pcbs/)。在廉价的 32 位微控制器时代，看到黑客仍然不时地拖动 ATtiny 也令人耳目一新。

 [https://www.youtube.com/embed/X6-7Co_gba8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X6-7Co_gba8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Abe]的提示。