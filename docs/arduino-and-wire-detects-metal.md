# Arduino 和 Wire 检测金属

> 原文：<https://hackaday.com/2020/10/21/arduino-and-wire-detects-metal/>

我们以前的数学老师有一句名言:“你必须用你知道的去发现你不知道的。”这同样适用于许多微控制器设计，包括[rgco]智能[金属探测器](https://www.instructables.com/Minimal-Arduino-Metal-Detector/)，除了 Arduino 之外几乎不使用任何其他设备。操作原理很简单。Arduino 可以测量时间，线圈和电阻会产生与电路值成比例的延迟，线圈周围的金属会改变线圈的电感。随着电感的变化，延迟也会变化，因此，Arduino 可以感应金属，正如您在下面的视频中看到的那样。

简单的原理在实践中也很简单。除了 Arduino 和线圈，还有一个电阻。你需要一个小线圈，因为大线圈检测不到小物体。如果你不想自己缠绕线圈，[rgco]建议使用一卷连接导线，只要电阻低于 10 欧姆。

你可以省略它，但最初的设计有一个蜂鸣器和一个电解电容器相连，当金属靠近时，除了内置的 LED 指示器外，还会产生蜂鸣声。如果线圈开路、过短、过长或电阻过大，LED 也会闪烁。

最大的问题是，可怜的 Arduino 需要测量纳秒范围内的延迟。它实际上不能直接做到这一点，所以代码需要进行测距测量，然后产生适当大小的脉冲，并将它们相加，以更好地了解总延迟。在帖子中有几个视频是在 Tic Tac 容器中构建的原型和最终设备，你可以在下面看到。

如果你想要一个有点花哨的东西，这里有[另一个简单的设计](https://hackaday.com/2020/05/02/a-smart-diy-metal-detector/)有几个更多的部分。或者你可以去找一个[超敏感的](https://hackaday.com/2020/10/18/precision-metal-detector-finds-needles-in-haystacks/)。

 [https://www.youtube.com/embed/U9xlYVrnF3o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U9xlYVrnF3o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

