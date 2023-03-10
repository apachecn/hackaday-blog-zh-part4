# 最小的分立晶体管 555 定时器

> 原文：<https://hackaday.com/2021/05/11/smallest-discrete-transistor-555-timer/>

在微型晶体管实验室，[Robo]以分立晶体管的形式[复制了经典的 555 定时器](https://www.tinytransistors.net/2021/05/06/the-tt555-a-discrete-555-timer-plug-in-replacement/)。为了加分，他还设法将它放在一个基本尺寸相同的包中，与 pin 兼容，并且是原版的插件替代品。第一项任务是决定采用哪种 555 电路。他研究了一些不同的实现——所谓研究，我们的意思是[解剖了它们，并在显微镜下研究了芯片电路](https://www.tinytransistors.net/2021/04/24/the-555-timer/)。最终，他选择了 Hans Camenzind 的原始电路，这既是一种致敬，也是因为它使用了最少的晶体管，这有助于管理最终的尺寸，仅比 IC 大一点点！

说到尺寸，你焊接过 EIA 01005 电阻吗？我们同意[mbedded.ninja]在一篇关于标准芯片电阻尺寸的文章中所写的观点，01005 是一种“肉眼几乎看不到的小得可笑的芯片封装”它的尺寸为 16000 x 8000(0.4 毫米 x 0.2 毫米)，尽管它的名称和位置在 Imperial 系列中，但它的尺寸还不到 an 0201 的一半。晶体管是标准的 2N3904 / 2N3906，但购买时采用非标准的 DFN 封装(双扁平封装，无引脚)。我们可能认为 1.0 x 0.6 mm 的元件很小，但与电路中的相邻电阻相比，它就很大了。

[Robo]以前做过这种项目，最近对经典的 741 运算放大器进行了[离散再造。早在 2011 年，我们就报道过一个类似的，但是更大的，](https://www.tinytransistors.net/2021/03/22/the-tt741-a-discrete-plug-in-741-replacement/)[离散 555 定时器项目](https://hackaday.com/2011/02/25/building-a-555-timer-from-discrete-components/)。如果你想真正大规模地进行自己的繁殖项目，可以看看五年前的[怪兽 6502](https://hackaday.com/2016/05/24/how-the-dis-integrated-6502-came-to-be/) 来获得更多的灵感。感谢[卢卡斯]的提示。