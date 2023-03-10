# 给旧收音机带来现代控制

> 原文：<https://hackaday.com/2021/01/11/bringing-modern-control-to-an-old-radio/>

现代业余无线电室可以有多种形式。有些是古代“船锚”收音机的圣地，因其重量相当大而得名。其他的只是一个小小的、不起眼的连接到笔记本电脑上的软件无线电(SDR)。现在很多窝棚倒在中间的某个地方。在一个古老的 Hallicrafters SX-115(听起来很像作者的装置)上面放着一个光滑的 Icom IC-7300 并不少见。当业余爱好者想要使用 FT-8 等数字模式时，他们无疑会选择配备 USB(在这种情况下是通用串行总线，而不是上边带)设备控制的新型收音机，但如果他们拥有的最新设备是一台 30 年前的 Kenwood 牌收音机呢？

如果这听起来像你，那么不要害怕，因为(史蒂夫·博塞特)已经报道了你。他带着他值得信赖的 Kenwood TS-50，这是一款 1993 年的经典收音机，其最先进的功能是模糊逻辑，[用 USB(也是串行总线)控制](https://hvdnnotebook.blogspot.com/2021/01/hacking-in-usb-cat-control-to-kenwood.html)对其进行了升级。

当肯伍德设计 TS-50 时，他们考虑的是计算机控制。该装置底部有一个隐藏的端口，露出一个连接器，与 Kenwood 专有的(也是昂贵的)串行控制电缆相匹配。令人欣慰的是，肯伍德的工程师们决定使用 UART 进行 PC 通信，因此在收音机的外壳上安装 USB 端口并不像听起来那么令人生畏。[史蒂夫]拿起一个 [CP2104 USB-TTL UART 串行适配器](https://smile.amazon.com/gp/product/B071SM35YZ/ref=ppx_yo_dt_b_asin_title_o07_s00?ie=UTF8&psc=1)并将其连接到无线电的控制端口。经过一些钻孔、拧紧和粘合，收音机有了升级(非专利！)接口兼容一直流行的 hamlib。虽然这并没有涵盖所有的无线电控制功能，但它让你调谐，这是非常重要的。为了获得完全现代化的无线电体验，[Steve]建议使用 8 针麦克风连接器和接口，如 Rigblaster 或 Signalink。这增加了 PTT 和音频信号路由。

如果你想自己尝试一下，一定要看看[Steve]的记录极其丰富的文章。你甚至可以更进一步，用我们几个月前看到的这个 [HTML5 界面从你的智能手机上控制你的 TS-50。](https://hackaday.com/2020/10/24/radio-remote-control-via-html5/)