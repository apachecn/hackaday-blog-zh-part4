# 开放式硬件 5V UPS 改进了廉价的电源组设计

> 原文：<https://hackaday.com/2022/01/31/open-hardware-5v-ups-improves-on-cheap-powerbank-design/>

通常，我们需要在旅途中为我们渴望 5V 的项目供电。[Burgduino]也是如此，而且，由于对现有解决方案不满，[设计了他们自己的 5V UPS！](https://www.reddit.com/user/soubitos/comments/rchcpu/open_hardware_tp5400_dc_ups_design_files_in_link/)它采用廉价的电源组设计，并增加了一些对其 UPS 目的至关重要的部件。

当面临这样的问题时，你可能会忍不住伸手去拿一个 powerbank，但它们中的大多数都有一个致命的缺陷，在你购买之前，你很难区分有缺陷的和正常工作的。这一缺陷是缺乏负载共享——当插入充电器时，能够继续为输出供电。大多数商店购买的 powerbanks 只是关闭输出，这阻止了一个项目在不关闭电源的情况下全天候运行，当涉及到像 Raspberry Pi 这样的东西时，可能会导致不利的后果。

可以理解的是，[伯格杜伊诺]对此并不满意。他们的 UPS 基于 TP5400，这是一种锂离子充电和升压芯片，在简单的电源组中使用很多，但不能负载共享。为此，使用了一个额外的 LM66100 芯片——一个“理想二极管”控制器。你可能会嘲笑它是德州仪器的一部分，但它似乎是广泛可用的，只比 TP5400 本身贵一点点！设计[是开放硬件](https://oshwlab.com/catech75/arduinouno-dc-ups_copy_copy)，PCB 文件可在 EasyEDA 上获得，BOM 清楚地列出，便于 LCSC 订购。

我们这些黑客可能会努力保持我们的便携式 Pi 项目的供电，[使用超级电容器](https://hackaday.com/2020/11/05/a-super-ups-for-the-pi/)和[修改设计糟糕的中国电路板](https://hackaday.com/2019/08/27/fixing-a-cheap-ups-hat-for-your-raspberry-pi-with-a-tiny-daemon/)。然而，一旦我们为我们的目的找到了合适的工具包，电池供电的项目往往会开辟新的领域——你甚至可以超越你的 Pi 和[用 UPS 插件](https://hackaday.com/2021/11/01/dc-ups-keeps-the-internet-up/)升级你的路由器！当然，这并不总是一帆风顺的，有时看似便携的设备[可能会以其设计怪癖让你大吃一惊](https://hackaday.com/2020/11/25/a-raspberry-pi-400-ups-add-on-its-not-all-plain-sailing/)。