# 添加矢量艺术到你的鹰板

> 原文：<https://hackaday.com/2018/11/24/adding-vector-art-to-your-eagle-boards/>

Badgelife 和艺术 PCB 的兴起正在拓展印刷电路板的应用范围。如果你在做 PCB 艺术，你真的想用向量来做。这是一个令人惊讶的难题，因为实际上很少有软件工具能够正确处理 DXF 和 SVG。[不要害怕，因为【TallDarknWeirdo】有适合您的解决方案](https://www.youtube.com/watch?v=EI2CLwQi6N0)。在 Eagle 中，它使用了 Illustrator *和* Inkscape，但是这又是一个难题。

这个例子的演示物品只是一棵圣诞树。绿色阻焊膜是标准的，FR4 看起来像木头，银色和金色等等。[TallDarknWeirdo]首先将这个矢量艺术分割成其组成部分——阻焊层、裸 FR4 和铜——然后将其导入 Inkscape 以制作 SVG。然后这个被扔进了一个在线工具中，这个工具创造了 Eagle 可以理解的东西。结果比导入位图更好，使完成的纸板线条更清晰。

不过，在我们进入这个话题之前，先给你提个醒:如果你在 2019 年或以后读到这篇文章，这些信息可能已经过时了。Autodesk 应该很快就会为 Eagle 发布一个矢量导入工具，我们将会深入研究这个工具，直到它可以工作为止。在此之前，这是将矢量艺术融入 Eagle 的最佳方式。

哦，对了，[塔尔达科韦多]不是别人，正是[布拉德利·高斯罗普]，他在压接电线上花的时间比我们认识的任何人都多。