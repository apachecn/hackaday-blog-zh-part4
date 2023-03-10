# 最后的科学计算器？

> 原文：<https://hackaday.com/2020/03/02/the-last-scientific-calculator/>

曾经有一段时间，作为一名工科学生意味着你有一把剑。嗯，实际上它是挂在你腰带上的计算尺，但称它为剑听起来更酷。计算尺剑让位于挂在腰带上的计算器，对许多工程师来说，计算器来自惠普。今天的学生更有可能拥有 TI 或卡西欧计算器，但惠普仍有惠普 Prime。很难称之为计算器，因为最新的版本有 528 MHz 的 ARM Cortex A7，256 MB 的 RAM 和 512 MB 的 ROM。但是如果你不能证明 150 美元的计算器是合理的，有一些便宜甚至免费的选择来获得这种体验。首先，惠普有一个运行在 Windows 或 Mac 上的免费应用程序,就像计算器一样工作。当然，这是免费的，而不是开源的免费。但是，它仍然可以在葡萄酒下运行，不需要比平常更多的哄骗。

你可能想知道为什么你的电脑上需要一个计算器，也许你并不需要。然而，HP Prime 不仅仅是你 80 年代的老式计算器。它还有数量惊人的应用，包括一个基于 [xCAS/Giac](https://www-fourier.ujf-grenoble.fr/~parisse/giac.html) 的完整符号数学系统。它也可以使用类似 Basic 或 Pascal 的特殊 HP 语言进行编程。其他应用程序包括绘图、统计、求解器，甚至可以容纳多达 10，000 行和 676 列的电子表格。

## 轻便

很容易认为惠普提供免费的 PC 软件，所以你会出去买真正的计算器，这可能是它的一部分。不过，你也可以获得 Android 和 iOS 的官方应用。它们不是免费的，但相对便宜。在 iOS 上，现在的价格是 25 美元，在 Android 上是 20 美元。也有免费的“精简”版本。

看起来这些应用程序并没有模拟实际的计算器硬件，而是计算器代码的移植。因此，这不是一个人只是编写一个虚拟计算器的情况，这些应用程序就像真正的计算器一样，因为它运行相同的源代码。例如，有一个应用程序，HP Connectivity Kit，可以让你通过网络与一个真正的计算器对话。PC 和手机版本也将像一个真正的设备一样连接。

## 编程；编排

您可以在设备上编写程序，或者如果您有 HP 连接软件(也是免费的),您可以在 PC 上编写程序。你甚至可以从网上找到一些。如果你想念你的旧计算器，有一个定义功能，让你像一个关键的宏记录编程。

这种编程语言不难学。这里有一小段:

```

EXPORT AREAVOL()
BEGIN
LOCAL N1, N2, L1;
CHOOSE(N1, "Area or Volume?", "Area", "Volume");
IF N1 == 1 THEN
CHOOSE(N2, "Choose shape", "Rectangle", "Triangle", "Disk");
ELSE
CHOOSE(N2, "Choose solid", "Prism", "Cylinder", "Cone", "Pyramid", "Sphere");
. . .

```

## 黑客和下一步是什么？

你可能会认为真正的硬件将是黑客攻击的主要平台，但迄今为止，这仍在待办事项列表中。真正的计算器唯一真正好的硬件黑客是给机器添加一个容量更高的三星电池。PCB 上还有一些诱人的焊盘，似乎支持蜂鸣器和 I2C 通信，但没有固件。已经有一些尝试将外星固件加载到设备中，但是还没有成熟的开发系统。到达 JTAG 港[看起来相当紧张](https://tiplanet.org/forum/viewtopic.php?p=238323#p238323)。还有不可避免的对[通信协议](https://hackaday.io/project/947-hp-prime-calculator-reverse-engineering)的黑客攻击。

历史上有很多产品在当时看起来很神奇，但结果却是更好产品的权宜之计。卡带让位于 CD，然后 CD 让位于数字音乐。电话答录机让位于语音信箱。计算器有这种感觉。我们还需要他们多久？虚拟 HP Prime 应用程序会让物理设备黯然失色吗？

不管怎么说，Prime 是最先进的，会让几年前的个人电脑相形见绌。你只能怀疑它是否会是最后一个伟大的计算器，或者是否会有更多的计算器出现。计算器仍然是一个很好的项目。并非所有的[自制计算器](https://hackaday.com/2018/08/07/diy-scientific-calculator-powered-by-pi-zero/)都很简单。