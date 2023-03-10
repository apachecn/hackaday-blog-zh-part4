# 千兆像素显微镜揭示大画面的微小部分

> 原文：<https://hackaday.com/2019/06/14/gigapixel-microscope-reveals-tiny-parts-of-the-big-picture/>

[JBumstead]不想要普通的显微镜。他想要一个能展示全局的，而不仅仅是委婉的。不过，问题在于分辨率。通常，图像的分辨率越高，在相同的光学条件下，视野就越窄，这是有道理的，对吗？你越放大，你能看到的区域就越小。他的解决方案是使用传统相机创建一个显微镜，并构建一个可以捕捉多张高分辨率照片的运动平台。然后将多张照片拼接成一张图像。这使得他的[显微镜能够以大约 15 微米](https://www.instructables.com/id/Desktop-Gigapixel-Microscope/)的分辨率拍摄一张 90×60 毫米区域的照片。理论上，分辨率可能好到 2 微米，但在这个比例下很难精确测量分辨率。

作为一个 Arduino 项目，这并不困难。它类似于 3D 打印机的绘图仪或 XY 工作台——只是一些步进电机和线性运动硬件。但是，基数需要非常稳定。不过，我们学到了很多光学方面的知识。

两个尼康镜头和一个由黑色纸板制成的光圈形成了一个可信的 3 倍放大元件。我们还学习了数值孔径及其与景深的关系。

该项目可以改进的一个地方是软件部门。一旦你拍摄了大量的图像，它们需要融合在一起。当然，这可以手动完成，但这并不好玩。还有一个 MATLAB 脚本试图自动将图像缝合在一起，将边缘融合在一起。根据作者的说法，代码需要做一些工作才能完全可靠。也有现成的缝合解决方案，可能效果更好。

我们已经看到[相似的设置](https://hackaday.com/2013/09/01/scratch-built-gigapixel-scanner/)来成像不同的东西。我们甚至看到它被应用于[一台老式显微镜](https://hackaday.com/2016/06/29/automating-a-microscope-for-cnc-micrographs/)。