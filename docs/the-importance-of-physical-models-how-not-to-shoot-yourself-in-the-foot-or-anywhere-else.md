# 物理模型的重要性:如何不打自己的脚或其他地方

> 原文：<https://hackaday.com/2022/11/10/the-importance-of-physical-models-how-not-to-shoot-yourself-in-the-foot-or-anywhere-else/>

对于我们的物理模型，我们总是走捷径。例如，我们很少考虑导线有电阻，或者电池有电源阻抗。这很好，直到它不是。以海军的格鲁曼 F11F 虎式飞机为例。超音速飞机令人印象深刻，尽管它有一些致命的缺陷。但是它也是第一架击落自己的飞机。

这是简单的数学。一架速度为 1 马赫的飞机大约以 1200 千米/小时的速度飞行——确切的数字取决于几个因素，比如你的高度和湿度。假设大约 333 米/秒。另一方面，20 毫米口径的枪射出的子弹的移动速度超过 1000 米/秒。所以当子弹离开飞机时，飞机需要超过三秒钟才能追上它，那时它已经移动得更远了，对吗？

## 谁把你打下来的？

不，1956 年，汤姆·阿特里奇从长岛起飞，在大西洋上空做武器试验。他爬到 20，000 英尺，开始以 1 马赫的速度俯冲，并在大约 13，000 英尺的高度发射耗尽弹药的大炮。

在 7000 英尺的高度附近，有东西撞到了他的挡风玻璃——可能是一只鸟。飞机开始失去动力，坠毁后留下一条 300 英尺长的火焰轨迹，穿过机场附近的树林。阿特里奇幸免于难，但腿和脊椎骨骨折。

但是撞上海军飞行员飞机的不是一只鸟。那是他自己的子弹。问题是，子弹确实以很高的速度离开了枪。然而，他们立即遇到了空气阻力，导致他们慢下来。当子弹减速到 643 米/秒时，飞机正以 1400 米/秒的速度前进。三颗子弹击中了飞机，一颗穿过了鼻锥，一颗穿过了挡风玻璃，还有一颗击中了右舷发动机进气口。这一切只花了 11 秒钟。你可以在下面的视频中看到整个故事。

 [https://www.youtube.com/embed/3kmRFD6q5iE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3kmRFD6q5iE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



与同时代的其他战斗机相比，这种飞机被证明不太可靠。它有其他不良特征，但它被用作训练飞机，蓝天使一直使用到 1968 年。

## 吸取教训了？

你可能会认为这足以证明出了问题，但事实并非如此。这被认为是“侥幸”当然，在 1973 年，一架 F-14 雄猫也用假导弹击落了自己。一架荷兰 F-16 也在 2019 年在一次非常类似的事件中击落了自己。你不得不怀疑是否还有其他未被报道的例子。

然而，这里有一个教训。常识并不总是工程常识。你认为两微米的偏差不重要吗？[再想想](https://hackaday.com/2020/04/29/test-equipment-shim-washers-and-a-30-year-old-space-telescope/)。或者也许你想在核电站用蜡烛检查[的空气泄漏？工程史上充满了这样的故事:任何一个有理智的人都会认为某件事很好，但现在回想起来，却一点也不好。](https://hackaday.com/2018/12/06/fail-of-the-week-1975-the-browns-ferry-nuclear-incident/)

俄罗斯有句古话“信任但要核实”这对我们来说也是一句很好的格言。相信你的直觉，但是要用考虑到一切的可靠的数学模型来验证。