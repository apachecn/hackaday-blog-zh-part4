# Pi 4 的电源:一些充电器可能不符合标准

> 原文：<https://hackaday.com/2019/06/28/power-to-the-pi-4-some-chargers-may-not-make-the-grade/>

Raspberry Pi 4 已经在消费者手中几天了，虽然每个人似乎都对他们的新主板感到满意，但有一些[报告称某些 USB-C 电源无法为他们供电](https://www.raspberrypi.org/forums/viewtopic.php?f=91&t=243423)。据推测，原因可能在于在 Pi 上的 USB-C 插座后面的配置通道(CC)线路上使用了下拉电阻，[推测可能使用了一个，而应该需要两个](https://www.scorpia.co.uk/2019/06/28/pi4-not-working-with-some-chargers-or-why-you-need-two-cc-resistors/)。名为[的供应品包括一些苹果 MacBook 充电器](https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=243799)，有一种说法是 Pi 可能不是这些充电器无法运行的唯一设备。

这是你应该担心的事情吗？几乎可以肯定不是。Pi 人员已经用各种各样的充电器测试了他们的产品，但不可避免的是，他们无法抓住每一个可能的充电器。如果您的充电器受到影响，请尝试另一个。

它确实说明了任何人在将一种新的电子产品推向市场时所面临的困难，不管他们作为一个组织是大是小。几乎不可能测试每一个可能的用例，事实上，以前的 Pi 模型就发生过这种情况。你可能记得[Raspberry Pi 2 可以通过相机闪光灯](https://hackaday.com/2015/02/08/photonic-reset-of-the-raspberry-pi-2/)复位，或者如果你有很长的记忆，最早的电路板在两条 1.8 V 线之间有一场不体面的战斗，导致 USB 芯片发热，这些小问题都没有削弱他们的电路板完成工作的能力。

错误时有发生。从相对简单的 micro-USB 向 USB-C 的转变对所有相关人员来说都是一个巨大的进步，如果它能毫无意外地通过，那将是一个惊喜。我们确信迟早会有一个修订版的 Pi 4，我们很想知道他们在这个角落里做了什么。