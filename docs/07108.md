# 加热器通过 ESP32 板加入物联网

> 原文：<https://hackaday.com/2020/07/08/heater-joins-the-internet-of-things-with-esp32-board/>

家用燃木加热器[g3gg0]运行良好，除了一个缺点:颗粒容器需要每隔几天手动重新填充。众所周知，人类是不可靠的生物，这一关键任务有时会被忽视，这自然会导致令人不寒而栗的结果。

由于自动填充系统昂贵且难以安装，[g3gg0]希望找到某种方式让[加热器通知其管理员任何潜在的故障情况](http://www.g3gg0.de/wordpress/esp32/mes-wifi-bringing-a-windhager-pellet-heater-online/)。不仅仅是燃料耗尽的事实(尽管这自然是最常见的警报)，而是任何其他可能使加热器无法正常工作的问题。简而言之，加热器将获得通往物联网的单程票。

事实证明，这个任务并不像你想象的那么困难。Windhager 加热器已经有升级舱，用户可以在那里插入额外的模块和传感器，以及 RS-485 上的基本数据总线。[g3gg0]所要做的就是接入总线，解码包中包含的内容，并使用这些信息在网络上生成警报。ESP32 完全可以胜任这项任务，它只需要一个定制的 PCB 和 3D 打印外壳，这样它就可以像官方扩展模块一样插入加热器。

当一条有趣的消息在总线上闪现时，ESP32 会捕获它，并将适当的消息传递给 MQTT 代理。从那里开始，[自动化的可能性几乎是无限的](https://hackaday.com/2020/01/15/automate-your-life-with-node-red-plus-a-dash-of-mqtt/)。在这种情况下，加热器的状态信息通过 Grafana 等工具可视化，重要的警报通过 PushingBox 发送到移动设备。有了这样的装置，风之使者再也不会挨饿了。

 [https://www.youtube.com/embed/8YCCq0s_L00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8YCCq0s_L00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

