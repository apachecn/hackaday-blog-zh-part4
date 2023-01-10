# NanoVNA 测试天线方向图

> 原文：<https://hackaday.com/2020/01/11/nanovna-tests-antenna-pattern/>

当[Jephthai]想要建造自己的八木天线时，他转向 MMANA 软件进行天线建模。这是一个天线分析程序，它使用矩量法来计算不同天线几何形状的参数。在建造八木之后，预测的调谐和阻抗与真实的天线非常匹配。但是辐射模式呢？为了测试这一点，他使用了一个 NanoVNA 和一个巧妙的测试装置。

他需要一个远离天线近场的测试点，因此他将工作站设置在距离测试天线 18 英尺的地方，测试天线安装在一个可以旋转的支架上。工作站桌子的边缘上贴着油漆工的胶带，是一个连接到笔记本电脑的 NanoVNA。

剩下的只是辛苦的工作。首先，测量共振频率。然后将天线旋转 10 度并重复。测量 36 次后，你就有了整个圆。

用 GNUPlot 绘制的结果数据与天线的预测性能非常吻合。这实际上是第二次尝试，在报告中，[Jephthai]报告说，保持一致对于一切正常运转至关重要。你可以在他的照片中看到他为保持一致性所采取的一些措施。

另一个有助于一致性的方法是使用 [NanoVNASaver 软件](https://github.com/mihtjel/nanovna-saver)。该软件允许扫频、显示和创建试金石文件。

在之前，我们已经看过了 [NanoVNA。如果你更愿意把你的天线模式看做一个 3D 体积，](https://hackaday.com/2019/08/11/nanovna-is-a-50-vector-network-analyzer/)[拿出 3D 打印机](https://hackaday.com/2017/06/11/3d-printed-radiation-patterns/)。