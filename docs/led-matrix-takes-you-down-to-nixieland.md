# led 矩阵带你去迪克西兰

> 原文：<https://hackaday.com/2020/05/20/led-matrix-takes-you-down-to-nixieland/>

据说模仿是最真诚的奉承。当然，有些人可能会简单地用花哨的引用来掩饰公然的抄袭，但仍然有来自善意、真诚的钦佩的情况。具有类似余烬的发光的数码管是一个肯定会得到很多赞赏的组件，作为一个喜欢 LED 的发烧友，[tuenhidy]看到了一个绝佳的机会[用 RGB LED 矩阵模仿它们，并用它建立一个虚拟的谢妮时钟](https://www.instructables.com/id/VIRTUAL-NIXIE-CLOCK-ON-LED-MATRIX-64X64/)。

听起来像是在 LED 矩阵上显示谢妮管的图像，实际上正是如此。使用 UTFT 库和转换器，[tuenhidy]将单独点亮的数码管数字的图片转换为 16 位 RGB 值的数组，并用它们在 ESP32 控制的 64×64 矩阵上显示当前时间。提供两种不同的图像尺寸，您可以将两个显像管并排放置，或者以 3×2 的排列方式放置，当然也为将来的扩展提供了足够的灵活性。在休息后的演示视频中，您可以看到两个选项在运行，同时显示完整时间和秒数。

不幸的是，通过相机镜头来判断 LED 项目总是很困难，尤其是在寻找数码管的特征颜色时，但我们相信[tuenhidy]的话，它在现实中更像它。另一方面，像素化的外观无疑增加了它自己的魅力，所以你可能会完全沉迷于这些颜色——这是我们不久前在看到的一种不同的 LED 主题谢妮替代品。

 [https://www.youtube.com/embed/FZR7EjD4_L4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FZR7EjD4_L4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

