# 索尼 ScopeMan 可能是他们从未生产过的最好的产品

> 原文：<https://hackaday.com/2021/01/21/the-sony-scopeman-possibly-the-best-product-they-never-made/>

从未来十年的角度来看，回顾过去时代的欲望的技术对象有时是古怪而有趣的。例如，在 20 世纪 80 年代，手持电视是成就的顶峰，在这十年中，随身听取代了晶体管收音机成为首选的袖珍小玩意，似乎视觉娱乐肯定会紧随其后。多家制造商加入了提供的口袋电视的范围，索尼公司采用的格式使用了一种扁平的 CRT，带有一个有角度的荧光屏，从后面透过玻璃外壳可以看到。[Niklas Fauth] [用一台索尼 Watchman 设备替换了它的电视电路板，使它变成了矢量显示器](https://github.com/NiklasFauth/sony-scopeman)。索尼 Scopeman 诞生了！

原理图看似简单，ESP32 通过蓝牙接收音频，并通过一对运算放大器和一组驱动晶体管驱动偏转线圈。这些电路很难弄对，在这个[中，他承认了他的灵感](http://www.e-basteln.de/file/asteroids/Vectrex_XY_Driver.pdf)。同时该软件有两个可选功能:一个相当传统的 [X-Y 矢量的范围显示](https://twitter.com/FauthNiklas/status/1337467949318279170)和[洛伦兹吸引子算法](https://twitter.com/FauthNiklas/status/1339650704584171522)。当然，它还可以[显示我们扳手标志的矢量版本](https://twitter.com/FauthNiklas/status/1349538538149335042)。

我们喜欢 Scopeman，事实上我们非常喜欢它。对于复古技术纯粹主义者来说，这可能会有些不适，因为它依赖于屠宰一个老式的守夜人来进行操作，但我们会注意到模拟广播电视的消亡已经使守夜人变得无用，并且还有一个死亡的守夜人可以用于转换项目的前景。

[Niklas]有不止一个项目出现在这些页面上，一个令人难忘的例子是[他的 PCB 特斯拉线圈](https://hackaday.com/2019/04/25/a-tesla-coil-from-pcbs/)。