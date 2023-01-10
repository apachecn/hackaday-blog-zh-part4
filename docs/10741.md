# 全球芯片短缺的故事:Smoothieboard

> 原文：<https://hackaday.com/2021/07/17/tales-from-the-global-chip-shortage-smoothieboard/>

由疫情引发的半导体短缺没有减缓的迹象。虽然汽车制造商是最先受到影响的，但短缺现在已经蔓延开来，并影响到各种项目，包括 [Smoothieboard 开源数控控制器。](https://www.robosprout.com/the-global-chip-shortage-and-smoothie/)

[克里斯·塞西尔]讲述了他们过去几个月的生产困境。它始于今年春天的一批 1.1 版主板。他们的一些芯片的价格开始上涨，然后他们被告知，作为 Smoothieboard 大脑的微控制器的价格只有旧价格的五倍。最后，他们下了一个较小的订单，在微控制器的价格恢复正常之前，V1.1 Smoothieboards 可能会很稀缺。

将 V2 电路板投入生产更加困难。就在最终原型的几周前，人们发现 V2 所围绕的 LPC4330 微控制器也在全球范围内销售一空。考虑到这种短缺，V2 最终版本的布局中留了一个洞，这样他们就可以围绕他们能够得到的任何微控制器完成设计。最终，他们能够锁定 STM32H745 控制器的供应，这实际上比原始设备的能力强得多。

如果你对芯片短缺的根源感兴趣，[一月份的这篇文章是一个很好的起点](https://hackaday.com/2021/01/18/pandemic-chip-shortages-are-shutting-down-automotive-production/)。零件短缺已经不是第一次给电子世界带来浩劫了——[有人记得 18 年的全球电阻短缺吗？](https://hackaday.com/2018/01/31/global-resistor-shortage-economics-and-consumer-behavior/)