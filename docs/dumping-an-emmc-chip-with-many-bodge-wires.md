# 倾倒一个带有许多桥接线的 EMMC 芯片

> 原文：<https://hackaday.com/2022/10/11/dumping-an-emmc-chip-with-many-bodge-wires/>

有时，您知道您需要的数据存储在哪里，只是没有办法访问它。在这种情况下，[缺氧]需要从相机中抢救出来的 eMMC 芯片上获取数据。不想等待适配器出现，[是时候打开盒子了！](https://twitter.com/GetHypoxic/status/1579538991141249024/photo/1)

一旦从 PCB 上移除，bodge 线就连接到芯片底部的球栅阵列触点上。令人难以置信的精细焊接是当时将这些连接到小焊盘上的命令，我们总共数了 11 或 12 根博奇线。手动给 eMMC 芯片提供 1.8 伏的电压，直接连接到旧笔记本电脑内置读卡器的触点上进行阅读。

尽管它看起来像老鼠窝，用黄色的聚酰亚胺胶带把它粘在一起，[get oxygen]报告说它安装成功并完成了任务。我们以前也见过类似的黑客攻击，[将 eMMC 芯片连接到 SD 卡适配器](https://hackaday.com/2017/07/12/emmc-to-sd-hack-rescues-data-from-a-waterlogged-phone/)。这可能看起来很乱，但是嘿——这肯定比等待发货要好！