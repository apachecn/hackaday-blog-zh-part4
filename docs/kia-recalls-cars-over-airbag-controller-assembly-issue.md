# 起亚因安全气囊控制器装配问题召回汽车

> 原文：<https://hackaday.com/2022/03/09/kia-recalls-cars-over-airbag-controller-assembly-issue/>

上个月[起亚汽车宣布大规模召回](https://www.businessinsider.com/kia-recalls-410000-vehicles-airbag-deployment-issues-2022-1)，原因是安全气囊控制器单元可能存在缺陷(ACU)。此次召回涵盖了许多车型和车型年，仅在美国就涵盖了 40 多万辆汽车，以及全球 50 多万辆汽车。从[NHTSA 报道](https://static.nhtsa.gov/odi/rcl/2022/RCLRPT-22V031-6787.PDF)我们了解到问题发生在组装时，一些 acu 的盖子干扰了 EEPROM 芯片的引脚。这可能会导致某些引脚开路。如果你的车有这个问题，警示灯会亮起，但更严重的是，安全气囊在事故中不会展开。起亚估计不到 1%的使用这款 ACU 的汽车有这个问题。有这种故障的汽车将得到一个新的 ACU，其他汽车将得到固件升级，以防止这种情况发生，如果 EEPROM 引脚在未来松动。

我们认为该 EEPROM 用于记录错误和碰撞事件，因此不在安全气囊展开的关键路径中。如果 EEPROM 出现故障，原始固件显然会阻止部署。据推测，在这个补丁之后，如果将来针脚断了，故障指示灯仍然会亮起，但你会有正常工作的安全气囊。

尚不清楚这些损坏的 EEPROM 引脚焊点是否从一开始就存在，工厂测试程序是否没有发现问题。还是销完好无损地离开工厂，随后由于碰撞和振动而断裂。撇开硬件问题不谈，即使电路的非关键部分存在故障，让安全关键固件执行其主要功能似乎也是一项从一开始就应该应用于 ACU 的要求。

这提醒了外壳设计的重要性，并确保 PCB 布局考虑了整个组件所需的所有间隙。有多少次你拿回了你的 PCB，却发现你甚至忘记了安装孔？

几年前，我们曾报道过类似的高田气囊惨败事件。如果你有一辆起亚，[网站上的这个表格](https://owners.kia.com/content/owners/en/recalls.html)会告诉你你的车是否会被召回。