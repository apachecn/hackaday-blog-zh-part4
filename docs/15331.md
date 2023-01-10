# Supercon 徽章读取“打孔”卡

> 原文：<https://hackaday.com/2022/11/17/supercon-badge-reads-a-punch-card/>

由于疫情，今年的 Hackaday Supercon 是 2019 年以来的第一次，与过去的事情非常相似。几乎每个面向硬件的黑客事件都有自己定制的电子徽章，Supercon 也不例外。今年的徽章是一个由我们自己的[Voja Antonic]创建的假想 4 位 CPU 的模拟平台，对一些在成长过程中从未接触过机器代码的参与者来说，这是一个真正的挑战。挑战集是为徽章想出最有趣的黑客，所以合作者[Ben Hencke]和[Zach Fredin]开始用他们的 [光学穿孔读卡器插件](https://hackaday.io/project/188133-supercon-2022-badge-card-reader) 确定比赛的“expandr”类别。

外围连接有些受限。这个想法是建立一个具有自己的本地处理的螺栓板——使用[Ben]带来的 PixelBlaze 板——来处理所有的扫描细节。然后，一旦卡上的程序被读取，通过其串行接口将整个事情转储到徽章 CPU。由于无法使用家里常用的设备，[Ben]和[Zach]显然不得不临时凑合他们所拥有的东西，以及可以从其他徽章或其他硬件上找到的东西。

一个大问题是，大多数人通常不会随身携带光电二极管，但幸运的是，他们记得当适当反向偏置时，LED 可以用作光电二极管。通过捐赠的 LM358 将 Meg 电阻上产生的信号馈入跨导放大器，STM32 ADC 有足够的变化来可靠地检测已填写程序卡上未填写和已填写复选框之间的差异。

CPU 需要 12 位操作码，这显然意味着需要 12 个光电二极管和 12 个发光二极管来读取每个字。PixelBlaze 板没有这么多模拟输入。一个简单的技巧是，所有 12 个光电二极管并联并馈入一个输入放大器，而不是分立输入。为了区分不同的位，照明 led 改为 charlieplexed，从而将单个位作为一系列值传送到 ADC，以供后续解串。演示视频显示，它的工作原理是，从卡上加载一个程序，然后手动启动。太有趣了！

穿孔卡通常有一个孔，可以机械读取，是配置测试器的一个很好的方式，比如 [有趣的真空阀测试器我们不久前讨论过](https://hackaday.com/2021/06/15/your-1958-punch-card-machine-tested-tubes/) 。

 [https://www.youtube.com/embed/37RK_2ZXmPU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/37RK_2ZXmPU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

