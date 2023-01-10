# Raspberry Pi On The Go 为车载系统供电

> 原文：<https://hackaday.com/2018/08/01/raspberry-pi-on-the-go-powers-car-system/>

大多数新车都有全球定位系统、后置摄像头以及车载系统能带来的所有其他奇迹。但是如果你有一辆旧车呢？[Fabrice Aneche]有一辆 2011 款汽车，想要一个后视摄像头。他从一个触摸屏、一个树莓派 3 和一个摄像头开始。但是你知道这些项目是如何独立运作的。到目前为止，[项目](https://blog.nobugware.com/post/2018/my_own_car_system_raspberry_pi_offline_mapping/)在[的博客中有两个条目](https://blog.nobugware.com/post/2018/my_own_car_system_raspberry_pi_offline_mapping_map_matching_places_part2/)。

没过多久，他就忍不住想加个 GPS。但是没有地图就没意思了。另外，你还需要一个接一个的方向。[Fabrice]用 Qt5 和 QML 做了很多用户界面。他开始用 X11 运行它，但速度很慢。尽管事实证明 Qt5 可以直接驱动 Pi 的视频而不使用 X11，所以这就是他最终做的。不在 QML 的代码——主要处理 GPS 定位——是用 Go 写的，而 MOCS 的代码(我自己的汽车系统)在 [GitHub](https://github.com/akhenakh/mocs) 上。

除了为了性能而转储 X11 之外，还有很多有趣的细节。他也不满意现有的 Linux GPS 守护进程，所以他也重写了 T1。

尽管他说这个系统还远未完成，但看起来很容易复制。他在 Raspberry Pi 上使用 Arch，但是老实说，使用任何 Linux 发行版看起来都不难。

今年早些时候，我们看到[一个使用 Android](https://hackaday.com/2018/02/26/crankshaft-open-source-car-computer/) 的类似项目。我们不禁惊叹于[自 1971 年](https://hackaday.com/2018/06/17/retrotechtacular-car-navigation-like-its-1971/)以来的发展。