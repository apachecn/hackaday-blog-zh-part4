# LED 艺术以非常缓慢的动作展现自己

> 原文：<https://hackaday.com/2020/09/15/led-art-reveals-itself-in-very-slow-motion/>

你看过的每一部电影或视频都是一种心理把戏，是一种基于每秒钟向你的眼睛闪现 24 到 30 个略有不同的图像的连续运动的光学幻觉。你两耳之间的湿件无法单独处理所有信息，所以它说服自己你看到的是平稳的运动。

但是如果你让时间变慢:每 100 秒或者每 1000 秒拨回一帧呢？这就是这个慢动作 LED 艺术展示背后的理念被恰当地称为“连续体”这是[路易斯·博多因]的作品，它的灵感来自于最初的慢动作电影播放器的[和我们最近更新的](https://hackaday.com/2018/12/30/the-very-slow-movie-player-does-it-with-e-ink/)的[。虽然这些播放器采用了电子纸显示器来显示逼真的图像，但“Continuum”采用了低分辨率的方法。显示屏由~~四个~~九个 HUB75 32×32 RGB LED 显示屏组成，每个显示屏间距为 5 毫米。最终的 96×96 像素显示屏非常适合宜家 RIBBA 相框。](https://hackaday.com/2020/08/23/e-paper-display-shows-movies-very-very-slowly/)

显示屏由一个 Teensy 4 和[Louis]定制设计的 [SmartLED 护罩](https://hackaday.io/project/174817-smartled-shield-for-teensy-4)驱动，该护罩直接插入 HUB75s。框架的后部用 APA102 LED 条镶边，形成流光溢彩的效果，显示器的前面有一个磨砂丙烯酸漫射器。它被配置为以任何速度显示动画 gif，从最初的每秒 ~~1 帧~~到每秒 1000 秒~~帧~~的速度，后者导致图像看起来是静态的，除非你稍后重新访问它。【Louis】充分利用了 Teensy 的处理能力，在每一对帧之间平滑过渡，整体效果相当奇妙。下面的视频尽可能地捕捉到了它，但我们认为这是最好亲自看到的东西。

[https://player.vimeo.com/video/452369443](https://player.vimeo.com/video/452369443)