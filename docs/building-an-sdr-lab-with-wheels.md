# 建造一个带轮子的 SDR 实验室

> 原文：<https://hackaday.com/2018/07/27/building-an-sdr-lab-with-wheels/>

软件定义无线电(SDR)硬件的成本低得令人难以置信，相关软件的成本通常为零，这是进入无线电世界的最佳时机。如果你口袋里有 30 美元，你就可以走了。但是就像任何投入成本低廉的引人入胜的爱好一样，你最终会冒走极端的风险。

[![](img/8d1935a0b6ef8a63614036872da1245c.png)](https://hackaday.com/wp-content/uploads/2018/07/sdrcar_detail.jpg) 例如，如果你车内的收音机档位接近该车的凯利蓝皮书价值，你可能已经被收音机的 bug 咬了。在休息后的视频中，[【腐蚀剂】向我们展示了他的天线装饰现代口音](https://www.youtube.com/watch?v=KMMlF87-A2o)，这是他在旅途中接收和分析大量模拟和数字无线电信号所需的一切。

他从车顶开始，车顶上有五个鞭状天线(不包括工厂安装的 AM/FM 收音机)和两个 GPS 接收器。汽车后部的接收器向下连接到后备箱，一组 noelec nes dr RTL-SDR 接收器将存储在 USB 集线器中。他只安装了一个用于测试，但他需要更多来完成他的计划。坐在后面的还有一台 BCD780XLT 扫描仪，这是他在易贝便宜买到的，因为它有一个死显示屏。

幸运的是，在[腐蚀剂]要去的地方，他不需要显示器。SDR 接收器和扫描仪都是通过 Windows 10 平板电脑从司机座位上控制的。这将运行 ProScan 软件，该软件提供 BCD780XLT 的虚拟接口以及各种 SDR 接口。他还拥有跟踪卫星的 Gpredict 和虚拟雷达等 ADS-B 程序。

汽车的主机已经被支持 USB 主机模式的 Android 娱乐系统所取代。[腐蚀剂]说它还没有连接上，但将来主机会有自己的 SDR 接收器，这样他就可以在仪表板上运行 RF Analyzer 之类的程序。我们敢打赌，这将是世界上唯一一辆同时拥有瀑布显示和“检查引擎”灯的汽车。

即使你不准备把它安装在你的汽车上，你也可能会喜欢阅读关于[为集群无线电使用多个 SDR 接收器](https://hackaday.com/2016/03/07/triple-threat-rtl-sdr-system-reads-trunked-radio/)或[设置你自己的 ADS-B 接收器](https://hackaday.com/2014/01/16/build-a-cheap-airplane-ads-b-radio-receiving-tracking-station/)的文章，以便在一切就绪并运行后更好地了解【腐蚀剂】的想法。

 [https://www.youtube.com/embed/KMMlF87-A2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KMMlF87-A2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

