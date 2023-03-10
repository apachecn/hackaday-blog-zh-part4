# 使用 ESP8266 的 DIY 喷水控制器

> 原文：<https://hackaday.com/2019/05/18/a-diy-sprinkler-controller-using-an-esp8266/>

依靠云的喷水系统的想法有一点奇怪的有趣之处。但是，正是一些商业产品的这种局限性导致[Zack Lalanne]在需要升级他的老化灌溉器时创造了他自己的控制器。

这是一个足够简单的设备，他在无处不在的 NodeMCU 板上采用了 ESP8266，并添加了一个移位寄存器，用于一些输出线路扩展，以驱动一组继电器。这里的兴趣[在于软件](https://selfhostedhome.com/diy-wifi-sprinkler-controller-using-esp8266-part-2/)，他在其中使用了 ESPHome 固件，并为移位寄存器添加了他自己的定制部分。仅这一改变就应该对许多其他使用‘8266 和 ESPHome 组合的实验者有用。

该设备的 ESP8266 端与他的[家庭助理](https://www.home-assistant.io/)家庭自动化中枢软件的实例相结合。在这一点上，他已经能够将他添加的所有各种喷头输出结合起来，并应用他选择的任何自动化脚本。结果是新浇过水的草坪，天空(或后端)没有一丝云彩。

这个项目的价值仅部分在于它对自动喷水装置所有者的使用，对我们来说，它还在于为其他有类似家庭自动化任务的人指明了道路。这不是制作 ESP 洒水控制器的唯一方法，[你还应该看到 2017 年的这个](https://hackaday.com/2017/09/05/diy-wireless-sprinkler-system-dont-mind-if-i-do/)。