# 开放式数据摄像头将相机、GPU 和神经网络结合在一个手工 DIY 谷物盒中

> 原文：<https://hackaday.com/2018/10/29/open-data-cam-combines-camera-gpu-and-neural-network-in-an-artisanal-diy-cereal-box/>

[moovel lab]的工程师和产品设计师创造了 Open Data Cam——一个人工智能相机平台，可以在物体通过其视野时识别和计数它们——以及用于制作自己的的开源指南[。](https://opendatacam.moovellab.com)

第一步:拿出你的尺子和美工刀。在这个无处不在的 3D 打印机世界中，他们对项目的外壳采取了一种明显的低技术方法:一个切割、折叠、带拉链的塑料盒，里面有一个纸板框架来放置电子元件。它是“防溅”的，制造起来当然很便宜，但我们有点担心内部电子设备的冷却和物理保护，因为它们不是便宜和坚固的组件。

那么里面是什么？一个 Nvidia Jetson TX2 板，一个带充电电路的 LiPo 电池和一个标准网络摄像头。然而，特别的调料是软件，[，它可以在 GitHub](https://github.com/moovel/lab-opendatacam) 上获得。[Moovel lab]的工程师们已经组装了一个好看的 wifi 可访问移动用户界面，用于标记你希望软件识别和计数对象的区域。实际的物体检测和识别任务由快速的 [YOLO 神经网络](https://pjreddie.com/darknet/yolo/)执行，Nvidia 板的 GPU 当然非常适合这项任务。

当开放数据摄像头一眨不眨的玻璃眼睛注视着我们的城市环境时，它会用一种古老而神秘的语言记录它的观察结果:CSV。这取决于你，人类，去解读这些信息，并善用它们。

在休息之后嵌入摘要视频和构建延时。

[https://player.vimeo.com/video/260744286](https://player.vimeo.com/video/260744286)

[https://player.vimeo.com/video/262991684](https://player.vimeo.com/video/262991684)

[通过[创意应用网络](https://www.creativeapplications.net/news/open-data-cam/)