# TapType:仅使用加速度计的人工智能辅助手部动作跟踪

> 原文：<https://hackaday.com/2022/05/14/taptype-ai-assisted-hand-motion-tracking-using-only-accelerometers/>

来自瑞士苏黎世联邦理工学院传感、交互和感知实验室的团队已经开发出了 [TapType，这是一种有趣的文本输入方法](https://siplab.org/projects/TapType)，它完全依赖于一对腕戴设备，当佩戴者在任何旧表面上打字时，它会感应加速度值。通过将来自每个手腕上的一对传感器的加速度值馈送到贝叶斯推理分类类型的神经网络，该神经网络又馈送到传统的概率语言模型(预测文本，对你和我)，得到的文本可以以高达 19 WPM 的速度输入，平均误差为 0.6%。专业打字者报告速度高达每分钟 25 个字，这是相当有用的。

细节有点缺乏(毕竟这是一个研究项目)，但实际的硬件似乎足够简单，基于[对话框 DA14695](https://www.dialog-semiconductor.com/products/bluetooth-low-energy/da1469x) ，这是一个很好的基于 Cortex M33 的蓝牙低能耗 SoC。这本身就是一个有趣的设备，包含一个“传感器节点控制器”模块，能够处理连接到其接口的传感器设备，独立于主 CPU。使用的传感器设备是[博世 BMA456](https://www.bosch-sensortec.com/products/motion-sensors/accelerometers/bma456/) 三轴加速度计，它以仅 150 μA 的低功耗而闻名

[![](img/dc8be8fe788164498c21e7e345f85e43.png)](https://hackaday.com/wp-content/uploads/2022/05/taptype_detail.jpg)

User’s can “type” on any convenient surface.

腕带单元本身似乎是一个包含 BLE 芯片和支持电路的主 PCB 的组合，连接到一个柔性 PCB，两端各有一对加速度计设备。然后，该组件被放入一个柔性腕带中，可能由 3D 打印的 TPU 构成，但我们只是猜测，因为从第一个嵌入式平台到可穿戴原型的进展尚不清楚。

清楚的是，腕带本身只是一个哑数据流设备，所有聪明的处理都在连接的设备上进行。通过记录志愿者在 A3 大小的键盘图像上“打字”,用运动跟踪相机跟踪手指运动，同时记录来自两个手腕的加速度数据流，来进行系统的训练(以及随后选择最准确的分类器架构)。在[发表的论文](https://siplab.org/papers/chi2022-taptype.pdf)中有一些更多的细节，供那些有兴趣更深入地挖掘这项研究的人参考。

眼尖的可能记得去年来自同一团队的类似内容，该团队[将骨传导感测与虚拟现实类型的手跟踪](https://hackaday.com/2021/03/16/bone-vibration-brings-typing-into-vr/)相关联，以在虚拟现实环境中生成输入事件。

 [https://www.youtube.com/embed/X2Yc0bmmGfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X2Yc0bmmGfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

