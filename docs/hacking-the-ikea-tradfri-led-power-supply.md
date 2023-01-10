# 侵入宜家特罗 DFRI LED 电源

> 原文：<https://hackaday.com/2019/10/08/hacking-the-ikea-tradfri-led-power-supply/>

仅仅因为某些东西被热情的黑客积极地记录和篡改，并不意味着这些信息就被方便地集中了。将不同的资源集中在一个地方会有很大的价值，这正是[Trammell Hudson]在他的资源页面上所做的事情，他破解了 IKEA tr DFRI LED 电源和无线接口。示意图拆卸，自定义固件映像，这一切都在一个方便的地方。

早在 2017 年，宜家特罗 DFRI 黑客场景[就围绕着 LED 灯泡](https://hackaday.com/2017/11/17/hacking-the-ikea-tradfri-light-bulb/)展开，但随着产品群的扩大，其余产品也引起了一些关注。

为什么要破坏这些装置呢？一个原因是添加特性，另一个原因是让它们通过您自己的 MQTT 网络进行通信。MQTT 就是你成为[树莓派和宜家之旅的原因](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)远离智能家居的开端，除了你自己，没有人能控制或影响它。