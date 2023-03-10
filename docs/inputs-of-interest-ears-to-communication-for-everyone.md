# 感兴趣的输入:倾听每个人的交流

> 原文：<https://hackaday.com/2020/02/19/inputs-of-interest-ears-to-communication-for-everyone/>

欢迎回到感兴趣的输入！如果你还没听说，当谈到与计算机和机器交谈的新方式时，我洗耳恭听。说到耳朵，你知道它们能做出有用的把戏吗？如果你紧紧地闭上眼睛和/或打哈欠，你可能会听到像远处雷声一样的低沉的隆隆声。相当一部分人能够自愿移动他们的手机，但不是所有人。也许你已经知道你可以发出隆隆声，并且用它来自娱自乐，或者抑制生活中不愉快的声音。

[![](img/b6145505f84baa9b1a879c762f033ce6.png)](https://hackaday.com/wp-content/uploads/2020/02/rg-ear-diagram-themed.jpg)

No, you can’t reach your tensor tympani with a Q-tip. Image via [Research Gate](https://www.researchgate.net/figure/Right-coronal-temporal-bone-view-including-the-external-and-middle-ear-the-cartilaginous_fig4_274900828)

那种隆隆声是由你中耳的一块肌肉伸展引起的。它被称为鼓膜张肌，其目的是保护你的耳朵免受咀嚼声等巨响的影响，奇怪的是，还有雷声。当鼓膜张肌被激活时，它们会拉紧耳膜，以防止它们振动和受损。不幸的是，它们的反应速度不够快，无法保护我们免受枪声等突发声音的伤害。

尼克 G 能够根据命令发出隆隆声，他想知道是否可以用它作为一种输入机制，他称之为 Earswitch 。他得到了一个便宜的 USB 耳镜相机，并发现鼓膜张肌的拉伸运动足以触发运动检测软件。到目前为止，[Nick]已经能够演示对一些东西的控制，比如 Windows 屏幕键盘、Grid3 辅助软件和头部跟踪工具。

[![](img/268267637eb2ce596e9a10782f51dec7.png)](https://hackaday.com/wp-content/uploads/2020/02/earswitch-current.png)

The latest version of Earswitch uses earbud tips for comfort.

## 激起兴趣

尼克的主要目标是帮助人们使用 Earswitch 交流，但他很高兴看到它以任何方式帮助任何人做他们否则不能做的事情。鼓膜张肌的神经分布在脑干的高处，所以只要这个人能够做出至少一个动作，它就应该是一个可用的输入驱动器。

有相当多的事情你可以用一个耳朵开关来控制，特别是如果你两只耳朵都有一个，并且能够独立地激活它们。它可以驾驶轮椅，打开和关闭手机耳机，或者除了键盘/鼠标/拉力轮/操纵杆设置之外，还可以控制游戏的某些方面。一个耳开关可以用来驱动一台机器，像钻床或冲压机。

目前，尼克正在用一个更小的耳镜缩小它的尺寸，并通过将相机放在耳壳内的降噪耳机(就像舞台演员使用的那种耳机)来使它更坚固。你可以看看下面 Nick 的设置图片——他通过用眼睛移动鼠标，并用 Earswitch 点击来使用 Windows 屏幕键盘。

他仍在考虑其他运动检测方法，如 CMOS 摄像头，或者热成像设备。Nick 在 IO 上有大量的信息和一些演示视频，所以去看看吧，尝试一下，让他知道你的想法。

[![](img/74fc46e0321f9d15dfe1d70972e895b4.png)](https://hackaday.com/wp-content/uploads/2020/02/workflow.png)

## 耳朵什么也听不见

我的两只耳朵都能发出隆隆声，尽管需要热身才能闭着嘴而不是张开嘴打哈欠。我决定买一个耳镜相机，看看我能看到什么。我第一次尝试抽动我的鼓膜时，我怯场了，在那里面对摄像机时我做不到。

后来我又试了一次，虽然出于某种原因，我仍然不能对着耳朵里的相机打哈欠，但我可以通过摆动我的下巴来看到运动。我加载了 iSpy，Nick 正在使用的动作捕捉软件，果然，每当我移动下巴时，画面就会变红。此外，iSpy 可以让你轻松地做任何你想做的事情，比如运行 Autohotkey 脚本、播放声音、发送 tweet 或许多其他事情。所有这些对我来说都是 HID 战线上的好消息。即使你不能发出隆隆声，只要你能弯曲下巴，你仍然有机会使用基于耳朵的输入设备。