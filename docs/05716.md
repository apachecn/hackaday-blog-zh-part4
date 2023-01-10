# 密码管理员使用现成的外形

> 原文：<https://hackaday.com/2020/02/19/password-keeper-uses-off-the-shelf-formfactor/>

如今，每个网站都要求创建一个账户，记住这么多登录信息会变得很困难。理想情况下，每个密码都应该是唯一的，以免你幻想中的足球游戏泄露，导致你损失数千个被盗的比特币。为了提供帮助，[vcch]使用一个有趣的现成平台开发了一个密码库。

[问题中的平台是 M5stickC，](https://www.banggood.com/M5StickC-ESP32-PICO-Color-LCD-Mini-IoT-Development-Board-Finger-Computer-p-1476576.html?akmClientCountry=AU&)它将 ESP32、彩色 LCD 和电池包装在一个吸引人的橙色外壳中。它甚至有 USB-C，使它成为一个着眼于未来的工具。它是一种快速启动和运行基本 IOT 项目的方法，而不必为设计自己的机箱或基本电源硬件而烦恼。

在这个平台上，[vcch]创造了一个工具，使跟踪密码变得容易。这款名为 PassStrong 的电脑可以存储大量密码，并通过蓝牙与主机进行通信。该界面充分利用了 LCD，为用户显示设备上每个按钮的当前模式和功能。它能够在 QWERTY 和 AZERTY 环境下工作，这应该会吸引欧洲用户。

在这方面，M5StickC 是一个完美的选择，它打包了足够的按钮和所需的蓝牙硬件来完成工作。无需花费任何时间来集成模块——只需打开盒子，开始编码。我们期望在未来看到这一领域的更多发展，并期待这将为各种项目带来效率的提高！