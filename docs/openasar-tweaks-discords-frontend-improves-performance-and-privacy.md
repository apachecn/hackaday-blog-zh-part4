# OpenAsar 调整了 Discord 的前端，提高了性能和隐私

> 原文：<https://hackaday.com/2022/06/19/openasar-tweaks-discords-frontend-improves-performance-and-privacy/>

并非所有的黑客攻击都发生在硬件上——时不时地，我们也应该攻击我们基于软件的工具。[Ducko]告诉我们一个部分开源的对 Discord 的电子前端的重写。Web 应用程序可能很难修改，这就是为什么这样的项目会受到赞赏。现在，这不是对 Discord 的 API 的逆向工程，也不是替代客户端本身，但它确实为 Discord 客户端应该为我们做什么提供了一个充满希望的视角。

首先，客户端加载明显更快，不像著名的 [GTA 在线加速](https://hackaday.com/2021/03/02/fixing-the-only-thing-thats-slow-about-grand-theft-auto-v/)(这也是用户驱动的改进)，频道和服务器切换变得不那么滞后 Linux 更新程序也被取消了。[Ducko]告诉我们她是如何摆脱原始代码的大量 NPM 依赖的——事实证明，大多数依赖可以很容易地用 Node 替换。JS 原生 API 或者 Linux 二进制比如`unzip`。除了备受赞赏的性能改进，还有遥测旁路等选项，以及针对您自己的主题的定制机制。你不会在你的苹果上得到不和谐的东西，但是本地客户会对你更友好一点。

虽然 Discord 最终是一个专有平台，但我们不时会在一些很酷的黑客中看到它的使用，比如这个[茶杯温度跟踪杯垫。](https://hackaday.com/2018/08/14/internet-of-tea-coaster-watches-for-optimum-drinking-temperature/)你愿意自己编写不和谐机器人吗？[我们为那个](https://hackaday.com/2018/02/15/creating-a-discord-webhook-in-python/)写了一个演练。最后但同样重要的是，如果你喜欢我们写的东西，并且你碰巧也使用 Discord，你应该去看看 [Hackaday Discord 服务器！](https://discord.com/invite/NkbHrAW7NG)