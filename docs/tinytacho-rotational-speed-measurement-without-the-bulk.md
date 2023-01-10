# TinyTacho:无主体的转速测量

> 原文：<https://hackaday.com/2020/11/26/tinytacho-rotational-speed-measurement-without-the-bulk/>

电子转速表是一种非常简单的设备，它可以检测旋转物体上白点的光反射，并随着时间的推移进行计数，测量每分钟的转数(RPM)。这是一项源于模拟电子技术的技术，其中产生的脉冲将馈入电荷泵，这是一项非常适合微控制器进行计数的任务。但是你需要一个会唱歌会跳舞的芯片来完成这项工作吗？斯蒂芬·瓦格纳以谦逊的态度做到了这一点。

他的 TinyTacho 是一个小 PCB，一端有一个红外 LED 和光电二极管，前面有一个小有机发光二极管显示器，后面有一个硬币电池架。电子设备可能极其简单，但在 ATtiny 有限的资源范围内，仍需付出相当大的努力。计算转数很容易，但是芯片没有自己的 I ² C 接口，需要一些位碰撞代码。你可以在 GitHub 库中找到你需要的所有设计文件和软件[，他上传了一段设备运行的视频，你可以在视频下方看到。](https://github.com/wagiminator/ATtiny13-TinyTacho)

转速表在这一带是一个很受欢迎的项目，多年来我们已经推出了很多。也许指导读者的最好地方不是另一个项目，而是如何使用转速表。

 [https://www.youtube.com/embed/Iz7LjheLYKo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Iz7LjheLYKo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

