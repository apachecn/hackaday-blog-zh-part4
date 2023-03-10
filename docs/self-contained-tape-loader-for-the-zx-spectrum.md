# 用于 ZX 光谱的独立磁带加载器

> 原文：<https://hackaday.com/2020/08/07/self-contained-tape-loader-for-the-zx-spectrum/>

虽然如今我们有幸拥有永不停机的互联网连接和云服务，但在过去，软件是在物理介质上交付的。一些最受诟病的媒体是数据磁带，因其缓慢的加载时间而备受指责。然而，这种有形性确实给了他们一些魅力，[和【JamHamster】决定用他的独立虚拟磁带加载器来重现这一点。](https://twitter.com/RealJamHamster/status/1291376935252172806)

加载程序的核心是一个 TZXDuino，一个与 Arduitape 相关的频谱磁带仿真器。它使用 Arduino Nano 来存储磁带数据文件，并重放它们以在 retro 平台上加载软件。[JamHamster]将它与盒式磁带外壳和盒式音频适配器的磁头结合起来，制作了一个数字磁带模拟器。TZXDuino 在外壳中塞满了一些模块，包括一个传感器，它可以检测到播放头在磁带内移动以触发播放。这源于一个更早的模块做了同样的事情，[只是没有板载电池。](https://www.youtube.com/watch?v=dMpGGf-YUzU)

这是一个干净利落的方法，也是在你的复古电脑上加载游戏的一个非常酷的方式。由于更广泛的 Arduitape 项目支持各种计算机，有了固件闪存，它应该也能与其他系统兼容。由于消除了使用现在已经过时的格式的麻烦，磁带模拟器在社区中很受欢迎。休息后的视频。

 [https://www.youtube.com/embed/dMpGGf-YUzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dMpGGf-YUzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

