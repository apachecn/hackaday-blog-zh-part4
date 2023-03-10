# 带有内置通知的 ESP8266 时钟

> 原文：<https://hackaday.com/2019/06/22/an-esp8266-clock-with-built-in-notifications/>

当我们最近讨论我们可能希望传授给年轻人的技能时，其中一个讨论的问题是说一种以上语言的能力。如果需要任何演示来说明为什么会这样，今天它出现在[Byfeel]的 [Notif'Heure，一款由 ESP8266 供电的时钟和显示器](https://github.com/byfeel/Notifheure)(法语，[谷歌翻译链接](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.com&sl=fr&sp=nmt4&tl=en&u=https://github.com/byfeel/Notifheure&xid=17259,15700021,15700186,15700190,15700256,15700259&usg=ALkJrhhHhg_zEcCCP7GEQvuc4MxNHIZUgg))。如果我们只关注英语项目，我们会错过很多画面。

该项目[于 2018 年 4 月](https://byfeel.info/diy-horloge-et-notification-domotique-matrix-led-avec-jeedom/) ( [谷歌翻译链接](https://translate.google.com/translate?sl=fr&tl=en&u=https%3A%2F%2Fbyfeel.info%2Fdiy-horloge-et-notification-domotique-matrix-led-avec-jeedom%2F))开始，此后经过许多软件版本，迅速发展到目前的 3.2 版。在硬件方面，它非常简单:一个 ESP8266 开发板驱动一组 LED 矩阵显示器。在软件中，虽然它具有 NTP 同步时钟的主要功能，但也支持通知显示和与 [Jeedom](https://www.jeedom.com/site/en/index.html) 家庭自动化包的集成。

多年来，我们已经推出了无数的 ESP8266 时钟，但令人惊讶的是，这是第一个与 Jeedom 集成的时钟。有这么多可供选择的，很难挑选出例子给你看，所以也许是时候去看看真正可笑的这个有 12 个 ESP 的怪物了。

非常感谢[埃尔文]的提示！