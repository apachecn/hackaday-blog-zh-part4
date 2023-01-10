# 绘制修复 R0tring CS-50

> 原文：<https://hackaday.com/2021/09/29/plotting-to-restore-a-r0tring-cs-50/>

如果你是某个时代的人，并且曾经画过任何技术图纸，很有可能你使用了某种类型的线，不管是铅笔还是钢笔。r0tring 不仅制造书写工具。他们还制造了电子划线器——一种小型绘图仪，可以根据输入内容在技术图纸上书写 ISO 字母。这比徒手或用模板印刷每个字母节省了大量时间。CS-50 旨在容纳顶级的 r0tring 绘图笔，除了花费时间找出问题外，这是这次修复中最昂贵的部分。

[Atkelar]喜欢打开东西，并在开机前对它们进行目视检查。我们认为这是一个很好的练习，即使悬念会杀了你。但是真的，[【阿特克拉】做的远不止这些](https://www.youtube.com/watch?v=rz_wnqaPhrs)。他首先更换了可能是 80 年代后期的硬币电池，尽管它的注册电压为 3 V。然后他更换了所有的电解电容和一个钽，用廉价的电动牙刷清洁了橡胶圆顶键盘部件(另一个伟大的想法)，并完全拆卸了 x-y 机构，以清洁和重新润滑它。

[![Building a new screw boss with cyanoacrylate glue and baking soda.](img/67e0b1beb5d1e31101abc88bcda8cc2a.png)](https://hackaday.com/wp-content/uploads/2021/09/glue-boss.jpeg)

Glue boss!

接下来是真相大白的时刻。输入工作并显示在屏幕上，但步进器不动。电机的波形看起来不错，但似乎过压约 3 V。虽然[Atkelar]无法在网上找到手册，但他确实找到了一篇关于这台机器的博客帖子，证实步进器上的 15 V 电压是正确的。

事实证明，有一个地面问题。电源电缆的护套充当公共接地，因此将其压在已拆卸机箱的底板上可以使步进器工作。但是过了一段时间，他们退出了。[Atkelar]清洁终端，但什么都没有改变-步进机会工作一段时间，然后停止。

我们认为这肯定会成为本周的失败，但[Atkelar]检查了更多的电机引脚，发现其中一个驱动芯片是死的。幸运的是，他找到了一个替代品，这东西工作起来像新的一样。休息后查看完整的修复视频，寻找我们最喜欢的部分。这时[Atkelar]通过用聚酰亚胺胶带建造一堵墙，并用氰基丙烯酸酯胶和小苏打填充空腔，模制出了一个新的螺旋凸台末端。

有心情做更多修复吗？[用【drygol】的东西肯定不会出错，这是肯定的](https://hackaday.com/blog/?s=drygol)。

 [https://www.youtube.com/embed/rz_wnqaPhrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rz_wnqaPhrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[macsimski]！