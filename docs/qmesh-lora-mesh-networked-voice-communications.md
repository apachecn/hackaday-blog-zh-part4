# 网络语音通信

> 原文：<https://hackaday.com/2021/06/06/qmesh-lora-mesh-networked-voice-communications/>

LoRa 非常适合长距离发送短数据包，但通常不适合语音通信。[Dan Fay]正在寻求用[q mesh 改变这种情况，这是一种用于业余无线电应用的同步泛洪网状网络协议](https://hackaday.io/project/161491-qmesh-a-lora-based-voice-mesh-network)。

在泛洪网状网络中，每个节点重复它接收到的每个消息。如果单个节点停止工作，这在理论上具有使网络自我修复的优势，但通常只是意味着节点会相互干扰。由于 LoRa 的一些特性，[Dan]正在使用一些技巧来解决这个数据包冲突问题。LoRa 网络可以利用“捕获效应”,如果功率电平差足够大，该效应允许接收器区分两个分组。通过增加前向误差校正和稍微改变 LoRa 啁啾的频率和定时，这一点得到进一步改善。QMesh 还通过将传输分成多个时隙来实现 TDMA(时分多址),并且每三个时隙才传输一次。这意味着它以 33%的占空比运行，这远远高于免许可证 ISM 频段允许的 0.1%-10%，这在法律上将其限制在 ham 频段。

在硬件方面，[丹]一直在使用带有 F4/L4/F7/H7 微控制器的 STM32 NUCLEO-144 开发板，以及带有 1 W LoRa 模块和有机发光二极管屏幕的定制屏蔽。虽然[Dan]希望最终制造手持无线电，但他计划首先开发小型 FM 中继器，将语音编码为 codec2，并使用 QMesh 作为回程。QMesh 仍在开发中，但我们希望看到一些长期测试的结果，我们很高兴看到它如何成熟。

如果你对一个更基本的基于 LoRa 的人对人的信息系统感兴趣，看看 [Meshtastic](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/) 。在过去的一年里，进展非常迅速。要了解更多关于 LoRa 和其他数字调制方案，请查看我们不久前用 SDR 举办的[速成班。](https://hackaday.com/2020/01/28/rf-modulation-crash-course-for-hackers/)