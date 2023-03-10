# AAA 供电的 LoRa 邮箱传感器持续使用

> 原文：<https://hackaday.com/2020/02/15/aaa-powered-lora-mailbox-sensor-goes-the-distance/>

随着世界上越来越多的通信进入电子领域，实体邮件也遭受了损失。曾经每一个新的一天都可能带来一个鼓鼓囊囊的邮箱，而今天，几天过去了，甚至连一张账单或优惠券都没有，这并不罕见。对 Eivholt 来说，这就提出了一个问题:他不想错过任何一个包裹，但是大多数的邮箱访问都是徒劳的。他的解决方案是[一个 LoRa 连接的邮箱监视器](https://www.element14.com/community/community/project14/rf/blog/2020/01/14/got-mail-lorawan-mail-box-sensor)，它从一对 AAA 电池中吸取能量，到目前为止，它已经在一台电视机上运行了两年多。

它的核心是一个单板，一个 Talk2 耳语节点。这是一个低功耗版本的 ATmega328 微控制器，还有一个 LoRa 无线电和一个高效的功率调节器，允许它在待机模式下仅消耗 8.70 uA，仅在极短的时间内醒来检查邮件并通过 LoRa 向物联网报告。该传感器只是一个微型开关，在发现簧片开关安装有问题后选择。最后，SDR 被用来调试无线电的运行。

这篇文章还介绍了超低功耗项目，包括测量这种微小电流的一些技巧。即使你对邮箱不感兴趣，任何有助于最大限度提高能效的技巧都值得一看。休息后，请观看视频，了解这个配备无线电的邮箱的运行情况。

 [https://www.youtube.com/embed/dKgmO95xJCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dKgmO95xJCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

