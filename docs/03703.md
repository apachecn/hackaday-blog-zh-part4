# ESP8266 发声机器远程安抚婴儿

> 原文：<https://hackaday.com/2019/07/28/esp8266-sound-machine-soothes-baby-remotely/>

[Zack]很难让他六个月大的孩子一觉睡到天亮。那是在他发现 YouTube 上的“嘘”视频之前。这就是它们听起来的样子:八个小时的某人对着麦克风发出的白噪音。他在婴儿室里把手机放在充电器上，让其中一部手机通宵播放。但是电话不可靠。它会锁死，或者完全崩溃，使婴儿的痛苦更严重。

为了恢复家中的宁静，他建造了一台声音机器，既简化又增强了白噪音的音量。它使用一个 ESP8266 和一个 [DFPlayer Mini](https://wiki.dfrobot.com/DFPlayer_Mini_SKU_DFR0299) 来循环播放一个单独的 MP3 文件 shh-video audio，并通过一个小扬声器播放。通过将机器与家庭助理集成，他能够在婴儿睡觉时远程触发声音。 [ESP Home](https://esphome.io/index.html) 没有 DFPlayer 的模块，但是【扎克】做了一个，他很乐意分享。

如果你陷入了早期为人父母的困境，这是一个很好的简单的解决方案。DFPlayer 完成从 SD 卡读取数据并将信号转换为模拟信号以供扬声器输出的所有工作，因此没有必要弄脏您的手，浪费宝贵的睡眠或儿童玩耍时间。

一旦孩子开始蹒跚走出婴儿期，[扎克]可以求助于[基于 ESP8266 的环境照明](https://hackaday.com/2018/06/07/ambient-lighting-for-baby-with-the-esp8266/)来帮助建立睡眠和醒来时间之间的差异。