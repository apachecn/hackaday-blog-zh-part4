# 基于 ESP8266 的低能耗电路板在被触发前会像木头一样休眠

> 原文：<https://hackaday.com/2018/11/13/low-energy-esp8266-based-board-sleeps-like-a-log-until-triggered/>

鉴于[黑客攻击和重新利用亚马逊 Dash 按钮](https://hackaday.com/tag/amazon-dash/)的流行，似乎真的需要一个简单的“当按钮被按下时，在互联网上做一些有趣的事情”的设备。如果你有这种需求，但不想让一个 Dash 设备屈服于你的意志，看看[【凯文·达拉】的 trigBoard](http://www.kevindarrah.com/wiki/index.php?title=TrigBoard) 吧。

trigBoard 是一款基于 ESP8266 的电池供电板，包括一些智能电路来帮助它几乎不消耗功率(不到 1 微安！)同时等待由数字输入触发。该输入可以是磁簧开关、按钮或类似装置，您可以将电路板配置为常开或常闭开关。

允许如此低功耗的智能硬件在[【Kevin】的 YouTube 视频](https://www.youtube.com/watch?v=TSbEN4bdt7I)中进行了解释，我们也在休息后嵌入了该视频。总结一下:EPS8266 大部分时间是完全不通电的。德州仪器 [TPL5111](http://www.ti.com/product/TPL5111) 功率定时器芯片消耗 35 纳安，每小时唤醒 ESP8266 以检查电池。该芯片还有一个手动唤醒引脚，正是这个引脚——以及更多的省电电路——用于根据外部输入触发操作。

显然，微控制器可以以某种方式区分被唤醒进行电池检查和按下按钮，所以你不必担心每小时都会意外地给自己发送警报。默认固件设置为使用[按钮](https://www.pushbullet.com/)发送通知，但是当然你可以做任何 EPS8266 能够做的事情。代码可以在[项目的维基页面](http://www.kevindarrah.com/wiki/index.php?title=TrigBoard#Base_Firmware)上找到。

该板还包括用于 LiPo 电池的标准微型 JST 连接器，并且可以通过微型 USB 端口对所述电池充电。trigBoard 的完整[原理图](http://www.kevindarrah.com/wiki/index.php?title=TrigBoard#Schematic)在维基上，预建设备[在 Tindie](https://www.tindie.com/products/kdcircuits/trigboard-ultra-low-power-esp8266-iot-platform/) 上可用。

[Kevin]的硬件演练视频在休息后嵌入。

 [https://www.youtube.com/embed/TSbEN4bdt7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TSbEN4bdt7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [危险原型](http://dangerousprototypes.com/blog/2018/11/07/trigboard-ultra-low-power-esp8266-iot-platform/)