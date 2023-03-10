# 惊人的开源四足动物能够动态运动

> 原文：<https://hackaday.com/2019/10/03/amazing-open-source-quadruped-capable-of-dynamic-motion/>

我们对[Josh Pieper]的四足机器人[mjbots quad A0](https://hackaday.io/project/167845-mjbots-quad-a0)了解得越多，我们就越对他一年来在设计上取得的进展感到惊讶。机器人的每个部分都值得有自己的文章:从经过大量修改的无刷电机(带有定制的行星齿轮)到仅为这个项目设计的定制电机驱动器。

[Josh]很早就意识到像[ODrive](https://hackaday.com/2016/05/23/hackaday-prize-entry-industrial-servo-control-on-the-cheap/)这样的现成组件不适合他的应用程序。因此，他设计了自己的主板，进行了四次修改，甚至对它进行了热量和循环测试。他最终得到了紧凑的 moteus 板。它可以输出 400 瓦的峰值功率，而其 3 兆位控制协议为实时动态控制留下了足够的带宽。

电机和变速箱也令人印象深刻。在他发明 8108 四轴直升机发动机之前，他进行了彻底的实验，并从其他项目中获得灵感。这种发动机被改造和升级得连他的母亲都认不出来了。这是所有包装成一个腿单位与三个自由度，甚至把最花哨的伺服为基础的四足动物自惭形秽。

最后，它被装进一个整洁的四条腿的机器人框架，带有电池和一个 Pi。你可以在这里或休息后获得机器人的视频摘要，我们建议阅读他的[博客](https://jpieper.com/)以获得更多图像和细节。

 [https://www.youtube.com/embed/aKOEN38e3hM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aKOEN38e3hM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

