# RasterCarve 将图像转换为 CNC

> 原文：<https://hackaday.com/2020/01/19/rastercarve-converts-images-to-cnc/>

数控机床是黑客工具集的重要组成部分。这些由计算机控制的木材、金属和其他材料的切割机可以在短时间内将设计转化为原型，使重复项目的过程更加容易。然而，创建这些设计的软件可能会很昂贵，所以[Franklin Wei]决定[编写自己的](https://www.fwei.tk/blog/opening-black-boxes.html)。特别是，他决定编写自己的程序来雕刻图像，将照片转换成可以切割的刀具路径。结果是 [RasterCarve](https://rastercarve.live/) ，一个将图像转换成可输入数控机床的 GCode 的网络应用程序。

这个项目的动机是学习如何做，但同时也是对软件成本的失望，例如 [PhotoVCarve](https://www.vectric.com/products/photovcarve) 。花费 149 美元，这个程序做的和[魏]写的那个差不多，只是增加了一些额外的功能。他出色地描述了转换过程的工作原理:他的代码创建了一系列穿过图像的路径，然后将每个像素的颜色转换为深度:图像越暗，切割越深。

他还描述了将这个简单的代码[转换成 Javascript web 应用](https://www.fwei.tk/blog/a-c-programmer-learns-javascript.html)的过程，这个过程让许多程序员疯狂。这只是表明，虽然使用别人的东西是好的，但尝试自己做往往是有意义的。