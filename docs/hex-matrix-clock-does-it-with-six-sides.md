# 六边矩阵时钟有六个边

> 原文：<https://hackaday.com/2021/01/13/hex-matrix-clock-does-it-with-six-sides/>

LED 矩阵曾经是一个令人头疼的问题，需要仔细考虑才能充分利用有限的 I/O 引脚和可用的微控制器资源。如今，可寻址 LED 灯串让这一切变得轻而易举。因此，打破常规并不令人畏惧。[[w . r . Simpson]用这个六进制矩阵时钟做到了这一点。](https://www.instructables.com/HexMatrixClock/)

依靠六边形而不是普通的笛卡尔网格需要注意行和列的布局，但是 Instructable 通过必要的坐标系统来处理显示。整个展示是在没有 3D 打印机的情况下建造的，而是依靠一些基本的工艺技能和一个相框作为外壳。WS2812B 发光二极管条用于构建六边形矩阵，由 Adafruit Metro Mini 328 运行。为了给每个六边形像素(hexel)一个清晰的轮廓，使用黑纸建立了一个阴影网格，以阻止打开时显示器片段之间的光泄漏。烟熏树脂玻璃不可用，所以取而代之的是，有色窗膜被用来使显示器的前面变暗。

结果令人印象深刻；虽然从阴影网格的一些胶水痕迹是可见的特写镜头，从远处看，由于六边形的布局，最终产品看起来令人难以置信的未来感。我们可以想象这将成为未来电影剪辑中的一个很好的布景；我们非常期待在下一首爱莉安娜·格兰德单曲的背景中看到这个概念。如果这种构造对满足你的胃口来说还不够有趣，也可以考虑加入超级六边形！