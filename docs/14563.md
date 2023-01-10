# 用 500 个垃圾电容器建造一个点焊机

> 原文：<https://hackaday.com/2022/08/20/building-a-spot-welder-from-500-junk-capacitors/>

[卡西扬电视台 YouTube 上有一堆数量相当大的备件，其中一些是有用的，并分配给了特定的项目，但鉴于他们感兴趣的电子产品类型，他们无法找到一袋 500 左右的低规格 470uF 电容器的用途。这些不是低 ESR 类型，也不是高电容类型，因此不适合单独用作电源。但是，[把它们都并联起来](https://www.youtube.com/watch?v=LdklXOSjQD0)呢？(视频，嵌入在下面)经过一些快速计算后，[卡西扬]确定所有 500 的总电容应该约为 0.23 法拉，ESR 在 16V 时约为 0.4 至 0.5mω，理论上总能量约为 30 焦耳。在适当的情况下，这足以打出一拳。

一个 PCB 被构造成将 168 个小罐并行布线，具有很宽的迹线，用多股直径为 1.8 毫米的铜线和顶部的一层很厚的焊料加固。为了使总电阻尽可能低，三个这样的 PCB 用相同的铜线并联。这种器件有一些实际用途，因为测得的 ESR 极低(0.6mΩ)且电容较大，使其成为许多应用中平滑电源的理想选择，但它能用来制作点焊机吗？嗯，是也不是。当与那些廉价的中国“点焊机”控制器结合使用时，它确实可以在带有薄镀镍电池条的 LiPo 电池上产生一些焊缝，但直接穿透它几乎没有穿透。[卡西扬]发现，电容器组可以与一个像样的 LiPo 电池并联使用，从而提供一个潜在的理想组合——电容器的巨大初始冲击力吹穿钢带，开始焊接，LiPo 随后以较低(但仍然巨大)的电流持续一段时间，以帮助渗透到电池端子中，完成焊接。

[Kaysan]对峰值电流传输及其分布进行了一些测量，表明即使是一堆非常普通的部件，只要稍加注意，也可以变成有用的东西。这样的组件和单个[超级电容](https://hackaday.com/2020/09/16/rapid-charging-supercapacitors/)相比如何？我们不久前谈到了[超级电容器和脂肪电池](https://hackaday.com/2021/12/01/supercapacitors-vs-batteries-again/)，这是一个有趣的讨论，如果你仍然感兴趣，[石墨烯基混合超级电容器](https://hackaday.com/2020/03/14/hybrid-supercapacitors-are-well-super/)也是一个东西！

 [https://www.youtube.com/embed/LdklXOSjQD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LdklXOSjQD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢【Danjovic】的提示！