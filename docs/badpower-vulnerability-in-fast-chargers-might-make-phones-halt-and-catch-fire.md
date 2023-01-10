# 快速充电器中的 BadPower 漏洞可能会导致手机停机并起火

> 原文：<https://hackaday.com/2020/07/22/badpower-vulnerability-in-fast-chargers-might-make-phones-halt-and-catch-fire/>

几天前，来自科技巨头腾讯的中国研究人员发布了一篇论文，概述了几种快速充电器电源模块的固件漏洞。这种攻击被称为 BadPower，它通过改变快速充电器固件中的默认参数来为设备提供超过其处理能力的电力，从而导致设备过热、熔化或着火。

古老而基本的 USB 充电规格在 5 V 时提供 0.5 A，相当于 2.5 W。理论上，这是这些类型的充电器所能提供的全部功率。但是新一代充电器就不一样了。当你将手机插入快速充电器时，它会在给手机充电前与手机协商电压和充电速度。

快速充电器可以在 20 V 或更高的电压下供电，以加快充电过程，具体取决于充电器和连接的设备。如果手机不做快充，就默认 5 V 标准。研究人员声称，BadPower 攻击能够损害设备，无论它们是否包括快速充电功能。当连接了有能力的设备时，充电器仍然会协商 5V，但却给出 20V 并肆虐。

在休息后的演示中，其中一个团队使用伪装成手机的恶意设备将 BadPower 固件更改为连接到电压表的快速充电器。发作前充电器给 5V。攻击后，它给出 5V 电压几秒钟，然后上升到 20V 附近。然后他们把现在已经脏了的充电器连接到两个相同的发光放大镜上。其中一个芯片释放烟雾怪物相当猛烈，另一个芯片发出火花。

研究人员测试了目前市场上 200 多种快速充电砖中的 35 种，发现其中 18 种容易受到 BadPower 的攻击，其中 11 种可以通过充电端口本身被利用。他们认为这个问题可以通过固件更新来解决。

目前还没有足够的信息来验证这项研究，也没有易受攻击的品牌/型号列表。研究人员表示，这些发现已于 3 月 27 日提交给中国国家漏洞数据库(CNVD)，因此这些信息的缺失可能是制造商需要更多时间来修补漏洞的产物。

你怎么想呢?我们说，半路出家的充电器不应该对它们正在充电的设备的固件攻击开放。任何像样的手机都应该内置电子保护，对吗？

 [https://www.youtube.com/embed/Es2SqubYSfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Es2SqubYSfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [ZDNet](https://www.zdnet.com/article/badpower-attack-corrupts-fast-chargers-to-melt-or-set-your-device-on-fire/)