# 如何构建自己的模拟电话网络

> 原文：<https://hackaday.com/2022/11/23/how-to-build-your-own-analog-phone-network/>

今天，模拟电话可能几乎过时了，但在为人类服务了一个多世纪之后，它们很可能会不时地出现在抽屉或阁楼上。如果你有几个这样的设备，并且你认为把它们连接起来并制作你自己的本地电话系统会很酷，那么看看[Gadget Reboot]的最新作品。他的视频系列展示了制造全功能有线电话系统的所有步骤。

当然，家庭或小型企业使用的专用电话交换机并不难找到，但[Gadget Reboot]认为从头开始设计自己的系统会更有趣。首先，他使用现成的用户线接口电路(SLICs)来实现正确的电压、电流和阻抗，以驱动模拟电话。然后，他添加了一个 DTMF 解码芯片，允许手机拨号，并将两个系统连接到一个控制整个系统的 ESP8266。它实现了接听、拨号、振铃和挂机的不同状态，并产生相应的音频信号。

通过实现多交换机布局，该系统变得更加有趣，就像在大规模电话系统中一样:当一个号码被连接到另一个交换机时，则必须在两个交换机之间建立连接才能完成呼叫。大规模系统使用 SS7 这样的专用协议，但是[Gadget Reboot]倾向于保持简单，使用 RS-485 连接。两个 esp 检查彼此的状态，如果一切正常，继电器连接两条线路，电路就完成了。

目前的系统有点乱，但它很有效，并且[Gadget Reboot]计划基于定制电路板进行更干净的设置，可能会扩展它的功能，如调制解调器支持。无论如何，它已经比简单的机电系统先进多了。想了解更多关于经典电话网络的信息吗？[我们已经为你准备好了](https://hackaday.com/2017/07/26/rotary-phones-and-the-birth-of-a-network/)。

 [https://www.youtube.com/embed/qM0ZhSyA6Jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qM0ZhSyA6Jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

