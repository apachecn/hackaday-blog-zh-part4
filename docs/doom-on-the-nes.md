# NES 的末日

> 原文：<https://hackaday.com/2019/06/06/doom-on-the-nes/>

“但它能运行毁灭吗？”也许是入侵一个平台的最终测试。从计算器到恒温器，我们已经看到 Doom 被硬塞进许多不同的硬件中。很多时候，我们对 mashup 感到困惑，这次也不例外。

[TheRasteri]对现有的毁灭之港不满意，所以[他决定将经典游戏带到经典主机](https://www.youtube.com/watch?v=FzVN9kIUNxw)NES 上。在休息后嵌入的视频中，他指出了运行《毁灭战士》的系统要求，并将其与 NES 的规格进行了比较。剧透:远远不够。

他是如何完成这一壮举的？他从任天堂自己的 SuperFX 芯片中获得灵感，在盒式磁带中嵌入了一个协处理器，并将盒式磁带中的视频流反馈到 NES。称它为协处理器可能不太公平，因为它是一个树莓 Pi，其处理能力是支持 NES 的 6502 的几千倍。这个想法可能看起来很熟悉，事实上它部分受到了去年[Tom7]类似的黑客攻击的启发。

使用 Cypress USB 控制器为图形总线供电，[ther astri]能够在 Raspberry Pi 上运行 Doom，从游戏中获取视觉效果，并将它们转换为 NES 希望从卡带中加载的图形块。最好的技巧是，他显然设法把所有东西都塞进了一个普通的 NES 弹药筒。他计划在他的频道上发布一个构建视频，所以请密切关注。

同时，别忘了看看我们提到的那些[计算器](https://hackaday.com/2012/01/19/doom-for-your-calculator-gets-a-color-upgrade/)和[恒温器](https://hackaday.com/2017/05/22/doomed-thermostat/)。

 [https://www.youtube.com/embed/FzVN9kIUNxw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FzVN9kIUNxw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

