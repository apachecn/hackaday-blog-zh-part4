# Arduino 交通灯唱着它的人民之歌

> 原文：<https://hackaday.com/2019/08/07/arduino-traffic-light-sings-the-song-of-its-people/>

得到一个旧的交通灯，并把它连接起来在你的房子里工作，这并不是一个新的技巧；这是如此普遍，它通常不会通过这些神圣的页面集合。在这一点上，即使使用一个 up 来显示您的构建或系统资源利用的实时状态，也是一种推动。为了引起我们的注意，你的交通灯需要有一个独特的挂钩。

那么，[罗纳德·迪亚兹]是如何让他的项目脱颖而出的呢？有趣的是，这不是你能看到的。他的交通灯不仅仅看起来像零件，听起来也像真的一样。他付出了比你想象中更多的努力和对细节的关注，使得他的澳大利亚行人交通灯正确地模仿了原版的复杂鸣叫声。

根据 YouTube 上的红绿灯视频，[罗纳德]能够提取和分离出他想要的音调。通过对音频样本进行频谱分析，他能够计算出组成完整模式的 11 个独立音调的频率和持续时间。从持续时间仅为 25 毫秒的 973 赫兹音调到连续 500 赫兹的“啄木鸟”，声音的每一个元素都在他的 Arduino 代码中得到了一丝不苟的再现。

用于控制交通灯的 Arduino Pro Mini 不仅负责通过压电扬声器播放音调，而且正如你所料，还负责启动继电器，最终控制红灯和绿灯。随着一切的精心策划，[罗纳德]现在可以得到真正的澳大利亚路边的经验，而不必离开自己的家。

如果你希望你的室内交通灯比现实的更有用，我们有大量的现有艺术供你检查。这个告诉你比特币价值走向的[红绿灯](https://hackaday.com/2018/11/22/this-bitcoin-price-tracking-traffic-light-isnt-just-a-red-led/)就是一个很好的例子。或者这个[可以告诉你网络是否中断](https://hackaday.com/2015/09/12/traffic-light-tells-you-if-the-internet-is-up/)。

 [https://www.youtube.com/embed/Tf-1cvpUQFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Tf-1cvpUQFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

