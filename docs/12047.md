# 辅助技术和视频游戏

> 原文：<https://hackaday.com/2021/12/07/assistive-tech-and-video-games/>

辅助技术在 Hackaday 上有很大的影响力，这个黑客非常有趣。[kerchoo_22]正在研究一款[免提视频游戏控制器，这是她工程课](https://www.instructables.com/Arduino-Leonardo-Game-Controller-for-Quadriplegics/)的最后一个项目，我们认为这值得分享。

电路的基本前提非常简单。她用纸板、胶带和铝箔制成的导电板 DIY 了几个接触开关。开关的输出由 Arduino Leonardo 上的模拟输入引脚读取。当开关关闭时，使用 1 兆欧电阻将模拟输入引脚拉高。但是，当用户将头撞在四个导电垫中的一个上时，开关接合，模拟输入引脚短路接地。

Arduino Leonardo 有一个本机 USB 端口，能够直接模拟键盘。每个导电垫被映射到对应于游戏中不同功能的不同按键。左，右，射，等等。这就是你想要的，不用手或控制器就能玩游戏！

现在，看起来好像[kerchoo_22]在头垫上放了适量的垫子，所以可能没有太多脑震荡的危险。无论哪种方式，你都不能太小心。