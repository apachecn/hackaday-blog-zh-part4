# 用 LoRaWAN 构建本地网络

> 原文：<https://hackaday.com/2022/10/22/building-a-local-network-with-lorawan/>

就其核心而言，互联网实际上只是一堆联网的计算机。没有理由不能有其他独立的计算机网络，或者我们都必须将我们拥有的每台计算机连接到一个互联网上来统治它们。事实上，对于很多嵌入式系统来说，给它们一个完整的网络堆栈和 Cat6e 以太网只是为了报告一些关于它们自己的细节，这没有太大的意义。进入 LoRaWAN，这是一种为物联网设备使用极低功耗的无线局域网，[以及在城市环境中实施这些网络中的一个](https://hackaday.io/project/187015-local-lorawan-infrastructure)。

建筑的核心是位于高楼顶端的 LoRaWAN 网关，以最大限度地扩大所有其他设备的无线覆盖范围。它在软件端运行 ChirpStack，并使用 Kerlink Wigrid 站进行广播。在这种设置下，报告的范围是 9 公里多一点。也可以添加其他网关，并且单独的 LoRa 模块可以向任何可用的网关报告。从那里，网关都与中央服务器通信，信息可以发送到更广泛的网络，互联网或其他。

该项目的创建者[mihai.cuciuc]指出，这种解决方案可能并不适合所有人。还有其他可用的广域网，但像这样使用 LoRaWAN 可能会随着越来越多的设备加入网络而扩展得更好。对于 LoRa 可以发挥巨大作用的一些其他方式，看看这个项目[，它用它建立了一个离网通信网络](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)。