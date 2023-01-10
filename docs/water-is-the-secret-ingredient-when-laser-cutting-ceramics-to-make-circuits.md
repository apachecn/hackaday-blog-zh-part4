# 水是激光切割陶瓷制作电路的秘密成分

> 原文：<https://hackaday.com/2021/10/02/water-is-the-secret-ingredient-when-laser-cutting-ceramics-to-make-circuits/>

应用科学公司的 Ben Krasnow 正在用他的廉价 CO2 激光切割机试验切割廉价的陶瓷片，这时他发现(正如所料)CO2 光束的热冲击会导致工件开裂和断裂。经过大量实验，他偶然发现了一个简单的解决方案:浸没在一层薄薄的水中足以带走多余的热量，防止热冲击，并最终切割材料。一些现有技术被发现，我们相信是英国曼彻斯特大学的[这篇博士论文](https://www.research.manchester.ac.uk/portal/files/54520291/FULL_TEXT.PDF) (PDF)。对于任何想更深入地研究这种技术的人来说，这是一本很好的读物。

CO2 激光切割机是一种非常通用的工具，能够切割和蚀刻多种材料，其中许多是天然材料，如纸板、皮革和木材，以及某些塑料和其他合成材料。但是，也有一些材料通常是不可行的，如金属、陶瓷和任何不能充分吸收激光波长或反射性太强的材料，所以在弓上有另一根弦是一件好事。毕竟，不是每个人都可以使用光纤激光器。

在解决了如何切割陶瓷的问题后，它变得更加有趣了。他开始沉积足够坚固的导电迹线，以便焊接。掩模由乙烯基薄片制成，并且使用刮板沉积厚层的银和尺寸为 1 um 或更小的玻璃颗粒。然后在一个小窑中烧结，用运行 [PicoReFlow](https://apollo.open-resource.org/mission:resources:picoreflow) 的树莓 Pi 控制，经过一点点擦洗，表面电阻是一个非常有用的 2mω/square。用激光切割的孔，再加上一些银材料，用橡胶滚轴挤出，不需要额外的努力就能形成通孔。这真是太棒了！

一些焊膏和零件被添加到演示板上，并添加了一个 flare，除了他之外没有其他真正的原因，只需直接给电路板通电即可回流。底部表面采用了加热器走线，使电路板能够自回流。现在那很酷！

 [https://www.youtube.com/embed/kxXEI0Ce6C0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kxXEI0Ce6C0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Baldpower]的提示！