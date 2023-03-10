# 酷炫自拍的热门打印机

> 原文：<https://hackaday.com/2020/05/07/a-hot-printer-for-cool-selfies/>

随机购买一些可破解的小工具，只是因为它们便宜，而且似乎对未来的项目有潜在的兴趣，这是我们大多数人都能理解的。[fruchti]在购买五个热敏打印机模块时也遇到过这种情况，当时他并没有明确的用途。直到几年后，他才在他的[逆热感相机](https://hackaday.io/project/171329-inverse-thermal-camera)项目中很好地利用了它们。

这个名字完美地概括了该设备的功能，即将图像转化为热量，而不是相反。用一种不那么神秘的方式来说，[fruchti]建造了一个自拍相机，可以立即在热变色纸上打印出照片。该项目在 Raspberry Pi 上很容易实现，但他选择了一种更简约的方法，即使用 STM32 微控制器。这涉及到一些挑战，因为 MCU 没有足够的 RAM 来存储整个帧，并且相机模块没有 FIFO 缓冲区。为了捕捉和存储图像数据，[fruchti]应用了一种逐行抖动[算法](https://en.wikipedia.org/wiki/Dither)，这在他的附带的[博客文章](https://25120.org/post/inverse_thermal_camera/)中有详细描述，而相应的代码可在[GitHub 上获得。](https://github.com/fruchti/inverse_thermal_camera)尽管外壳是用废弃的 PCB 材料临时制作的，但成品看起来仍然很棒。特别是，用来固定纸卷的保险丝座让它看起来像蒸汽朋克。

自然，这不是我们第一次看到[热敏打印机被用于即时拍照](https://hackaday.com/2018/04/16/polaroid-gets-thermal-printer-and-raspberry-pi/)，也可能不会是最后一次。