# 线性 CCD 是更好的相机

> 原文：<https://hackaday.com/2019/05/30/linear-ccds-make-for-better-cameras/>

数码相机已经有四十年左右的历史了，第一批是围绕 CCD 制造的。这些是二维 CCD，如果你曾经看过复印机，扫描仪，或者 90 年代的那些奇怪的手持扫描仪，你会发现一些完全不同于你在数码相机里看到的东西。线性 CCD 就像它们听起来的那样——一行像素。如果你对光谱学感兴趣，这很好，但这些线性 CCD 也有一些令人疯狂的分辨率的优势。一个 4 英寸宽的线性 CCD 将有数千个像素，如果你能以某种方式拖动一个线性 CCD 穿过一幅图像，你将拥有一个了不起的相机。

许多人尝试过，但很少人成功，而“线性 CCD 相机”是迄今为止制作线性 CCD 相机的最佳尝试。它拍了一张模糊的树的照片，这对于概念验证来说已经足够好了。

本项目中使用的线性 CCD 的工作原理类似于模拟移位寄存器。使用差分时钟，您只需将值从 CCD 推出，然后馈入 ADC。这个 CCD 的驱动板使用了大量的电流，时序有点棘手，但它确实与 Teensy 3.6 工作。但那只是图像的一条线，你还需要移动 CCD。为此，这个项目使用了类似家酿 CD 驱动器的东西。有一个微小的步进电机和一个丝杠拖动 CCD 穿过图像平面。所有这些都附在 Mamiya RZ67 相机机身的背面。

有用吗？是的。出人意料的是。经过大量的工作，一棵树的图像被捕获。这是一个 RGB CCD，目前它只使用一个颜色通道，但它确实工作。这是以 2000 x 3000 灰度位图呈现的概念证明。最终目标是围绕这个 CCD 建造一个 3750 万像素的中画幅相机，进展看起来很棒。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)