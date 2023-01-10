# 前门摄像头通过文本发送自动警报

> 原文：<https://hackaday.com/2019/01/21/front-door-camera-sends-automatic-alerts-by-text/>

在这个动荡的时代，记者、危言耸听者和诚实的公民担心自己和家人的安全。增加一些安全功能可以减轻这些担忧，随着廉价技术的出现，前门摄像头变得流行起来。市场上有各种各样的选择，但除了观看几个小时的记录视频，它们并不总是超级有用。加入一些智慧真的会有帮助——正如彼得·奎因所做的那样。

对于这个项目，[Peter]选择了 JeVois 智能摄像机。它不仅仅是一个 USB 网络摄像头，还包含一个运行机器视觉算法的四核处理器。这允许对象识别和其他任务在相机本身上运行。在这个设置中，[Peter]将 JeVois 摄像机配置为检测人员。当检测到有人站在门口时，摄像机会通过串行接口向连接的 Raspberry Pi 发送一条信息。然后，Raspberry Pi 通过 USB 连接从相机中捕捉 JPEG 图片，并使用 Twilio 向[Peter]的手机发送通知。

这是一个集成良好的系统，可以自动拍摄到[彼得]家的访客，几乎不需要用户干预。我们也看到了其他集成的机器视觉平台—[,如 OpenMV](https://hackaday.com/2018/09/23/the-tiniest-computer-vision-platform-just-got-better/) ,它始于 2017 年的 Hackaday 奖参赛作品。