# 低下身子，用这个无线“盖革计数器”掩护

> 原文：<https://hackaday.com/2019/04/08/duck-and-cover-with-this-wifi-geiger-counter/>

也许没有比盖革计数器疯狂的滴答声更容易辨认的声音了。不是因为这是一个后世界末日的世界，每个人都亲自熟悉这些设备的操作，而是因为这是许多电影、电视节目和视频游戏中使用的常见效果。如果有人听到这种声音，即使它在上下文中没有意义，他们也知道事情要变得严重了。

[![](img/b95cb72497aa9cd3a042310ec66fcb82.png)](https://hackaday.com/wp-content/uploads/2019/04/espclicker_detail.jpg) 利用这一现象，[【安东·海岱】已经拼凑出一个快速的黑客技术，将 ESP8266 变成 WiFi 的“盖革计数器”](https://github.com/anha1/esp8266-wifi-fake-geiger-counter)。这个小工具不是检测辐射，而是拾取附近最强的 WiFi 信号，并根据信号强度开始点击。随着信号变强，咔嗒声也变强。虽然主要是一个新奇的东西，但这是一个有趣的想法，可能对猎狐等事情很有用。

硬件非常简单，只是一个基本的蜂鸣器，连接到 NodeMCU 开发板的一个数字引脚上。这个项目更多的是一个概念验证，但如果它被进一步开发，那么看到电子设备被放置到一个旧的民防盖革计数器的 3D 打印副本中会很有趣。甚至可能集成一个模拟仪表，可以根据信号强度来回跳动。

软件方面，可以选择锁定一个网络 SSID，或者允许设备找到该区域最强的网络。即使你不在市场上寻找一个啁啾 WiFi 探测器，该代码也是一个很好的例子，说明如何检测信号 RSSI 并据此采取行动；这是一个巧妙的技巧，在未来的项目中可能会派上用场。

如果你对真实的东西更感兴趣，我们在档案馆里有很多 DIY 盖革计数器供你查看。从可以安装在 9V 电池顶部的小型建筑到带有触摸屏界面的高科技固态版本，如果你想在下一次穿越切尔诺贝利禁区之前装备好自己，你应该会有很多灵感。

 [https://www.youtube.com/embed/JckX73Gao08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JckX73Gao08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

