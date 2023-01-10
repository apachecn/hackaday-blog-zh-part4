# DIY 视频发射器变身 WiFi 干扰器

> 原文：<https://hackaday.com/2022/08/27/diy-video-transmitter-turned-wifi-jammer/>

FPV 无人机的激增带来了大量廉价的无线视频技术。在驾驶并坠毁了一架便宜的 FPV 无人驾驶飞机之后，[GreatScott]决定尝试建造自己的[视频发射器](https://www.youtube.com/watch?v=LyztbYNB0Eg)，这比预期的要困难得多。

虽然数字技术已经赶上了 FPV 世界，但许多系统仍然使用模拟视频，尤其是在无人机比赛中。视频质量不是很好，但它的优势是非常低的延迟。该技术与旧的模拟电视广播非常相似，但主要使用 5.8 GHz 免许可证频段。它本质上是模拟视频信号，频率调制到 5.8 GHz 载波信号上，通过适当大小的天线传输。

在用分立元件构建的简单电路进行了短暂的失败实验后，[GreatScott]将注意力转向了压控振荡器(VCO)。他从全球速卖通(Aliexpress)购买了几个 5.8 GHz VCOs，创建并使用了一个简单的运算放大器电路，将 FPV 摄像头的视频信号提升到 VCO 所需的输入电平。这未能在他的视频接收器护目镜上产生任何可识别的图像。为了证实 VCO 产生了所需的频率，他订购了一个类似的 2.4 GHz VCOs，并构建了一个短程(20 cm) [WiFi 干扰器](https://hackaday.com/2017/08/13/wifi-deauthentication-vs-wifi-jamming-what-is-the-difference/)。用信号发生器创建一个简单的输入信号，并确认它干扰了他笔记本电脑的 WiFi 连接。

在对其他 VCO 进行了更多实验后，最接近成功的[GreatScott]是使用 Maxim 2.4 GHz VCO 传输的几乎无法识别的图像。如果你对 VTX 赛道缺少什么有任何想法，请在下面的评论中提出。

建造干扰你周围合法信号的射频电路，或者带外广播，通常不是一个好主意，可能会让你受到当局的不愉快访问。如果你想建立自己的数字视频传输，看看 [Wifibroadcast](https://hackaday.com/2015/06/13/wifibroadcast-makes-wifi-fpv-video-more-like-analog/) 项目。

 [https://www.youtube.com/embed/LyztbYNB0Eg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LyztbYNB0Eg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

