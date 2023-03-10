# 开放硬件峰会的精美徽章

> 原文：<https://hackaday.com/2018/09/27/the-exquisite-badges-of-open-hardware-summit/>

过去几年都是关于电子会议徽章，今年也不例外。现在，我们正在麻省理工学院举办[开放硬件峰会](https://2018.oshwa.org/)，今年的徽章绝对非同寻常。这是一个支持 WiFi 和蓝牙的电子纸徽章，为每位与会者单独编程。2018 年开放硬件峰会徽章是一件艺术品，它都是在 hackaday.io 上[创作的。](https://hackaday.io/project/112222-2018-open-hardware-summit-badge)

该板基于由[Mike Rankin]设计的 [ESP 小饰品](https://github.com/mike-rankin/ESP_trINKet)和来自[Alex Camilo]的额外硬件设计。该徽章基于 ESP32-wroom-32 模块，配有分辨率为 250 x 122 像素的 2.13 英寸电子纸显示屏。对此，徽章增加了一个 I2C 加速度计和对附加设备的[支持](https://hackaday.io/project/52950-shitty-add-ons)。还有用于 SD 卡支架的焊盘——如果你愿意，这是一个焊接挑战——以及一些用于比特和 bob 的额外焊盘。

但是没有软件，徽章什么都不是，这就是它真正变好的地方。ESP32 模块是一个发电站，能够模拟 NES 游戏或作为文件服务器。在这里，徽章的常用配置相当简单:您可以启动一个 WiFi AP，登录到一个网页，然后更改徽章上显示的名称。你也可以启动一个 FTP 服务器，这是非常有趣的事情。在 FTP 服务器上放下一个应用程序，[就可以运行微 Python](https://hackaday.io/project/112222-2018-open-hardware-summit-badge/log/153395-micro-python-firmware-on-ohs-18-eve) 。

### 徽章是伟大的，但编程夹具是*可怕的*

电路板是通过奥什公园制作的，尖叫电路负责组装。任何曾经制作过徽章的人都会告诉你，不是装配让你得到了它，而是编程和供应。这一点尤其正确，因为开放硬件峰会徽章分发时已经预先加载了与会者的姓名。那是几百个徽章，都有独特的固件。从任何角度来看，这都是一场噩梦。

然而，问题总有好的解决方案，来自奥什公园的[Drew]在 Artisan's 疯人院的峰会赛前向我展示了我见过的最好的编程夹具。

 [![IMG_20180926_191039](img/c9d6612f3d27da659279408a75a99481.png "IMG_20180926_191039")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180926_191039.jpg?ssl=1)  [![IMG_20180926_191110](img/dfca0aa85e3e969b1028f4947ea6085c.png "IMG_20180926_191110")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180926_191110.jpg?ssl=1)  [![IMG_20180926_191141](img/002a4d4d61afbe23f233473f3a37b58a.png "IMG_20180926_191141")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180926_191141.jpg?ssl=1)  [![IMG_20180926_191146](img/2d50a8f9ffa312926506a9674b97f6cc.png "IMG_20180926_191146")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180926_191146.jpg?ssl=1)  [![IMG_20180926_191002](img/5baa3da2dd40263ffd3ded33990f1aa8.png "IMG_20180926_191002")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180926_191002.jpg?ssl=1) 

你现在看到的是一个 3D 打印的盒子，里面装有触摸屏显示器、一个 Raspberry Pi Zero W 和几个弹簧针。这个 Raspberry Pi 通过连接到互联网，下载当前版本的固件，并将该固件加载到徽章上来完成所有繁重的工作。由于有了触摸屏界面，还有更多的选项，包括为所有徽章提供与会者的姓名——这可以通过读取与会者列表并将下一个人上传到夹具中的徽章来完成。所有这些都包裹在一个漂亮的激光切割盖中，它可以安全地将每个徽章*准确地*固定在弹簧针需要接触的地方。

毫无疑问，这是我见过的最好的编程夹具。任何徽章制作者都应该注意:这就是你如何编写几百个徽章的程序。徽章本身就很棒，就在这篇文章发表的时候，将会有数百名热切的黑客对这个非凡的硬件无所事事。如果你想了解徽章破解的最新进展，[查看 Twitter 上的更新](https://twitter.com/ohsummit)