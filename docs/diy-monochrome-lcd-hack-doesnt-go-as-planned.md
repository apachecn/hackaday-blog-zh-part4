# DIY 单色 LCD Hack 没有按计划进行

> 原文：<https://hackaday.com/2020/03/01/diy-monochrome-lcd-hack-doesnt-go-as-planned/>

使用掩模立体光刻(MSLA)工艺的低成本 3D 打印机制造商能够如此廉价地制造他们的机器，因为他们使用重新利用的智能手机或平板电脑液晶面板来屏蔽紫外线背光。考虑到你从入门级的 MSLA 树脂打印机中获得的质量，我们当然不会抱怨这种节俭。但是正如[Jan Mrázek]在最近的博客文章中解释的那样，当然还有改进的空间。

问题是，正如你所料，这些重新利用的液晶面板是彩色显示器。毕竟，几十年前，即使是最底层的移动设备也不再使用单色显示器。但在这种情况下，这不是你真正想要的。由于打印机使用单一波长的光，LCD 内部的滤色器实际上吸收了可能固化树脂的光。因此，单色屏幕的 MSLA 打印机将消耗更少的能源，打印速度更快。只有一个问题:在 2020 年找到高分辨率的单色显示器并不容易。

[![](img/6a95300c8e6d4c4af0f2d134f963c642.png)](https://hackaday.com/wp-content/uploads/2020/02/monosla_detail.jpg) 因此[Jan]决定尝试用一个替换屏幕来替换他的 Elegoo Mars MSLA 打印机，并通过拆卸和手动移除滤色器来将其从彩色转换为单色。如果这听起来有点疯狂，那是因为确实如此。原来拆开一个液晶显示器，修改它的内部布局，然后把它们重新组装起来，就像你想象的那样困难*和*。

但还是值得一试。[Jan]将显示器拆开，移除液晶，刮掉彩色滤光片，然后将它们重新组装起来。他的第一次尝试让他得到了一个实际工作的单色显示器，但由于碎片被困在屏幕内，图像太差了，没有用。他又试了一次，这一次更努力地不让异物进入晶体。但是当他第二次把它组装起来时，他发现它不再起作用了。他认为可能是他清理显示器内部的尝试过于激进，但实际上有太多的事情可能会出错，很难只确定一个。

长话短说，为低成本 MSLA 打印机手动创建单色显示器可能不是一个可行的选择。在更好的解决方案出现之前，你可能会有兴趣看看[一些稍微不那么侵入性的方法来提高你的树脂印刷质量](https://hackaday.com/2019/11/12/improving-exposure-on-masked-sla-printer/)。