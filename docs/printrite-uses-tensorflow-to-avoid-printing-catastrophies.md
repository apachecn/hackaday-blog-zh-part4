# PrintRite 使用 TensorFlow 来避免打印灾难

> 原文：<https://hackaday.com/2019/03/03/printrite-uses-tensorflow-to-avoid-printing-catastrophies/>

TensorFlow 是一个流行的机器学习包，尤其擅长图像识别。如果你想使用网络摄像头监控你草坪上的猫，或者提醒你有访客，TensorFlow 可以通过一系列预烤库帮助你实现这一目标。[Eric]对 PrintRite 采取了不同的策略—[使用 TensorFlow 来监控他的 3D 打印机，并在打印变坏或更坏时向他发出警告。](https://hackaday.io/project/163587-printrite-tensorflow-for-3d-printing)

该项目依靠训练 TensorFlow 来识别变坏的 3D 打印图像。如果层被分离，或者喷嘴被融化的粘性物质覆盖，停止打印可能是个好主意。最坏的情况是，您的打印机可能开始冒烟或着火–在这种情况下，[Eric]将系统配置为使用支持 TP-Link Wi-Fi 的电源插座关闭打印机。

目前，该项目作为 OctoPrint 的插件存在，并依赖于两个 Raspberry Pis 一个零来处理相机，一个 3B+来处理 OctoPrint 和 TensorFlow 软件。它还处于发展的早期阶段，可能还不能完全取代人工监管。尽管如此，这是一个充满希望的项目，我们渴望看到这一领域的进一步发展。

在提高 3D 打印机的可靠性方面有很多进展—[我们甚至看到了一种恢复失败打印的神奇设备。](https://hackaday.com/2018/04/13/resuming-failed-3d-prints-automatically/)