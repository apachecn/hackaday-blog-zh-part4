# Adafruit AVRProg 增加了对 UPDI 接口的支持

> 原文：<https://hackaday.com/2021/11/08/adafruit-avrprog-grows-updi-interface-support/>

使用嵌入式应用程序制作少量东西非常简单，您通常只需使用适当的适配器电缆将编程器或调试器加密狗(如 AVRISP2)插入您的主板，将代码加载到任何适合该设备的 IDE 工具中，然后点击程序按钮。但是，当你把规模扩大到数百或数千台时，这种工作方式就不够了。添加任何你需要的功能性或面向缺陷的测试，你将需要一个定制的编程装备。

Adafruit 在构建嵌入式主板和处理适当的测试和编程方面有相当多的经验，现在他们已经更新了他们的 [AVR 编程库](https://github.com/adafruit/Adafruit_AVRProg)，以支持已经转移到 [UPDI(统一编程和调试接口)编程接口](https://onlinedocs.microchip.com/pr/GUID-DDB0017E-84E3-4E77-AAE9-7AC4290E5E8B-en-US-4/index.html?GUID-9B349315-2842-4189-B88C-49F4E1055D7F)的最新设备。UPDI 是一种单线双向异步串行接口，支持在 Microchip 的大量新型 AVR 品牌器件上编程和调试嵌入式应用。一个例子是 [AVR128DAxx](https://www.microchip.com/en-us/product/AVR128DA48) ，这位抄写员最近一直在摆弄它，因为它很便宜，具有出色的电容触摸支持，并提供原型友好的 28 引脚 SOIC 封装，使其易于焊接。

该库旨在与 Arduino 平台一起使用，所以它应该可以在大量硬件上运行，没有任何特殊要求，所以用我们很多人都有的硬件制作一个定制的编程夹具并不是一件大麻烦。

Adafruit 在 GitHub 项目中提供了几个应用示例来帮助您，例如[这个 ATTiny817 示例](https://github.com/adafruit/Adafruit_AVRProg/tree/master/examples/attiny817_updiprog)可以擦除闪存、设置适当的保险丝并插入引导加载程序。

UPDI 代码取自中国装备 LilyGo 的[【brandan lane 的】portprog](https://gitlab.com/bradanlane/portaprog)，该软件位于 [TTGO T-Display](http://www.lilygo.cn/prod_view.aspx?Id=1126) ESP32 板上，也值得一试。

不久前，我们看到了 AVR Multitool，[AVR GPP 如何学习说 UPDI](https://hackaday.com/2020/07/02/avr-multi-tool-learns-the-latest-tricks/) ，并且由于我们是在编程接口上，它有可能让[廉价芯片 USBasp 也说 TPI 语](https://hackaday.com/2021/05/03/teaching-a-usbasp-programmer-to-speak-tpi/)。

 [https://www.youtube.com/embed/sXSll5yI22Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sXSll5yI22Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

