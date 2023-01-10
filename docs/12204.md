# 谷歌的 T-Rex 游戏移植到了 ESP32

> 原文：<https://hackaday.com/2021/12/15/googles-t-rex-game-ported-to-the-esp32/>

当互联网连接中断时，大多数 Chrome 用户都会遇到一个整洁的小复活节彩蛋——一个名为“T-Rex”的游戏，其中一只恐龙必须跳过 cactii。无论这在进化时间表方面是否准确，这都有点有趣，Volos 项目的教育家 T2 决定将这款游戏移植到 ESP32 上。

这款游戏在 LILYGO TTGO T-Display 开发板上运行，该开发板将强大的微控制器与 1.14 英寸彩色液晶显示器配对。他的克隆版在按下触摸按钮进入游戏之前，从谷歌 Chrome 中真实地复制了“禁止上网”的页面。

该游戏使用基于精灵的引擎构建，这使得游戏在屏幕上的闪烁最小化。透明度是为了防止精灵不必要地遮挡其他屏幕元素。[Danko]还没有发布一个关于在 ESP32 上使用精灵的完整教程，但是[代码可以让](https://github.com/VolosR/TRexTTGOdisplay)自己消化。

这不是我们第一次看到[Danko]的 [ESP32 游戏，](https://hackaday.com/2020/10/19/ttgo-esp32-module-with-multiple-personalities/)因为他这些年已经开发了一些。其他人甚至为平台编写了 8 位仿真器[。](https://hackaday.com/2020/06/09/run-your-favorite-8-bit-games-on-an-esp32/)休息后的视频。

 [https://www.youtube.com/embed/ilC4LIQZ77g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ilC4LIQZ77g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

