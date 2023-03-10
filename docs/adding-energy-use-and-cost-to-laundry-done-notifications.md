# 向“洗衣完毕”通知添加能源使用和成本

> 原文：<https://hackaday.com/2018/11/03/adding-energy-use-and-cost-to-laundry-done-notifications/>

前一段时间，[Xose Pérez]对在他的洗衣机完成一个循环时生成通知很感兴趣，现在随着[增加了像报告用电量和成本](http://tinkerman.cat/useful-notifications-from-your-home-appliances-using-node-red/)这样的功能，他将所有这些都放在了一个[节点-红色](http://nodered.org/)节点中，使其易于修改或与其他项目集成。

[Xose]从他发明的一个[洗衣监控器](https://hackaday.com/2016/08/01/your-laundry-is-done/)开始了这段旅程，它有效地利用廉价的硬件(和他自己的固件)来监控他的洗衣机的当前使用情况。该传感器被用作发送通知的基础，每当电器的周期结束时通知他。从那以后，他继续认真对待家庭电力监控，通过一点额外的工作，不仅可以判断给定设备何时启动和停止，还可以总结设备的能源使用和成本，使通知更加有用。这个包被命名为[node-red-contrib-power-monitor](https://flows.nodered.org/node/node-red-contrib-power-monitor)，也托管在 [GitHub](https://github.com/xoseperez/node-red-contrib-power-monitor) 上。

[支持 WiFi 的廉价智能开关](https://hackaday.com/2018/02/06/hacking-a-sonoff-wifi-switch/)使最笨的电器也有可能加入物联网，所以不要忽视【Xose】在 [ESPurna](https://github.com/xoseperez/espurna) 上的补充工作，这是一种替代的开源固件，用于各种基于 ESP8266 和 ESP8285 的智能开关、灯和传感器。