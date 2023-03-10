# 通过 Firmata 将您的 C64 与 Arduinos 连接

> 原文：<https://hackaday.com/2019/04/09/interface-your-c64-with-arduinos-through-firmata/>

微控制器很酷，但有时它们提供的用户界面选项令人失望。有问题的平台可能没有足够的马力来驱动一个像样的屏幕，而且出于安全性或复杂性的原因，web 界面通常是不可取的。有时候你只是需要一个好的芯片和电脑之间的软件接口。Firmata 是一种专门为此而设计的协议，而[[nano lite]已经将其引入 Commodore 64。](https://github.com/nanoflite/C64_Firmata)

这是一个有趣的项目，它允许人们使用 C64 迷人的复古图形与基于 Arduino 的项目进行交互。通过用户端口的连接速度是 2400bps，对于大多数 UI 应用程序来说已经足够快了。[nano lite]展示了与 Arduino Uno 和 Grove shield 的接口。C64 能够显示 LED、继电器和伺服输出的状态，以及读取 Arduino 的按钮和电位计输入。

这是将 Commodore 64 集成到微控制器设置中的一个很好的方式，无需重新发明轮子。我们认为它将成为家庭自动化系统或类似建筑的一个令人敬畏的老式界面。如果你感兴趣，但你没有自己的 C64 可以玩，不要害怕—[你可以做一个新的](https://hackaday.com/2019/03/12/its-raining-brand-new-commodore-64s/)。