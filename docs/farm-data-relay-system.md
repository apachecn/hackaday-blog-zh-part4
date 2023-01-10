# 农场数据中继系统:结合 LoRa 和 2.4 Ghz 网络，无需 WiFi 路由器和云依赖

> 原文：<https://hackaday.com/2022/07/02/farm-data-relay-system/>

在大范围内建立无线传感器网络会很快变得成本高昂，而且让一切顺利通信会是一件非常头痛的事情，尤其是当您将短程 Wi-Fi 与远程 LoRa 相结合时。为了简化这一点，[Timm Bogner]创建了[农场数据中继系统](https://github.com/timmbogner)，该系统简化了在广域范围内以各种拓扑结构组合 LoRa、2.4Ghz 模块和串行通信的过程。

FDRS 在短距离内使用 ESP32/8266 传感器节点，在长距离内使用 LoRa 节点。ESP 节点使用 Espressif 的无连接 [ESP-NOW](https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/) 点对点协议，允许多个 ESP 板直接通信，无需 Wi-Fi 路由器。ESP 模块可以具有 3 种角色之一，节点、中继器或网关，并且网关和中继器共享相同的代码。节点接受传感器输入，并被配置为每个节点都有一个唯一的`READING_ID`。

中继只是重新传输 ESP-NOW 数据包以扩展网络范围，而网关则根据需要在 ESP-NOW、MQTT over Wi-Fi、LoRa 或串行消息之间转换数据包。中继器和网关都有唯一的`UNIT_MAC`用于寻址。处理 ESP 设备通信的代码很简单，并且有很好的文档记录，因此您只需要设置一些配置值，然后就可以将精力集中在特定应用程序所需的代码上。

系统的中枢是运行 [Node-RED](https://hackaday.com/2020/01/15/automate-your-life-with-node-red-plus-a-dash-of-mqtt/) 的 Raspberry Pi，它充当最终的 MQTT 网关，并连接到 ESP MQTT 网关。这意味着所有的操作都发生在本地网络中，不依赖于互联网连接和云服务。但是，它仍然可以根据需要使用 MQTT 或任何其他协议在互联网上发送和接收数据。Node-RED 使得构建定制自动化和接口变得特别容易。

在休息后的视频中，Andreas Spiess，这个带着瑞士口音的男人，也参与了这个项目，讲述了所有的功能，设置和注意事项。

 [https://www.youtube.com/embed/6JI5wZABWmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6JI5wZABWmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



LoRa 是一个非常有用的户外远程网络工具。从没有互联网的[监测鸟舍](https://hackaday.com/2022/04/09/lora-powered-birdhouses-enable-wireless-networking-when-the-internets-down/)，没有手机网络的[短信](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)，甚至从月球上反弹信号的，都有很多用途。