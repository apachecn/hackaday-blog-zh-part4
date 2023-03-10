# 按钮→推送通知

> 原文：<https://hackaday.com/2018/12/30/pushbutton-%e2%86%92-push-notification/>

有多少普通设备升级到物联网，因为它们让你监控单个数据点或变量？在沟通悬崖上的小小推动让你多收 500%的费用。现在，如果你像黑客阅读器一样方便，你可以花一个下午的时间解决这个问题，从一个“笨”的设备上获得同样的效果。如果物联网就像当你的衣服干了，或者你的水开了时获得通知一样简单，那么你真正需要的只是一个 WiFi 设备和一个推送通知，对吗？需要比这更复杂吗？[【Gianni】认为就是这么简单](https://www.settorezero.com/wordpress/come-ricevere-notifiche-push-sul-cellulare-dal-nostro-sistema-domotico-con-pushover-esp8266/) ( [机器翻译](https://translate.google.com/translate?hl=en&tab=TT&authuser=0&sl=auto&tl=en&u=https%3A%2F%2Fwww.settorezero.com%2Fwordpress%2Fcome-ricevere-notifiche-push-sul-cellulare-dal-nostro-sistema-domotico-con-pushover-esp8266%2F))并在 Raspberry Pi、Arduino 和 ESP8266 上构建了一个易于实现的版本。

[Gianni]利用名副其实的 Pushover(一个有 1 周试用期的付费应用)将你的比特、字节、单词或字符串转换成推送通知。这个想法源于对家庭安全系统的渴望，这种系统不需要持续的监控，而是提醒你注意问题。你需要的最低要求是让你的手机发出一个提示:“你的前窗传感器被触发了。”现在是时候启动您的 IP 摄像头应用程序或呼叫附近的人了。

这不是革命性的，它可能是物联网的“Hello World”，但这是一些人所需要的。不管你想用什么样的框架，总的想法都是一样的。例如，如果你有一个谷歌套件账户，你可以建立一个聊天室来接收提醒通知；谷歌的 quickstart 用 Python 测试大约需要 3 分钟。同样的[设置也可用于 Slack](https://api.slack.com/incoming-webhooks) ，【汤姆·纳尔迪】给[做了不和谐](https://hackaday.com/2018/02/15/creating-a-discord-webhook-in-python/)的指导。这些处理接收端，但是发送端也非常灵活——您构建的 MQTT 代理很容易成为警报的来源。

在一个周末制作几个这样的东西，放在附近，用几个焊点将你的下一个项目提升到物联网状态。也许它会是你自己的[安全系统](https://hackaday.com/2017/04/21/iot-security-is-hard-heres-what-you-need-to-know/)的[运动传感器](https://hackaday.com/2018/07/19/a-super-simple-esp8266-iot-motion-sensor/)。