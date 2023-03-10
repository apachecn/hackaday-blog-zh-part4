# 路由器重新启动不费吹灰之力

> 原文：<https://hackaday.com/2019/11/02/router-rebooter-without-the-effort/>

这是我们这个时代的惯例之一，当带宽变得不稳定时，重启家庭路由器。打开电源，大约半分钟后，你的 YouTube 视频又开始播放了。消费级路由器硬件不是你将拥有的最可靠的计算设备，正如[Nick Sayer]在他度假屋的路由器不够可靠以支持他的远程监控设备时发现的那样。他的解决方案是[一个自动重启设备](https://hackaday.io/project/168150-reboot-o-matic)，它根据命令重启有问题的设备。

一个显而易见的方法可能是切换主电源，但他采取了更简单的选择，即通过三个 MOSFETs 的巧妙安排，将 DC 从路由器的壁式电源切换到其他电源，以保持路由器在任何情况下都默认打开，除非它被监督它的 ATtiny 微控制器命令关闭。该芯片提供额外的故障安全和去抖动功能，以确保不会意外重启。

驱动电路的是一个处理房屋监控的 Raspberry Pi，Python 脚本在其上检查互联网访问，如果没有，就要求重启。为了额外的安全，在路由器固件升级的情况下，在这样做之前，它需要访问一段持续的时间。

这并不是第一个路由器重连器，对于一个电源开关 ESP8266 来说[看看这个](https://hackaday.com/2018/01/31/router-rebooter-eliminates-hassles/)。

路由器图片:Asim18 [ [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:ADSL_router_with_Wi-Fi_(802.11_b-g).jpg)