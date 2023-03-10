# PSP 转向机器人远程定制软件

> 原文：<https://hackaday.com/2022/05/24/psp-turned-robot-remote-with-custom-software/>

毫无疑问，索尼的 PlayStation Portable (PSP)在 2004 年发布时是一款令人印象深刻的硬件，但尽管它有着神奇的技术，却无法撼动任天堂在手持设备市场上的霸主地位。也许这解释了为什么我们仍然看到如此多的怀旧黑客攻击任天堂的 Game Boy 和双屏(DS)系统，而 PSP 黑客往往很少。

但是看着像这样的项目[将 PSP 变成一个有能力的机器人控制器](https://www.youtube.com/watch?v=do1674d6Rbo)(视频，嵌入下面)我们不禁想知道这个社区是否被遗漏了。得益于该系统的开源软件开发包，[iketsj]能够编写一个 WiFi 控制器程序，该程序可以在任何带有兼容家酿固件的 PSP 上运行。

[![](img/5bae53145971dcd0e615b17de7671583.png)](https://hackaday.com/wp-content/uploads/2022/05/pspbot_detail.jpg) 方程式的另一边是一个由 ESP8266 驱动的简单机器人。为了控制机器人，用户将他们的手持设备连接到 MCU 提供的 WiFi 网络，并从主菜单启动控制器应用程序。这一切都非常巧妙，事实上你不需要对 PSP 的硬件做任何修改，这是一个巨大的优势。从休息后的视频中，我们得到的印象是，远程软件在其当前形式下非常简单，但我们认为唯一真正的限制是，你在为一个以今天的标准来看相当资源受限的系统编写 C 代码方面做得有多好。我们希望看到宽屏显示器点亮，从机器人的角度展示第一人称视频。

这些年来我们看到的许多 PSP 黑客[都是关于重新利用硬件](https://hackaday.com/2015/06/03/psp-media-player-for-the-home-workshop/)，或者在某些情况下，用树莓味的东西替换系统内部的[。这些项目肯定以它们自己的方式很有趣，但是我们真的很喜欢这样的想法，即仅仅通过为它编写一些定制代码，就能够将一个主要是股票的系统推向一个新的角色。](https://hackaday.com/2018/10/21/stock-looking-psp-hides-a-raspberry-pi-zero/)

 [https://www.youtube.com/embed/do1674d6Rbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/do1674d6Rbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

