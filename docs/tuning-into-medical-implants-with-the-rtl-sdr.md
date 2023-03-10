# 利用 RTL-SDR 调谐至医疗植入物

> 原文：<https://hackaday.com/2021/07/11/tuning-into-medical-implants-with-the-rtl-sdr/>

运气好的话，你的一生都不需要植入医疗设备。但是如果你*真的*最终得到你的医生将在你体内安装一个有源发射器的消息，你还不如破解软件无线电(SDR)和[看看你是否能像【伍沾德】最近做的那样解码它的传输](https://analogist.net/post/decoding-radio-ph-capsules-with-rtl_433/)。

在美敦力 Bravo 反流胶囊连接到他的下食道之前，[詹姆斯]仔细观察了铅笔宽度的小工具的演示单元。尽管医疗技术人员告诉他，该设备使用“类似蓝牙”的通信协议将他的食道 pH 值传输到可穿戴接收器，但硬件上醒目的 433 让他认为值得仔细看看文档。果然，它在 FCC 数据库中的条目不仅确认了无线电发射了 433.92 MHz OOK-PWM 编码信号，而且它甚至分解了每个包的内容。要是一直这么简单就好了，对吧？

[![](img/9961022b35383cb486a4d8b1644c9d48.png)](https://hackaday.com/wp-content/uploads/2021/07/bravoph_detail2.jpg)

The 433 ended up being a coincidence, but it got him on the right track.

当然，他仍然必须将这些信息付诸实践，所以下一步是为流行的`rtl_433`程序制作一个配置文件，该程序将每个数据包分成其主要部分。对于那些可能希望从自己的 433 MHz 传感器(医疗或其他)获取数据的人来说，这部分内容尤其有趣

不幸的是，仍然有一块拼图丢失了。[James]知道哪个字段是 FCC 数据库中的 pH 值，但他收到的 16 位整数没有任何意义。在对硬件进行进一步研究后，他发现了 RTL-SDR 项目早期的另一种解码传输的尝试，他意识到他实际上看到的是同时发送的两个 8 位 pH 测量值的组合。

我们惊喜地看到[詹姆斯]能够找到多少关于美敦力 Bravo 反流胶囊的公开信息，但在一个完美的世界里，这将是常态。你应该知道关于一件将被放置在你体内的电子设备的一切，但迄今为止，朝向开放硬件医疗设备的[运动](https://hackaday.com/2018/01/30/making-the-case-for-open-source-medical-devices/)一直难以获得更多的牵引力。