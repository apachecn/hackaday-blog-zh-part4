# Notkia:构建一个开放的、基于 Linux 的数字平板手机

> 原文：<https://hackaday.com/2022/06/18/notkia-building-an-open-and-linux-powered-numpad-phone/>

我们许多黑客都渴望拥有带数字小键盘的手机。我们也有一个共同的理解，现在，这样的手机必须是开放的和 Linux 驱动的。今天的项目， [Notkia，](https://hackaday.io/project/185645-notkia)是制造符合我们要求的键盘手机的最有前途和最现实的努力。Notkia 是诺基亚 168x 系列手机的替代板，配备了改进的显示屏、USB-C、WiFi、蓝牙和 LoRa ——[ sudo maker]的[Reimu NotMoe]告诉我们[这个项目的广泛故事。](https://hackaday.io/project/185645-notkia/details)

Notkia 的努力始于两年前，因为[灵梦]越来越不喜欢现代智能手机——这是每个黑客都熟悉的。她详细叙述了 Android 手机侵犯隐私和黑客攻击限制的第一手经验，这使她坚信当今可用的手机存在根本问题。从头开始构建新硬件似乎是前进的方向。两年后，这正是我们得到的！

当谈到这款手机的物理外形时，重复使用现有的外壳是最经济的解决方案，Hackaday.io 页面描述了寻找合适外壳的旅程。最终，诺基亚 1680 系列手机被证明是完美的候选产品。这些手机很小，很容易拿在手中，外壳内部有足够的空间，而且现在很容易买到替换的外壳和电池——至少是你可能想要的那种手机。

这种替代主板包含相当多的功能。陈旧落后的 128×160 显示屏被可视面积为 220×280 像素的 IPS 屏幕所取代。他们找不到足够小的 4G 模块，但 Notkia 使用了一个 [LoRa 模块](https://twitter.com/ReimuNotMoe/status/1535706889425543168)来代替。有 [WiFi](https://twitter.com/ReimuNotMoe/status/1537035854681559041) 、[蓝牙](https://twitter.com/ReimuNotMoe/status/1537339414493294594)、雅马哈 MA-3 音乐合成器、用于充电和 OtG 的 USB Type-C 端口、RGB LED、SHT20 传感器，1680 版本支持 5MP 摄像头。这样的功能集使得 Notkia 生产一款可用手机的雄心勃勃的目标非常容易实现。

![](img/12beab4900a9d67934fa65253b1da55b.png)就像[我们报道的 X1501 项目一样，](https://hackaday.com/2022/06/05/new-part-day-x1501-makes-for-a-tiny-and-open-linux-som/)Ingenic x 1000 CPU 有免费提供的开放数据表。这款手机已经运行 Linux 从这里开始，软件支持工作正在进行，有一个简单的途径来实现全磁盘加密等功能。有一系列的演示:[键盘输入](https://twitter.com/ReimuNotMoe/status/1532632301074452480)， [LCD 背光调光，](https://twitter.com/ClassicOldSong/status/1533042915261358081) LVGL [音乐播放器，](https://twitter.com/ReimuNotMoe/status/1527010359348973568)当然还有[坏苹果](https://twitter.com/ClassicOldSong/status/1531946930669924352)——通过 USB-OtG 用 USB 音频适配器。[进行了跌落试验，](https://twitter.com/ReimuNotMoe/status/1536427686939176960)也进行了跌落试验。有兴趣买一块 Notkia 板吗？[灵梦]的目标是在众筹上推出它——在那之前，有一个电子邮件注册列表[来获取项目更新。如果你有兴趣帮助一个软件优先级，似乎也有可能提前介入。](https://mailchi.mp/803fa91c2178/notkia-updates)

看到一款 Linux 手机有如此大的生产潜力，令人欣慰。重新利用旧手机外壳以获得可行的功能手机的项目不时出现。这些[诺基亚 3310](https://hackaday.com/2018/07/22/ihc-badge-its-not-quite-a-nokia/) 和 [3210 重建](https://hackaday.com/2017/09/12/hackaday-prize-entry-retrofit-a-nokia/)有一些好主意可以借鉴， [WiPhone](https://hackaday.com/2019/04/03/phone-for-hackers-launches-a-crowdfunding-campaign/) 已经成功地在 ESP32 前端交付了 SIP 呼叫。如果你想进行更多的 DIY，你可以尝试[在几块电路板之间夹一个 Pi Zero，](https://hackaday.com/2017/09/19/hackaday-prize-entry-the-50-raspberry-pi-smartphone/)或者用 PCB 外壳制作一个 [ATMega 供电的手机！](https://hackaday.com/2016/11/28/building-beautiful-cell-phones-out-of-fr4/)