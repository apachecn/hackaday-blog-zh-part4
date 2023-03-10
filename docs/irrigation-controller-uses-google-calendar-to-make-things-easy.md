# 灌溉控制器使用谷歌日历使事情变得简单

> 原文：<https://hackaday.com/2020/02/20/irrigation-controller-uses-google-calendar-to-make-things-easy/>

灌溉控制器已经存在很长时间了，通常使用普通制造商熟悉的类似硬件。然而，你当地五金店货架上的许多产品相当昂贵，相当于一个微控制器、显示器和继电器板。[oscillator]有这样一个钻机，[但想把它带入 21 世纪，IOT 风格。](https://newadventuresinwi-fi.blogspot.com/2020/02/smart-irrigation-controller.html)

现有的霍尔曼灌溉系统包括一个控制箱，连接到四个由继电器控制的电磁阀。[oscillator]决定用更好的东西来代替它，这样就很简单了。采购了一个封装了 ESP8266 的继电器板，并用 [Tasmota 固件进行了刷新。](https://github.com/arendst/Tasmota)然后通过闭路电视电源连接霍尔曼的 24v 交流电源，使新控制器与现有硬件并行运行，以防万一。日程安排则由谷歌日历控制，[配合家庭助手。](https://www.home-assistant.io/integrations/calendar.google/)

[oscillator]现在有一个可以通过网络控制的浇水系统，不需要安装任何定制的应用程序。简单地创建一个日历条目就足以让系统开始工作。我们也看到其他人使用类似的方法。这是一个使用现成零件快速构建有用的定制家庭自动化设置的绝佳例子！