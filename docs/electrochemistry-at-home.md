# 家庭电化学

> 原文：<https://hackaday.com/2020/08/02/electrochemistry-at-home/>

几年前，我的生物传感器研究需要一个非常小的恒电位仪。我在 [Hackaday](https://hackaday.com/2011/09/14/cheapstat-an-open-source-potentiostat/) 和 [HardwareX](https://hackaday.com/2020/04/13/three-years-of-hardwarex-where-are-they-now/) 上找到了大量很酷的示例项目，但它们并没有完全满足我的需求。正如你们任何人在这种情况下都会做的那样，我决定制造自己的设备。

[现在，我们已经在](https://hackaday.com/2018/12/03/why-is-continuous-glucose-monitoring-so-hard/)之前讨论过恒电位仪。这些器件与商用血糖仪中使用的器件相同，因此它们广泛适用于多种生物传感应用。在我的互联网搜索中，我偶然发现了德州仪器公司的一款名为 LMP91000 的酷芯片，它最初似乎为我做了所有的艰苦工作。不幸的是，LMP91000 的一些功能有点限制，没有给我提供我的研究所需的灵活性。你看，电化学的工作原理是将一组电极偏置在一个给定的电位上，然后驱动一个化学反应。电子转移由传感电极测量，并使用跨阻放大器(TIA)转换为电压。商用恒电位仪可以有微伏分辨率的偏压发生器，但我只需要约 1 mV 左右。问题是，LMP91000 在 3.3 V 电源下的分辨率约为 66 mV，这要求我像其他人一样，用外部数模转换器(DAC)来增强 LMP991000。

然而，用 DAC 改变 LMP91000 的内部基准电压会混淆 TIA 的电压测量值，因为 TIA 也参考与偏置电压发生器相同的内部零点。这似乎是我遇到的其他 DIY 解决方案应该提到的问题，但我没有找到任何其他描述这个问题的论文。打了自己一拳后，我想这可能对除我之外的其他人来说更明显一些。有时候就是这样。哦，好吧，这是一个有点简单的修复，最终使我的小恒电位仪比我原来想象的更有能力。

我本来可以像偶然发现的其他几个例子一样制作一个完整的定制恒电位仪电路，但 LMP91000 的集成方面有点太难了。我的设计需要尽可能小，因为我最终希望将设备集成到可穿戴设备中。我使用的是带有内置 DAC 的 SAMD21 微控制器，因此解决问题比我最初想象的要方便一些，因为我的设计中不需要额外的芯片。

我对结果非常满意。我的稳压器叫 KickStat，大约有 25 美分硬币大小，有一吨的空间，可以在我下一次修改主板时很容易地修剪掉。我想象这可以被用作任何大型设计中的子系统，如[血糖仪](https://hackaday.com/2016/06/28/hackaday-prize-entry-a-universal-glucose-meter/)、[手机](https://hackaday.com/2013/07/20/arduino-cellphone/)，甚至可能是[智能手表](https://hackaday.com/2019/01/01/a-smartwatch-you-can-easily-build-yourself/)。

在我的[研究实验室的 GitHub 页面](https://github.com/LinnesLab/KickStat-Paper-Firmware)上查看所有开源文件。我希望我的经验能对黑客社区有所帮助。绝对是一个有趣的构建，我希望你们都像我一样从中得到乐趣。