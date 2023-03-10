# 以现代方式重置您的路由器

> 原文：<https://hackaday.com/2019/01/03/reset-your-router-the-modern-way/>

许多 Hackaday 读者将在假期结束后回到他们的生活中，与太多各式各样的亲戚一起挤在某个家庭女家长的房子里，放弃了他们的快速互联网连接，转而使用奶奶住的地方的宽带。电话公司提供的廉价路由器将会在一群青少年在 YouTube 上观看其他青少年的无聊行为的压力下枯萎，重置路由器的圣诞节仪式将会进行多次。

[![A very simple schematic for the resetter.](img/14a5ab5382b4acdbb0d3844e33aa51b3.png)](https://hackaday.com/wp-content/uploads/2019/01/resetter-schematic.jpg)

A very simple schematic for the resetter.

如果您的路由器在每次崩溃或互联网连接中断时简单地重置自己，这不是很好吗？[Cyb3rn0id] [有一个解决方案](https://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Fwww.settorezero.com%2Fwordpress%2Fresetternet-un-dispositivo-basato-su-esp8266-che-resetta-il-router-in-caso-di-mancanza-di-collegamento-ad-internet%2F)(意大利原文[此处](https://www.settorezero.com/wordpress/resetternet-un-dispositivo-basato-su-esp8266-che-resetta-il-router-in-caso-di-mancanza-di-collegamento-ad-internet/))，以 ESP8266 的形式，每隔几秒钟 ping 一次在线服务，并在 ping 尝试重复不成功的情况下，通过电源继电器关闭并再次打开路由器。它非常简单，只需要一个 GPIO 和一个 MOSFET 来触发带有 LED 指示器的继电器，以便进行良好的测量，并且它是建立在一块原型板上的。为了安全起见，路由器电源被切换到低压侧。

该软件非常简单，并且内置了 WiFi 证书，所以我们猜测可能会有一个带有网络界面的版本。但作为一个缓解路由器崩溃痛苦的个人设备，尽管有这个缺点，它还是赢得了我们的投票。

这不是我们在这里看到的第一个路由器重置器，但是以前的模型仍然需要人工干预。