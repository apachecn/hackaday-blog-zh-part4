# 为您的下一个项目安装一个 I2C 导航键

> 原文：<https://hackaday.com/2019/04/11/a-bolt-on-i2c-navigation-key-for-your-next-project/>

我们经常在 Hackaday 谈论模块化硬件的优势；只需在线订购一些零件，用一些跳线将它们连接起来，然后转移到软件方面，这种能力对于原型制作来说是一种巨大的时间节省。因此，每当我们看到一个新的模块，将节省我们的时间和恶化的道路上，我们变得有点兴奋。

今天，我们向您展示由[赛蒙] 开发的非常精巧的 I2CNavKey，这是一个为您的构建提供的交钥匙接口解决方案，它无法通过几个拨动开关来实现。它不仅给你一个带中央按钮的四向方向键，还有一个像旧 iPods 那样的旋转“轮子”。得益于 I2C 的奇迹，您可以通过最少的布线轻松到达所有这些地方。

[![](img/94b35a199eca38062d959c06da070617.png)](https://hackaday.com/wp-content/uploads/2019/04/navkey_detail.jpg) 但即便如此，也可能是在卖空该模块。这不仅仅是分线板上的几个按钮，I2CNavKey 由自己的 PIC16F18345 微控制器供电，具有三个可配置的 GPIOs，支持 PWM(非常适合 RGB LED ),外加 256 字节的板载 EEPROM 存储。

[赛蒙]已经将整个项目作为开源硬件发布，以满足你的黑客乐趣，但你也可以在 Tindie 上以 18 美元的价格获得现成的模块[。无论您是否是付费客户，您都可以访问该项目的绝对非凡的文档，包括近 30 页的手册，其中包含您想要了解的关于 I2CNavKey 以及如何将其集成到您的项目中的所有信息。如果所有的硬件都以这种奉献精神被记录下来，对于像我们这样的人来说，这个世界将会变得更加美好。](https://www.tindie.com/products/Saimon/i2c-navkey-7-functions-joypad-on-the-i2c-bus/)

如果你认识这个名字，或者也许是对整洁的 I2C 连接输入设备的喜爱，这可能是因为[你以前在这些页面上见过他非常相似的 I2C 旋转编码器](https://hackaday.com/2018/04/15/rotary-encoders-become-i2c-devices/)，这是[在 2018 年 Hackaday 奖](https://hackaday.com/2018/05/02/these-twenty-amazing-projects-won-the-open-hardware-design-challenge/)期间参加我们*开放硬件设计挑战赛*的决赛。