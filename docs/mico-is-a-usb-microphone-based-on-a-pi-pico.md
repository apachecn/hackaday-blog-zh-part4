# Mico 是基于 Pi Pico 的 USB 麦克风

> 原文：<https://hackaday.com/2021/12/25/mico-is-a-usb-microphone-based-on-a-pi-pico/>

当[Mahesh Venkitachalam]在 Raspberry Pi 上试验机器学习音频应用程序时，他发现自己在寻找一个简单的 USB 麦克风。便宜的很容易找到，但是音质和方向性还有待改进。一个大的、录音室质量的麦克风就太大了，所以[Mahesh]决定简单地制造出所需要的东西:一个紧凑而高质量的 USB 麦克风，他称之为 Mico。

传感器件是一个 MEMS 麦克风，输出脉冲密度调制(PDM)信号。有芯片可以直接将这样的麦克风连接到 USB 端口，但[Mahesh]发现很难使用它们，因此决定使用他已经知道的东西:Raspberry Pi Pico 平台。幸运的是，有人已经想出了如何读出麦克风并把 USB 设备呈现给 PC，所以所有需要做的就是把所有的比特组合成一个方便的形状因子。

Pico 平台的优点在于它的主控制器芯片 RP2040 是一个独立的组件。[Mahesh]设计了一个光滑的小 PCB，用于容纳 RP2040 以及 MEMS 麦克风和 USB 连接器。最终的结果看起来足够整洁，它可能来自一个大规模生产的小发明。这些通常没有完整的原理图和源代码，但 Mico 有:任何东西都可以在 GitHub 页面上找到，任何人都可以重复使用和改进。

你可以在下面嵌入的视频中自己判断音质。如果你喜欢 DIY USB 麦克风，你很幸运:我们已经推出了一款基于 STM32 的[，以及一款录音室品质麦克风](https://hackaday.com/2021/06/02/diy-usb-microphone-seems-overkill-is-surprisingly-in-depth/)的[精美再现。](https://hackaday.com/2021/11/06/cheap-diy-mic-sounds-and-looks-damn-good/)

 [https://www.youtube.com/embed/G_soM9alIGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G_soM9alIGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

