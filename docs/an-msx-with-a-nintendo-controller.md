# 带任天堂控制器的 MSX

> 原文：<https://hackaday.com/2019/08/12/an-msx-with-a-nintendo-controller/>

游戏机拥有者居住在他们自己的部落里，这取决于他们选择的制造商，所以两者经常不会相遇。但有时也会有一些假设的时刻，马里奥会不会通过 PlayStation 按钮更快地救出公主，或者刺猬索尼克会不会有一个任天堂控制器？[【Danjovic】正在寻找其中一个问题的答案](https://hackaday.io/project/167059-nsx-64)，任天堂 64 控制器和 MSX 硬件之间的接口，包括早期的世嘉游戏机。

在硬件方面，这是一个非常简单的设备，就像许多这样的项目一样，一个 Arduino Nano，一个电阻和几个插座。聪明的部分不在于它选择的微控制器，而是它使用 Nano-s 定时的方式，以确保按钮按下和游戏动作之间的最小延迟。细节在报道中，但简而言之，它利用了 MSX 人需要关注视频线路来为任何转换步骤争取额外的时间。

过去，MSX 电脑也曾因任天堂硬件而进行过控制器升级，我们曾见过 Wii 双节棍控制器与它们对话，还有 T2 和 SNES 的 T3。

标题图像:[mboverload] ( [公共域](https://commons.wikimedia.org/wiki/File:N64-controller-black.jpg))。