# 穹顶下的钟

> 原文：<https://hackaday.com/2020/10/25/the-clock-under-the-dome/>

在只能被描述为艺术作品的作品中，[【sued bunker】在玻璃穹顶下创造了一个时钟](https://hackaday.io/project/175446-dome-clock)。运动谢妮管，DS3223，BCD 编码器，以及由 MCP23008 I/O 扩展器驱动的 MPSA43 晶体管，这确实是一个值得一看的景象。[suedbunker]之前创造了[马戏团时钟](https://hackaday.com/2018/01/03/celebrate-display-diversity-for-a-circuit-circus-clock/)，一种类似的时钟，庆祝时间显示方式的多样性。

圆顶钟代表了这一理念的延续。读时钟需要分别看水平和垂直数字。水平方向是小时，垂直方向是分钟。背面的霓虹灯代表周一至周日。底部的电源为各种类型的灯提供各种电压，包括 5 V、12 V、24 V、45 V、90 V、150 V 和-270 V。为了安全起见，在-270 伏上使用光耦合器来驱动清晰的七段显示器。

Arduino Nano 通过 I2C 与 DS3232 实时时钟模块和端口扩展器通信来控制整个时钟。尤其是焊接和布线工作，既整洁又美观。我们期待着[suedbunker]和他妻子的未来时钟。

 [https://www.youtube.com/embed/qk7Pl5d1Tog?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qk7Pl5d1Tog?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

