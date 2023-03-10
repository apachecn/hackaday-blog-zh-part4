# 借助 MQTT 的力量让智能灯泡变得更加智能

> 原文：<https://hackaday.com/2020/12/25/making-smart-bulbs-smarter-with-the-power-of-mqtt/>

智能家居自动化有什么意义？当然是为了让每天的任务更简单！根据[Tomasz Cybulski]的说法，当他在衣柜里安装宜家智能灯时，情况并非如此。把它们放在一个普通的开关里很方便，在这种情况下是一个遥控器，但是每次他需要灯的时候都必须去找它，这需要一些改进。进入他的项目，通过使用一个简单的 ESP8266 让智能灯泡变得更智能。

虽然将门开关挂在灯的电源上可以提供一个快速的解决方案，但[Tomasz]的妻子希望保持遥控器的功能，所以他不得不去别处寻找。这些灯泡使用简单的 Zigbee 协议，因此安排其他设备相当简单。为他现有的 Raspberry Pi 自动化控制器配置了与协议接口的 USB 加密狗，而 ESP8266 通过连接到安装在壁橱门上的簧片开关来充当现实世界的传感器。

所有的硬件都解决了，让它们互相交流就很简单了。ESP8266 使用 Tasmota 固件向运行在 Raspberry Pi 上的 MQTT 服务器发送信号，该服务器又通过加密狗将其转换为 Zigbee 频率上的远程触发器。门打开时灯亮，门关上时灯又灭。由于没有对灯具本身进行进一步的改造，最初的宜家控制器仍能正常工作，我们相信[Tomasz]的妻子会对此表示赞赏！

MQTT 可能是一个有趣的软件，不仅仅是家庭自动化，如果你家里已经有一个服务器，你可以用它把你剪贴板的内容转移到另一个设备上。如果你用它来实现家庭自动化，[这里有一个相当不寻常的仪表板](https://hackaday.com/2020/11/29/mqtt-dashboard-uses-sharp-memory-lcd/)的灵感，让事情变得有趣。休息之后看看这个黑客的行动。

 [https://www.youtube.com/embed/OVvCoBITh-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OVvCoBITh-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

