# 基于云的雅达利游戏

> 原文：<https://hackaday.com/2021/07/29/cloud-based-atari-gaming/>

虽然 Google Stadia 可能是云游戏领域中最新最棒的，但还有很多其他方式来体验这种新的游戏风格，尤其是如果你愿意有点复古的话。例如，这个项目[将 Atari 2600 带入云](https://www.mikekohn.net/software/cloudtari.php)以获得完全托管在服务器上的近乎完整的游戏体验，包括视频渲染。

[Michael Kohn]创建这个项目主要是为了更好地熟悉 Kubernetes，这是一个开源软件，有助于自动化和部署基于容器的应用程序。该设置在两个 Raspberry Pi 4s 上运行，可以通过将浏览器指向其网络上的正确 IP 地址或通过 VNC 连接到它们来访问。从那里，模拟器运行一个名为空间复仇的特定游戏，选择它是因为它的内存需求和它没有版权的阻碍。有一些限制，因为他使用的模拟器不能实现所有的 Atari 控件，并且声音不能通过远程桌面设置获得，但它仍然令人印象深刻

[Michael]也掩饰了这一部分，但 Atari 模拟器是他“尽快”编写的，因此他可以专注于 Kubernetes 的设置。这本身就令人印象深刻，当然他还在 GitHub 页面上展示了如何建立基于云的系统。他还认为像这样的系统也有运行 NES 系统的潜力。不过，如果你在寻找更现代一点的东西，也可以用任天堂 Switch 建立一个[基于云的游戏系统。](https://hackaday.com/2021/01/05/raspberry-pi-4-brings-cloud-gaming-to-nintendo-switch/)

 [https://www.youtube.com/embed/4xJULDDAJs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4xJULDDAJs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

