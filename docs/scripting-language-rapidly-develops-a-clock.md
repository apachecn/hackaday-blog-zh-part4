# 脚本语言快速开发了一个时钟

> 原文：<https://hackaday.com/2019/06/27/scripting-language-rapidly-develops-a-clock/>

在过去，你很可能已经开始用 Basic 编程了。它不是一种非常强大的语言，并且很难用它来构建大型项目，但是它简单易学，易于使用，并且解释器使得在不投入大量时间的情况下进行尝试变得很容易。今天，你更有可能开始使用像 Arduino 这样的东西，但是当你在做简单的项目时，很容易错过可访问的语言和即时的反馈。附件 WiFi RDS(快速开发套件)是一种用于 ESP8266 的脚本语言，不是很基本，但它有很多相同的属性。来自[cicciocb]的一个示例项目是[滚动点阵 LED 时钟](https://sites.google.com/site/annexwifi/projects/3d-printed-clock)。

代码非常简单:

```
' Simple program using Annex and a MAX7219 dot matrix module
' by cicciocb 2019
'Set 4 8x8 displays with GPIO15 as CS pin
MAXSCROLL.SETUP 4, 15
INTENSITY = 5
'Set the first message with Annex
MAXSCROLL.PRINT "Annex"
MAXSCROLL.SHOW 31, INTENSITY
PAUSE 1000
'Set the refresh rate of the display (50 msec) - lower values -> scroll faster
TIMER0 50, SCROLLME
WAIT

SCROLLME:
'Scroll the display with the intensity defined before
MAXSCROLL.SCROLL INTENSITY 
' Set the text with the Date and Time
MAXSCROLL.TEXT DATE$ + " " + TIME$
RETURN
```

当然，简单的一个原因是 Annex 有一个内置的 LED 驱动程序(MAXSCROLL)。它还非常容易与远程 web 浏览器集成，因此您可以将 HTML 输出嵌入到您的项目中。

如果你看看这个项目的主页，它支持很多东西，包括新像素、伺服系统、液晶显示器和温度传感器。它还支持从 MQTT 到 PID 控制器的许多协议和算法。

如果真的很怀念 Basic，可以在 web 上用[。更不用说，那个](https://hackaday.com/2018/09/17/its-the-web-basically/) [QuickBasic](https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/) 还在飘来飘去。