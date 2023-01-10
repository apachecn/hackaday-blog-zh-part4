# 3D 打印激光扫描共聚焦显微镜测量微米

> 原文：<https://hackaday.com/2021/04/26/3d-printed-laser-scanning-confocal-microscope-measures-microns/>

当一个人想到显微镜，它似乎大多是定性的。观察充满细菌或原生动物的载玻片与其说是为了进行测量，不如说是为了识别特征并描述它们的外观。然而，并不是所有的显微镜都是一样的，有些显微镜更适合对微观领域进行精确测量。

[这台 3D 打印的共焦激光扫描显微镜](https://www.youtube.com/watch?v=9TYlQ4urcg8)是测量非常小的东西的仪器的一个很好的例子。正如[Zachary Tong]所指出的，共焦扫描显微镜使用一种巧妙的光学装置来收集样本中单个明确点的光；扫描功能不是获得二维焦平面内所有点的图像，而是在三维空间中通过样品移动焦点，捕捉空间数据和光学信息。

[Zach]的显微镜载物台基于[open flex 的 Delta 载物台](https://openflexure.org/projects/deltastage/)，这是一个开源的 3D 打印 delta-bot 运动控制平台，能够以亚微米精度定位样本。舞台上方是看似简单的光学系统，有一个激光二极管光源、一个物镜和一个针孔后面的光电二极管检测器。探测器向自制的跨阻抗放大器提供信号，当样品在一个小的三维空间中移动时，该放大器可以捕捉数百万个点的数据。所有这些数据都经过处理，以找到与每个点的最大强度相对应的 Z 轴位置。

收集所有这些数据需要一段时间——即使是一个小样本也需要几天时间——但它工作得很好。[扎克]已经有了一些减少噪音和加快扫描时间的想法；也许像这样的基于 DVD 部件的阶段会比 delta 阶段更快。我们期待看到他的进步。

 [https://www.youtube.com/embed/9TYlQ4urcg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9TYlQ4urcg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[smellsobikes]的提示！