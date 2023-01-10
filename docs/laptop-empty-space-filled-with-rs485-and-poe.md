# 充满 RS485 和 PoE 的笔记本电脑空间

> 原文：<https://hackaday.com/2022/01/05/laptop-empty-space-filled-with-rs485-and-poe/>

在所有通常可用的笔记本电脑升级选项中，您不会想到这个特定的选项。[controlmypad]决定将他的 RS485 设备编程工作流程的一部分,[放入他廉价购买的备用笔记本电脑](https://hackaday.io/project/6964-laptop-with-on-board-poe-rs485)中。通常，他会占用一些桌子空间，并布置一个笨拙的组合，包括 USB-RS485 加密狗、PoE 电动注射器、注射器的 PSU 和几根连接它们的电缆——在工具袋中是额外的重量，布置时会弄乱工作空间，RS485 适配器在与工作相关的运动中会慢慢磨损 USB 端口。然而，没有理由说所有这些不能装在一台笔记本电脑里。

非常有用的是，在许多现代廉价笔记本电脑中，主板相当小，可以毫不犹豫地省略 DVD 驱动器塑料占位符。从两个适配器上切掉塑料模制件后，它们分别变成了一个可重复使用的电路板和一个小型 PoE 模块。在用业余爱好刀费力而小心地切割笔记本电脑外壳后，PoE 注射器正好适合，本质上，给笔记本电脑增加了一个额外的 RJ45 端口。从 Hackaday.io 文章停止的地方看，这个 mod 似乎没有完全完成，但大多数重要的细节都可供我们借鉴。被遗漏的是将其连接到内部 USB 端口(应该有助于主板的原理图在线提供)，以及从笔记本电脑的电源轨产生 12V-24V。然而，在这一点上，这个 mod 在可用性方面向前迈进了一大步，即使它仍然需要一个外部 PSU。

笔记本电脑内部升级项目很少，但很珍贵——它是“大胆”、“好奇”和“一丝不苟”的结合，使人们成功地侵入了他们肯定不打算侵入的东西，并让那个东西更好地服务于他们的需求。除了[所有为一代笔记本电脑改装者设立了标杆的 EEE PC 升级选项](https://hackaday.com/2008/01/19/add-everything-to-your-eeepc/)之外，还有无数非常规的笔记本电脑改装途径——你可以[从零开始进行彻底的 C 型充电端口改装](https://hackaday.com/2021/02/03/a-usb-pd-laptop-conversion-in-extreme-detail/)，用 FSF 认可的开放固件 WiFi 加密狗替换你的网络摄像头[，在](https://hackaday.com/2018/06/13/chromebook-trades-camera-for-wi-fi-freedom/)[中内置一个用于自动定向](https://hackaday.com/2013/01/31/12-axis-sensor-adds-auto-screen-orientation-to-this-older-tablet-pc/)和数据记录的“12 轴”传感器[，或者为你的笔记本电脑发明一个远程自毁机制](https://hackaday.com/2015/09/22/dont-steal-this-laptop/)。事实上，在制造商网站上定制笔记本电脑时，你通常不会在可用选项列表中找到这些东西。