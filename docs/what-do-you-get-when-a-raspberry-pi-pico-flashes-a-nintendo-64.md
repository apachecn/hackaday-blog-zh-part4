# 当树莓派微微闪现任天堂 64 时，你会得到什么

> 原文：<https://hackaday.com/2022/06/24/what-do-you-get-when-a-raspberry-pi-pico-flashes-a-nintendo-64/>

大约四分之一世纪前，当任天堂 64 第一次出现在街头时，这个名字中的 64 不是指板上的技术，而是指墨盒的过高成本。不管真相是什么，它现在已经完全被康拉德·贝克曼(Konrad Beckmann)用他的由树莓皮微型电脑(Raspberry Pi Pico)驱动的[任天堂 64 flash cart](https://twitter.com/kbeckmann/status/1539738410063208454)([Nitter Link](https://nitter.net/kbeckmann/status/1539738410063208454))彻底埋葬了。

原理图出奇的简单，Pico 做了所有需要的事情来连接 N64 和 SD 卡以保存软件。这个巧妙的工作是由 RP2040 固件完成的，可以在该项目的 GitHub 库的[的“开发”分支中找到它和硬件细节。虽然最早的版本是带有大量跳线的 Raspberry Pi Pico，但更精致的版本专注于定制的 PCB 和裸露的 RP2040 芯片。](https://github.com/kbeckmann/PicoCart64)

也许 N64 多年来没有得到应有的关注，因为它被最初的 PlayStation 等竞争对手掩盖了，但像这样的项目提醒我们，任天堂 90 年代的旗舰产品仍然有生命力。说到这里，如果你是索尼团队的一员，但仍然想使用你的 Pi Pico，看看我们最近报道的这个 [DIY PlayStation 存储卡](https://hackaday.com/2022/06/13/raspberry-pi-pico-replaces-playstation-memory-card/)。