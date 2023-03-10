# 新零件日:最小的 ARM MCU 根除竞争，需要研究

> 原文：<https://hackaday.com/2022/03/01/new-part-day-smallest-arm-mcu-uproots-competition-needs-research/>

【Cedric】联系过我们，告诉我们[他见过的最小的 ARM MCU](https://twitter.com/CedHon/status/1495190668435722241)–华大 [HC32L110](https://www.hdsc.com.cn/Category82-1393) 。对于我们这些喜欢微型产品的人来说，这种 Cortex-M0+封装集 [(PDF 数据表)](https://hdsc.com.cn/cn/Index/downloadFile/modelid/65/id/8/key/0)于一身，将低功耗、高性能和丰富的外设封装在一块 1.6 毫米 x 1.4mm 毫米的可焊接硅中。

这是火柴头规模的计算，比我们以前在这样的规模下所能获得的能力要大得多，正等着被争论。与同样采用 WLCSP 封装的 8 位 ATTiny20 相比，这是一个显著的规格提升，它拥有更强大的 CPU、16 倍的 RAM 和 8-16 倍的闪存！更不用说[第一季度的 1 美元一个](https://item.szlcsc.com/897254.html)，这大约是一个 20 英镑的价格。作为一个 0.35 毫米间距的 16 引脚 BGA，你的典型板屋可能不会很满意你，但一旦你得到了一个电路板 fabbed，并从一个 fab 交付值得他们的盐，一点印刷和回流将让你在任何时候开发板。

弊端？没有英文数据表或者 Arduino 端口，我们找到的 67 页 PDF 也没有一些寄存器映射之类的东西。LILYGO [承诺](https://twitter.com/lilygo9/status/1495771839284801537)他们将很快开始销售开发板，但我们确信开发自己的开发板并不难。从那以后，我们希望[能产生类似 ESP8266 的效果](https://hackaday.com/2014/08/26/new-chip-alert-the-esp8266-wifi-module-its-5/)——缺失的信息被一点一点地拼凑、翻译并变得容易获取。

当焊接这种小封装时，我们强烈推荐回流焊接。然而，如果你决定[走磁线路线](https://hackaday.com/2013/07/03/hand-soldering-bga-wafer-chips/)，我们不敢反对——只要确保给我们发照片。毕竟，像 ATTiny20 这样的微型微控制器似乎有足够的吸引力，以至于[的人们会选择最疯狂的路线](https://hackaday.com/2018/06/26/no-caffeine-no-problem-a-hand-soldered-chip-scale-package/)来玩一把。他们说，勇敢者的疯狂是生活的智慧。

我们感谢[【Cedric】](https://hackaday.io/cedric)与我们分享这些！