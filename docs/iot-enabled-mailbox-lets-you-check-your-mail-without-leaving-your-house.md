# 支持物联网的邮箱让你足不出户就能查看邮件

> 原文：<https://hackaday.com/2022/02/24/iot-enabled-mailbox-lets-you-check-your-mail-without-leaving-your-house/>

无论你住在市中心的公寓里还是郊区的独立式住宅里，如果你的邮箱没有安装在家里，你就必须到外面去看看有没有东西。但是当你发现你的邮箱是空的时，你如何避免那种可怕的失望感呢？嗯，我们生活在 2022 年，所以今天你的邮箱只是另一个连接物联网的东西。这正是[fhuable]在制作太阳能物联网邮箱时所做的事情。

基本的想法是给邮箱安装一个摄像头，让它发送邮件内容的图片。一个 ESP32-Cam 模块可以做到这一点:使用 1600 x 1200 的摄像头传感器，160 MHz 的 CPU 和集成的 WiFi 适配器，[fhuable]只需要编写一个 Arduino 草图，让它每隔几个小时拍摄一张照片，并上传到 FTP 服务器。

[![A pile of components making up an IoT Mailbox](img/272b8c805a4311ce7e59756b655fdb98.png)](https://hackaday.com/wp-content/uploads/2022/02/IoT-Mailbox-components.png)

The components inside: a solar cell, battery, power controller, LDO and ESP32-Cam module with WiFi antenna

但是，由于从家里一路走一条长电缆并不是一个有吸引力的选择，整个模块必须完全无线。[fhuable]决定使用一个 18650 锂离子电池为其供电，该电池通过安装在邮箱顶部的 1.5 W 太阳能电池板不断充电。其他部分装在一个完全密封的 3D 打印外壳中，以防止潮湿。

外壳必须由在阳光直射下不会降解的材料制成，这就是为什么[fhuable]决定尝试使用 as 灯丝；这应该对紫外线有很强的抵抗力，但事实证明这很难加工。它在冷却过程中扭曲得如此厉害，以至于从打印机中取出一块固体的唯一方法是将整个机器封装在一个纸板盒中，以保持其内部温暖。

最终的结果是值得的:在邮箱的背面有一个整洁的小扩展，只要阳光继续照耀，它就可以继续发送内部的照片。相机还应该给出关于邮箱内容的良好指示，允许用户忽略任何垃圾邮件；这是对以前物联网邮箱的有益改进，以前的物联网邮箱使用[接近传感器](https://hackaday.com/2019/11/30/youve-got-mail/)、[微动开关](https://hackaday.com/2020/02/15/aaa-powered-lora-mailbox-sensor-goes-the-distance/)或[光学传感器](https://hackaday.com/2016/11/15/waiting-for-a-letter-this-iot-mailbox-will-tell-you-exactly-when-it-arrives/)。

 [https://www.youtube.com/embed/QnxEXPgSWag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QnxEXPgSWag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

