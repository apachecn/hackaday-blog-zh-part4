# 如何通过 HDMI 驱动智能手机屏幕

> 原文：<https://hackaday.com/2021/07/05/how-to-drive-smartphone-screens-over-hdmi/>

与大多数出售给制造商的小型液晶显示器相比，智能手机屏幕拥有出色的色彩、亮度和高得惊人的分辨率。不幸的是，驾驶它们很难一帆风顺。为了让它变得更容易， [[peng-zhihui]着手开发工具，允许从一个简单的 HDMI 馈送驱动这样的屏幕。](https://github.com/peng-zhihui/HDMI-PI)对于那些中文有些生疏的人来说，[谷歌翻译链接可能会很有用。](https://translate.google.com/translate?sl=auto&tl=en&u=https://github.com/peng-zhihui/HDMI-PI)

第一次尝试是使用东芝的 TC358870XBG ASIC，能够通过 HDMI 输入驱动 MIPI DSI 1.1 的屏幕。[peng-zhihui]基于该公司的评估板设计设计了一个简单的芯片测试模块，[与[ylj2000]一起提供软件来帮助实现该解决方案。](https://github.com/ylj2000/HDMI_To_MIPI)

[![](img/bd61aa99ed0b58b571eaf4f37b1e9885.png)](https://hackaday.com/wp-content/uploads/2021/06/Smarphone-screen-hdmi-driver-Pengzhihui.jpg) 不过，就目前来看，这个解决方案并不完善，所以【彭志辉】还试验了龙讯 LT6911 HDMI 转 MIPI 的驱动程序。虽然便宜，但有关这部分的信息很少，而且该公司自己使用硬件的源代码只能通过签署 NDA 才能获得。然而，[彭志辉]为那些希望使用硬件的人提供了预编译的固件。

[彭志辉]很好地利用了这些知识，[使用看起来像是龙讯芯片的东西建立了一个带有 MIPI 屏幕的电源库](https://github.com/peng-zhihui/PocketLCD)。该设备可以通过 USB 供电，也可以充当 HDMI 显示器。

虽然现在还为时尚早，驱动这些屏幕仍然很困难，但很高兴看到黑客们走出去，找到让新部件为他们工作的方法。我们以前见过类似的工作，使用 FPGA 而不是现成的 ASIC 。如果你找到了自己的方法让这些高端显示器工作起来，[一定要给我们写信！](http://hackaday.com/submit-a-tip)

【感谢 peterburk 的提示！]