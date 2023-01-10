# 短缺时代的旧服务器硬件国产化

> 原文：<https://hackaday.com/2022/01/24/domesticating-old-server-hardware-in-the-age-of-shortages/>

我们自己的[戴夫·罗恩特里]在做涉及未公开类型的模拟的有偿工作时开始遇到瓶颈，并决定为此获得一台单独的计算机。如今，寻找经济实惠的高性能计算机是一项令人失望的任务，因此，[是时候让一台使用了 10 年的 HP Proliant 380-g6](https://davidrowntree.co.uk/upcyling-an-hp-proliant-dl380-g6/) 从 Dave 的存储机架中出来了。这款 Proliant 服务器是一款令人印象深刻的硬件，设计为 24/7 运行，具有双 CPU 选项、18 个 RAM 插槽和硬盘硬件 RAID 足够旧，更换和升级零件很便宜，但足够新，是满足[Dave]需求的合适工具！

在论证了一些特殊的选择之后，如使用双低功耗 GPU，仅填充 18 个 RAM 插槽中的 12 个，以及选择 Windows 而不是 Linux，[Dave]描述了一些使该服务器服务良好所需的硬件模块。首先，专有的硬件 RAID 控制器备用电池必须更换为常规的镍氢电池组。更大的问题是服务器异常吵闹。事实证明，双 GPU 让主板管理控制器太困惑了。有人写了一个修改过的固件来解决这个问题，但是这个固件有一个[戴夫]不想冒的风险。最终结果？[Dave]在服务器中设计和改装了一个 Arduino 供电的 PWM 控制器，并配有看门狗功能，以降低过热情况的风险。所有这些的解释和代码都可以在博文中找到，光是见解就值得一读。

如果你需要一个功能强大的硬件放在你的桌子旁边，并且得到了一台二手服务器，这篇文章将告诉你要注意的问题。我们不经常报道服务器黑客——我们在黑客在线空间[看到的典型服务器都是树莓 Pi 板](https://hackaday.com/2021/07/21/raspberry-pi-server-cluster-in-1u-rack-mount-case/),看到真实的服务器硬件获得新生令人耳目一新。这台服务器永远不需要 KVM 急救车，但是如果你决定无头运行你的，不妨[用一台报废的笔记本电脑](https://hackaday.com/2019/03/10/from-a-dead-laptop-to-a-portable-kvm-and-pitop/)造一台急救车。如果你认为运行一台旧服务器比购买新硬件花费更多的电费，这是公平的——但是[不要忘记在回收剩余部分之前重新利用它的 PSU](https://hackaday.com/2012/07/17/repurposing-server-psu-for-your-charging-needs/)!