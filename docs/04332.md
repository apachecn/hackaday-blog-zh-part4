# DIY 热像仪使用 DIY 高斯模糊

> 原文：<https://hackaday.com/2019/09/29/diy-thermal-imager-uses-diy-gaussian-blur/>

在正确的情况下，高斯模糊可以使图像看起来更加清晰。[DZL]用一个轻量级和紧凑的高斯插值例程来演示这一点，使低分辨率热传感器数据在一个小有机发光二极管上显示得更好。

[DZL]使用 MLX90640 传感器创建了一个带有小型有机发光二极管显示器的 [DIY 热成像仪](http://blog.dzl.dk/2019/06/08/cheap-diy-thermal-imager/)，但是由于传感器的分辨率相对较低，为 32×24，直接显示数据看起来非常粗糙。高斯插值来改善显示看起来真的很好，但事实证明，全高斯插值不是一个微不足道的计算写在自己身上。因为[DZL]想在微控制器上实现它，轻量级的实现就诞生了。项目页面详细介绍了高斯插值以及一些有效的快捷方式是如何实现的，所以一定要看一看。

MLX90640 传感器也在 2019 年 Hackaday 奖的参赛作品之一的[开放式热感相机](https://hackaday.com/2019/09/22/getting-the-heat-on-with-a-thermal-camera/)中亮相。如果你对热成像感兴趣，不要错过这个[拆卸热成像相机](https://hackaday.com/2018/11/07/teardown-of-a-relatively-cheap-thermal-camera/)。