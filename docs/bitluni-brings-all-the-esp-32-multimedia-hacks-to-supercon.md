# Bitluni 将所有 ESP-32 多媒体技术带到了 Supercon

> 原文：<https://hackaday.com/2020/02/24/bitluni-brings-all-the-esp-32-multimedia-hacks-to-supercon/>

在所有我期待在 Supercon 见到的人当中，除了那些与我共事了五年却从未谋面的普通同事，还有一个来自德国的名叫马蒂亚斯·巴尔维尔兹的家伙。这个名字可能听起来没什么印象，但他肯定会为黑客读者所熟悉，因为 Bitluni 是 YouTube 上“Bitluni 的实验室”的一张面孔，有时很傻，但总是很有趣，很有启发性。

这些年来，我一直在报道 Bitluni 的许多 ESP32 黑客活动，并与他建立了通信联系，就我开始但不知何故从未完成的许多项目交换想法并征求建议。幸运的是，Bitluni 在跟进方面比我好得多，在派对搬到隔壁进行徽章黑客演示之前，他将这种广度和深度的经验带到了 2019 年超级会议的最后一次演讲的设计实验室阶段。

在他的演讲和许多实验中，Bitluni 为 ESP32 成为音频和视频应用的完美芯片提供了一个很好的例子。Espressif 芯片拥有双核微处理器(如果算上超低功耗的协处理器，则为三个)和 520 kiB 的 SRAM，确实是一个非凡的怪兽，但正如 Bitluni 指出的那样，它的引擎盖下还有更多，其中大部分他已经学会在他的项目中很好地使用。

以这个 ESP-32 X-Y 显示器为例，这是 2017 年引起我们注意的第一个 Bitluni 版本。即使在那时，比特鲁尼也在拓展芯片的功能；当他发现板载 DAC 的速度不够快，无法满足他的需求时，他研究了 I S 代码，发现可以将速度提高 27 倍。他将新学到的 DAC 技能用于使用 R-2R 梯形电阻的[AM 无线电发射机](https://hackaday.com/2018/01/28/esp32-makes-for-worlds-worst-radio-station/)和[复合视频编码器](https://hackaday.com/2018/02/22/software-defined-television-on-an-esp32/)，最终[VGA 显示器](https://hackaday.com/2019/02/05/back-to-video-basics-with-an-esp32-vga-display/)。ESP-32 上的 HDMI 显示似乎仍然遥不可及，但我们怀疑他无论如何都会继续努力。

本质上，将 ESP-32 的一个内核转变为 GPU，留下另一个内核用于其他任务，使 SOC 成为一个完美的低端游戏主机。这种合成视频和单声道空间拍摄利用了他对 ESP-32 的所有了解，实际上是早期 10 人游戏控制台的简化[，旨在娱乐制造商博览会上的人群。](https://hackaday.com/2019/09/11/10-way-game-console-lets-everyone-play/)

可悲的是，没有太多的硬件与 Bitluni 一起前往 Supercon，但你只能带这么多。对他来说，来分享他来之不易的 ESP-32 智慧以及他的机智已经足够了。

 [https://www.youtube.com/embed/AZYjIPrQe7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AZYjIPrQe7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

