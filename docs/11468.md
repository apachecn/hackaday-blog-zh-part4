# 微 GPS 看到你忽略的东西

> 原文：<https://hackaday.com/2021/10/07/microgps-sees-what-you-overlook/>

GPS 是一个非常强大的工具，它可以让你的智能手机等设备知道它们的大致位置，在某些情况下精度约为一米。然而，这对于许多用例来说太不准确了，并且当在内部时，例如依赖于地板上的条形码的仓库机器人，准确性会大大下降。作为回应，普林斯顿大学的研究人员[广林·张，亚当·芬克斯坦，Szymon Rusinkiewicz]开发了一个他们称为 MicroGPS 的系统，该系统使用地面照片来确定其位置，精度达到亚厘米级。

该系统有一个朝下的单色摄像机，带有遮光板来控制曝光。摄像头输出馈入 Nvidia Jetson TX1 平台进行处理。这个想法实际上与[光学鼠标非常相似，因为它们通常只不过是一个经过一些巧妙处理的朝下的低分辨率相机](https://hackaday.com/2021/07/30/streaming-video-from-a-mouse/)。研究人员试图捕捉绝对位置，而不是像老鼠一样捕捉相对位置。想象一下，拿起你的鼠标，把它放在鼠标垫上的不同位置，让光标捕捉到屏幕的不同部分。在我们离地面很远的地方，沥青、柏油路面、混凝土和地毯看起来很均匀。但是对于宏观相机来说，裂缝、纤维和瑕疵是清晰可辨的。

他们提前对表面进行采样，将所有图像拼接在一起，创建全球一致的地图。然后，在四处移动时，他们提取特征并实施投票方法来过滤掉大量的误报。该系统足够强大，即使在外部道路上创建初始数据集一个月后也能工作。他们把树叶放在地上，试图欺骗系统，但看到了非常稳定的导航。

他们的论文、代码和数据集都可以在网上获得。我们期待融合系统能够将 GPS、Wifi 三角测量和 MicroGPS 结合起来，提供稳定而精确的位置。

休息后的视频。

 [https://www.youtube.com/embed/oQn1wvIkC0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oQn1wvIkC0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

