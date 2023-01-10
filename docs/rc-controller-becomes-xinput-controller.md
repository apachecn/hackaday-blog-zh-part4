# RC 控制器变成 XInput 控制器

> 原文：<https://hackaday.com/2019/01/05/rc-controller-becomes-xinput-controller/>

XInput 是应用程序用来与 Windows 的 Xbox 360 控制器交互的 API。360 控制器在某种程度上成为了“标准”的 PC 游戏手柄，因此许多游戏和应用程序都支持 XInput 标准。

[James]正在设计一个机器人竞赛的参赛作品，并且想要一个更适合他们体型的控制器用于他们的电脑。他们拿了一个 RC 控制器，并将其转换为与 XInput 一起工作。

问题中的控制器是 JJRC Q35-01，这是一种触发型 RC 控制器，售价不到 20 美元。转换执行得很巧妙，原来的 STM 微控制器从电路板上移除，PCB 走线连接到 Teensy 3.5，后者接管整个过程。

转换是非常完整的，团队不仅仅停留在阅读按钮和转向电位计。使用 USB 逻辑分析仪来确定如何控制 LCD，并实施校准模式以防万一。

[【James】已经在 Github](https://github.com/jcorcoran/jjrc_xinput_controller) 上分享了这项工作，所以对于一般的开发者来说，它是可复制的。我们已经在这个领域看到了大量的构建，[，就像来自【电子人】](https://hackaday.com/2018/10/02/a-new-tilt-on-rc-car-controllers/)的这个倾斜控制器。休息后的视频。

 [https://www.youtube.com/embed/4KyOlYCAPlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4KyOlYCAPlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

