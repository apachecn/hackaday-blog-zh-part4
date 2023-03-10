# TTP223 为 LED 灯带来简单的触摸控制

> 原文：<https://hackaday.com/2022/10/04/ttp223-brings-simple-touch-controls-to-a-led-lamp/>

您可以购买带有电容式触摸检测 IC 的小模块，最常见的是 TTP223，这是一种单按钮电容式模块，具有可配置的输出模式。这些设计是为了与微控制器或一些简单的逻辑电平输入配对，但[Alain Mauer]想要的是将触摸控制带到一个简单的 LED 条上。为了不被吓倒，他组装了一个简单的基于 TTP223 的开关板。

最初，他使用常规 TTP223 板之一作为模块制作了一个原型，但随后将完整的原理图转移到一个 PCB 上。最终电路板使用一个能够处理高达 3 安培电流的 NPN 晶体管来完成开关工作，并使用基于齐纳二极管的调节从 12 V 输入为 TTP223 本身提供 5 V 电压。[Alain]分享原理图，以及 2×3 面板的 [BOM 和 Gerber 文件](https://github.com/awall9999/Capacitive-Touch-Switch-12V),以防您有兴趣将这些方便的电路板添加到您的零件箱中。

TTP223 是一款无处不在且功能强大的芯片——我们已经看到它被用来制作[一个带有低驱动力按钮的鼠标、](https://hackaday.com/2021/08/30/capacitive-mouse-built-for-a-friend-makes-for-a-touching-tale/)一个[软电源开关、](https://hackaday.com/2020/07/21/a-simple-soft-power-switch-using-common-modules/)甚至是一个[紫外线感应护身符](https://hackaday.com/2021/11/14/tiny-talisman-warns-wearer-about-uv-exposure/)，它是微型电子产品和迷人的金属制品的同等组成部分。

 [https://www.youtube.com/embed/Rd30Y7E_KMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rd30Y7E_KMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

