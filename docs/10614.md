# 带编码器和细绳的亚毫米机械 3D 扫描仪

> 原文：<https://hackaday.com/2021/07/01/sub-mm-mechanical-3d-scanner-with-encoders-and-string/>

[Scott Rumschlag]想要一种方法来精确绘制改造项目的内部空间，但不想处理由光学 3D 扫描创建的大量数据集，并且发现缺少经济高效的光学工具的精度。相反，他建造了一个 3D 电缆测量设备，可以通过使用连接到电缆的手动探针来绘制地图。

电缆缠绕在可伸缩的卷轴上，穿过滑轮，并穿过安装在双轴万向节上的碳纤维管。有一些商业机器使用这种机械方法，但[斯科特]在看到价格后决定自己制造一台。万向节的每个轴的旋转角度和延伸电缆的长度用编码器测量，并且理论上探针的相对坐标可以用简单的几何学计算。然而，对于[斯科特]想要的精确程度来说，问题在于细节。为了确定 3 米距离上 0.5 毫米以内的点的位置，编码器的角度分辨率必须小于 0.001°。机械编码器会增加不必要的阻力，磁编码器也不是完全线性的，所以使用光学编码器。许多其他因素也会引入误差，如电缆的拉伸和下垂、轴承的粘性、万向节轴的垂直度，甚至编码器导线产生的弹簧力。这些误差都必须在计算中考虑进去。起初，[Scott]使用 Arduino Mega 进行几何计算，但在他发现 Mega 的浮点精度不好后，他将它转移到了自己的笔记本电脑上。

[Scott]花了大约 500 个小时来构建和调整设备，但最终结果令人印象深刻。令人惊讶的是，很少有光学机器能够达到这种精度和准确度，而且它们会受到物体反射率等因素的影响。

如果你真的想进入真正的 3D 扫描，一定要花时间阅读[【姜懿翔·帕普】的优秀指南，了解各种技术的实际应用。我们大多数人的口袋里已经有一个智能手机形式的 3D 扫描仪，可以用于](https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/)[摄影测量](https://hackaday.com/2019/04/07/get-great-3d-scans-with-open-photogrammetry/)。

 [https://www.youtube.com/embed/euo25NMkgWM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/euo25NMkgWM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

