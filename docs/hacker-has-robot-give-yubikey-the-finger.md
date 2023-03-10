# 黑客让机器人给了 Yubikey 手指

> 原文：<https://hackaday.com/2020/10/06/hacker-has-robot-give-yubikey-the-finger/>

[Bertrand Fan]并不喜欢普通 Yubikey 上的小而难操作的按钮。在 2020 年发生之前，[Bert]将这个小的 2FA nano-donglette 插入他们笔记本电脑侧面的一个备用 USB 端口，这样无论笔记本电脑走到哪里，它都是可用的。现在在家工作已经成为常态，[Bert]把笔记本电脑放在一边，放在够不着的地方。

一根 USB-C 延长线当然让它更容易接近，但对这个小按钮的启动失败率没有任何帮助。厌倦了不便和寻找一个锁定项目，[【Bert】决定制造一个按钮式机器人手指，由他们时髦的 TKL 键盘](https://bert.org/2020/10/01/pressing-yubikeys/)上的备用键驱动。

它在 Wemos D1 mini 上运行，使用一个小型步进电机推动 3D 打印的手指沿着齿条齿轮传动装置移动。由于 Yubikey 需要电容触摸，所以[Bert]在接地的指尖上加了一个螺丝。现在[伯特]所要做的就是按下一个明显更酷的键，让手指为他按下按钮。休息之后，请观看简短的演示。

如果这个安全漏洞让你不舒服，[也许这个 2FA 发射控制台更合你意](https://hackaday.com/2020/03/26/launch-console-delivers-enjoyment-to-software-deployment/)。正如我们最近看到的，如果你不喜欢 Yubikeys 的成本，[你可以用蓝色药丸](https://hackaday.com/2020/06/10/stm32-blue-pill-turned-gpg-security-token/)滚动自己的 2FA 设备。

 <https://bert.org/assets/posts/yubikey/full.webm?_=1>

[https://bert.org/assets/posts/yubikey/full.webm](https://bert.org/assets/posts/yubikey/full.webm)