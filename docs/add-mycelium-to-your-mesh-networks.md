# 添加菌丝体到你的网状网络

> 原文：<https://hackaday.com/2021/10/26/add-mycelium-to-your-mesh-networks/>

在世界上的许多地方，在一场好的降雨后的几天，看到各种蘑菇从地里冒出来是相当常见的。然而，这些神秘的生物并不是故事的全部。生物是一个巨大的隐藏纤维网络，称为菌丝体，通过地面扩散到它可以定居的任何其他有机物质中。它神秘的空气和广阔的覆盖面是整部《星际迷航》的灵感来源，当然，还有像这个基于劳拉的网状网络“菌丝体”这样的项目。

菌丝体是[Catamine]的发明，与更典型的网状网络相比，它包括许多新颖的特征。首先，它旨在用于低功率应用，使用户能够通过分布式网络而不是像手机服务提供商那样的集中式网络发送消息。另一方面，消息能够被加密和认证，这在目前其他网状网络如 APRS 是不可能的。这个想法是，一个大型网络，除了一个 ESP32、一个天线、[和这个软件](https://0xacab.org/radical-comms/mycelium-mesh)之外，没有任何复杂的东西，就能够在中央网络不可用的情况下安全地通信，无论是因为自然灾害还是因为政府组织在政治动乱期间禁用互联网。

网状网络目前正在积极开发中，虽然还不能发送消息，但该网络能够识别节点并维护密钥库。肯定有很多这样的例子是有用的，就像我们以前从其他基于(非加密)LoRa 的网络解决方案中看到的那样[，这些解决方案是围绕类似的原则构建的。](https://hackaday.com/2020/12/12/irc-over-lora-for-when-things-really-go-south/)

感谢[dear userhon]的提示！