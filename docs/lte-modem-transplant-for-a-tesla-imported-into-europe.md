# 进口到欧洲的特斯拉的 LTE 调制解调器移植

> 原文：<https://hackaday.com/2022/01/03/lte-modem-transplant-for-a-tesla-imported-into-europe/>

当现代联网汽车跨越各大洲时，新的兼容性问题突然出现。[Oleg Kutkov]是一名经验丰富的工程师，当一个美国定制的 LTE 调制解调器在他刚从美国-欧洲进口的特斯拉上工作不佳时，他并没有烦恼，并且[向我们介绍了他用另一个兼容欧洲 LTE 频段的特斯拉调制解调器模块替换调制解调器的旅程](https://olegkutkov.me/2021/06/10/tesla-model-3-us-lte-modem-replacement-and-some-reverse-engineering/)。

[Oleg]的帖子介绍了板上的不同部分，并向您展示了在特斯拉的媒体计算机单元(MCU)的更大画面中如何需要它们，甚至移除了 LTE 调制解调器的屏蔽来描述其下的 IC，iFixit 拆卸图风格！一个值得注意的亮点是芯片上的 SIM 卡，本质上是一种非常受欢迎的 DFN 封装的 SIM 卡，谢天谢地，在一些延长线上用常规 SIM 卡的插座代替它已经证明是卓有成效的。由此产生的特斯拉现在可以以超过 EDGE 提供的速度享受互联网连接。这篇报道对其他面临同样问题的特斯拉车主来说应该是一个很好的指导，但它也有助于我们在集体意识中让电动汽车不那么像黑匣子。

并非特斯拉设计决策的所有结果都是如此微小；例如，今年，我们已经描述了[特斯拉汽车](https://hackaday.com/2019/10/17/worn-out-emmc-chips-are-crippling-older-teslas/)的一种流行的 eMMC 故障模式，以及[特斯拉如何未能解决它](https://hackaday.com/2021/02/11/tesla-recalls-cars-with-emmc-failures-calls-part-a-wear-item/)。谢天谢地，特斯拉汽车越来越成为黑客社区的目标，无论是[制造一个计算机视觉辅助机器人](https://hackaday.com/2021/07/02/a-robot-to-top-up-your-tesla/)来插上充电电缆，[以经销商成本的一小部分进行修理](https://hackaday.com/2021/07/16/repair-hack-saves-tesla-owner-from-massive-bill/)，还是[甚至用废旧零件组装你自己的特斯拉](https://hackaday.com/2017/09/20/salvaging-your-way-to-a-working-tesla-model-s-for-6500/)！