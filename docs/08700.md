# SNES 射线追踪

> 原文：<https://hackaday.com/2020/12/17/a-snes-ray-tracing/>

任天堂为了让其慢慢老化的 SNES 游戏机在新的竞争中保持新鲜而使用的一个著名技巧是生产新游戏，在游戏盒中加入额外的支持芯片，以推出迄今为止不可想象的性能。像著名的 SuperFX 这样的芯片为我们提供了 3D 多边形图形，但即使更快的平台也需要几年才能实现实时光线跟踪。任天堂可能没有做到这一点，但在 2020 年 [[Ben Carter]在他的工作台上有一个 SNES 渲染一个复杂的 3D 光线追踪世界](https://www.shironekolabs.com/posts/superrt/)。

光线跟踪指的是通过跟踪朝向每个像素的光线，使用精确的照明渲染场景的实践。它可以达到甚至接近照片真实感的效果，但对于任何计算机来说，它仍然是一项计算量非常大的工作。为了用 SNES 做到这一点，他没有求助于现代计算机，如基于树莓派的优秀的 [NES 末日卡带](https://hackaday.com/2019/08/29/how-to-play-doom-and-more-on-an-nes/)，而是试图创造一些可能会在 20 世纪 90 年代为任天堂定制芯片增光添彩的东西。该工具可能是一个完全现代的 DE10-Nano FPGA 开发板，但它所实现的可能是 20 世纪 90 年代规格的 ASIC。其中有三个光线跟踪核心完成这项工作，但最终的渲染是由 SNES 自己处理的。在 200 x 160 像素和 256 色的情况下，它不是一个图形发电站，但 30 fps 的最大帧速率使它在一天中不会懒散。广告下方的视频提供了额外的细节。

也许一个意想不到的场景在于它的时代。它来自一个棋盘地板、镜像球和湛蓝天空看起来如此未来的时代，并且就在像*玩具总动员*这样的游戏重新定义公众对 3D 渲染的期望之前。如果任天堂使用这样的芯片制作了一款光线追踪 SNES 游戏，这无疑将是那十年游戏的决定性时刻。

 [https://www.youtube.com/embed/2jee4tlakqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2jee4tlakqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[马克]的提示。