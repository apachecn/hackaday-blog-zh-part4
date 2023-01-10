# 从 rom 创建视频

> 原文：<https://hackaday.com/2021/09/10/creating-video-from-a-rom/>

我们已经习惯了带显示屏的电脑，但我们中有多少人创造了直接驱动电脑的电路？当然，我们已经在微控制器上编写了 SPI 显示驱动程序，但是还要创建硬件来生成可用的视频信号吗？那就有点难了。[Jdh]尝试了一下，[用 TTL 显卡](https://www.youtube.com/watch?v=OW1EmG7b4DU)。

在这种情况下，它不是一个卡，而是一组试验板，但所有的逻辑都是为了产生同步所需的复杂视频时序阵列，并以正确的电压电平顺序输出位给模拟监视器。值得指出的是，这不是一个复合视频信号，因为它是单色的，没有副载波。

最后，他遇到了问题，他的 ROM 对于像素速率来说不够快，因此图像有伪像，但它至少在屏幕上产生了可识别和可读的东西。视频行业的老手可能会指出，当涉及到精确的定时和行数时，模拟电视有点宽容，所以电路很可能被简化，并且牺牲一些分辨率可能会解决 ROM 速度问题。但这是一件令人印象深刻的作品，任何对视频工作原理感兴趣的人都会特别感兴趣。

面包板上显卡的粉丝们也应该去看看[【Ben Eater 的】7400 系列显卡](https://hackaday.com/2019/07/07/low-res-video-card-is-still-amazing-since-its-made-out-of-logic-chips/)。

 [https://www.youtube.com/embed/OW1EmG7b4DU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OW1EmG7b4DU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。