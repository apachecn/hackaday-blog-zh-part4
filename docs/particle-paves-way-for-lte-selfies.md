# 粒子为 LTE 自拍铺平了道路

> 原文：<https://hackaday.com/2019/01/15/particle-paves-way-for-lte-selfies/>

从汽车到冰箱，似乎每一项新技术都与互联网相连。不管是好是坏，我们已经深入“物联网”了。但是你的相机呢？不，不是你智能手机里的摄像头；那个已经连上了互联网把你的秘密卖给出价最高的人。难道你不认为你信赖的 DSLR 可以通过注入广域网而得到改善吗？

[![](img/796041451827c8839f29f09d6f27e7ae.png)](https://hackaday.com/wp-content/uploads/2019/01/ltecam_detail.jpg) 不管你对这个问题的答案可能是什么，【托马斯·基特里奇】决定通过[让他心爱的佳能 EOS Rebel T6 成为物联网](https://github.com/timmah1991/CameraController)的荣誉成员来改善他的生活。说实话，他说他还没有想出这个项目的应用程序。但由于他既想尝试支持 LTE 的粒子硼开发板，又想为专业生产设计自己的 PCB，这似乎是一个很好的尝试方式。

由此产生的电路板是一个相当简单的硼粒子“屏蔽”,让[托马斯]通过互联网或蓝牙在本地触发多达两个摄像头。如果 LTE 不是你喜欢的类型，不要担心。由于 Boron [遵循 Adafruit Feather 规范](https://learn.adafruit.com/adafruit-feather/feather-specification)，因此有一整套具有各种连接选项的开发板可供这个小插件使用。

在 GitHub 存储库中，[Thomas]已经上传了 PCB 文件、3D 打印外壳的 STL 文件，当然还有加载到粒子板上的固件源代码。他目前有代码将两个快门触发器作为粒子云 API 的函数公开，还有一个实际的例子，当特定的单词在松弛通道中使用时，它会触发相机。

在一年多一点的时间里，[粒子硼是细胞开发板](https://hackaday.com/2018/02/13/particle-introduces-new-hardware-adds-mesh-support/)世界中一个相当新的成员。历史上，我们还没有看到太多支持蜂窝的项目，[可能是因为让它们上线太麻烦了](https://hackaday.com/2019/01/04/finding-the-goldilocks-cell-module/)，但随着像 Boron 这样的新电路板的出现，我们可能会开始看到具有这种形式连接和面向互联网的 IP 地址的随机设备的增加。当然*这不会有什么不好的结果！*