# 让您的微控制器以光速在线

> 原文：<https://hackaday.com/2020/04/28/get-your-microcontroller-online-at-the-speed-of-light/>

当使用 ESP8266 或 ESP32 开发支持网络的项目时，处理 WiFi 凭证的最简单方法是将接入点和加密密钥硬编码到程序中。但这意味着如果你想在不同的网络上使用它，就要重新编译固件，如果你想做一些其他人可以轻松使用的东西，这真的不是一个选项。如果你在期待奶奶拔掉 UART 电缆，我们有坏消息要告诉你。

围绕这个问题有各种各样的方法，但我们认为[Pekka Lehtikoski]开发的方法特别聪明。通过一个简单的应用程序，[网络凭证可以通过快速闪烁 Android 设备上的闪烁 LED 来“闪现”到等待的微控制器](https://iocafe.org/989-2/)。这使得无论用户的技术熟练程度如何，信息都可以被快速且容易地传送。有人甚至可以说，它比其他一些进行初始设置的方法更安全，因为如果窃听者想窃取你的加密密钥，他们真的需要看到你这样做。

[![](img/396c5c59ddfb57473bf57f9c111a04ca.png)](https://hackaday.com/wp-content/uploads/2020/04/gazerbeam_detail.jpg)【PE kka】已经将 Android 应用程序的源代码和“Gazerbeam”库开放给任何想在自己的项目中包含该功能的人。要接收闪烁的光，你只需要在电路中增加一个光电晶体管、一个运算放大器和一些无源器件；使这个解决方案足够便宜，甚至可以在小规模生产中使用。这个概念也不限于网络凭证。每当我们再次举行会议时，让与会者定制他们的徽章可能是一种有趣的方式。

当然，[Pekka]并不是第一个用这一招的人。精通 WiFi MCUs 历史的黑客可能会记得，电动 Imp [使用了一种非常类似的配置方法，称为 BlinkUp](https://hackaday.com/2012/09/04/hands-on-with-the-electric-imp/) 。如果你遇到一个设备，要求你把手机屏幕放在一个小窗口上进行初始设置，[很有可能它里面有一个小恶魔](https://hackaday.com/2019/04/30/teardown-refuel-propane-tank-monitor/)。