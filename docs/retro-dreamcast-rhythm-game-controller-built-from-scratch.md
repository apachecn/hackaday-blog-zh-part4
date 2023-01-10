# 复古 Dreamcast 节奏游戏控制器从头开始构建

> 原文：<https://hackaday.com/2021/02/23/retro-dreamcast-rhythm-game-controller-built-from-scratch/>

流行音乐是一种节奏游戏，多年来在街机和家用游戏机上都有发行。[查理·科尔]是 Dreamcast 版本[的粉丝，并决定使用新的热门产品树莓 Pi Pico](https://github.com/charcole/Dreamcast-PopnMusic)为游戏制作自己的控制器。

控制器本身是由多层激光切割的中密度纤维板制成，顶部是丙烯酸树脂，底部是软木，使其可以很好地放置在表面上。安装街机按钮来玩节奏游戏，模仿街机中看到的官方橱柜的设计。为了运行控制器，一台 Pico 投入使用，[查理]希望使用 Pico 的 PIO 硬件来轻松有效地与 Dreamcast 的 Maple 总线接口。在这个过程中有一些令人头痛的问题，它并没有完全达到预期，但是通过一些对双核的巧妙使用，[Charlie]能够让一切正常运行。

通常，这种老式游戏硬件很少，所以拥有自己开发的技能会很有用。我们以前也见过节奏游戏的硬件改造，[像这个重新设计的 DJ 英雄控制器](https://hackaday.com/2020/02/24/dj-hero-controller-gets-a-new-gig/)。休息后的视频。