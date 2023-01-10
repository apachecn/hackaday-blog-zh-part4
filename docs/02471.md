# 图书馆使 ESP 空中更新变得容易

> 原文：<https://hackaday.com/2019/03/21/library-makes-esp-over-the-air-updates-easy/>

潜在地，将设备连接到网络的最大好处之一是你可以远程更新它。然而，你如何做到这一点呢？如果您为 ESP8266 或 ESP32 使用 Arduino 设置，您可以尝试[scottchiefbaker 的] [库](https://github.com/scottchiefbaker/ESP-WebOTA)，它有望使该过程变得简单。

添加它看起来很简单。当然，你需要包含。如果不介意使用端口 8080 和路径/webota，只需要从主循环调用 handle_webota()即可。如果您想更改默认值，您需要在设置中添加一个额外的呼叫。您还需要设置一些全局变量来指定您的网络参数。

唯一需要注意的是，循环中的长延迟语句会阻碍工作，无论如何都不是一个好主意。如果您有它们，您可以用 webota_delay 替换所有的延迟调用，这将阻止系统忽略更新请求。

代码从另一个在线教程开始，但是很好地打包了代码以供重用。要进行更新，只需通过网络浏览器导航到设备，并使用正确的端口号和路径。在那里，您可以使用 export compiled binary 命令上传从 Arduino IDE 中获取的新的二进制映像。

我们看到的唯一问题是代码似乎根本无法验证您的身份。这意味着任何人都可以将代码加载到您的 ESP 中。这在专用网络上可能没问题，但在公共互联网上肯定是自找麻烦。最初的教程代码确实有一个硬编码的用户和密码，但它看起来不是很有用，因为密码是明文的，如果你知道正确的 URL，它不会阻止你上传。从库中删除它可能是有意义的，但是我们希望在我们部署的任何东西中构建某种有意义的安全性。

如果你有网络连接，我们已经看到[用一个带无线芯片的普通 Arduino](https://hackaday.com/2018/01/18/over-the-air-updates-for-your-arduino/) 做了同样的把戏。你甚至可以[通过 WiFi](https://hackaday.com/2014/11/13/programming-an-arduino-over-wifi-with-the-esp8266/) 来做这件事，但是要用一个 ESP8266，然后你也要能够更新它。