# 互联网控制着这个怪物

> 原文：<https://hackaday.com/2020/01/06/the-internet-controls-this-monster/>

有什么比在互联网上释放一个怪物更糟糕的？允许互联网控制怪物！但这正是[8BitsAndAByte]所做的，[创造了一个互联网上任何人都可以控制的怪物](https://www.instructables.com/id/The-Internet-Monster)。幸运的是，这个怪物只会说话。

这是一个非常简单的项目，大部分零件都是现成的。硬件方面，怪物的身体是由一个塑料花盆制成的；它的嘴是一块木头，盖在花盆的顶部；它的眼睛是一个塑料球的两半，漆成白色，上面有一些虹膜的感觉。然后整个东西被一些蓝色的假毛皮覆盖。

就电子产品而言，一个树莓派正在发挥作用，处理文本到语音转换的是一顶 AIY 语音帽。一个伺服装置安装在花盆里，用来打开和关闭怪物的嘴。在软件方面，已经编写了一点 Python，它等待一点文本，将其发送到语音帽子的文本到语音模块，并移动伺服系统来打开和关闭嘴巴。可怕的部分是，将怪物连接到互联网是通过 [remo.tv](https://github.com/remotv/controller) 完成的，这是 GitHub 上托管的一些开源代码，专门用于通过互联网控制机器人。

这是一个简洁的小项目，非常简单，孩子们可以自己做一个。指令和 python 脚本在[可指令页面](https://www.instructables.com/id/The-Internet-Monster)上，你可以在 remo.tv 的[页面](https://remo.tv/join/lwppotv)上看到这个怪物的行动。也许【8BitsAndAByte】可以给这个怪物添加几个这些[互联网控制的机器人手臂](https://hackaday.com/2011/11/24/internet-controlled-robotic-arm-2/)来创造一个可以造成一些真正破坏的怪物！

 [https://www.youtube.com/embed/7WvK_5svj98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7WvK_5svj98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

