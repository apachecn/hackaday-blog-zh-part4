# 自行车上安装的合成孔径雷达可以拍摄出详细的图像

> 原文：<https://hackaday.com/2019/08/15/bike-mounted-synthetic-aperture-radar-makes-detailed-images/>

合成孔径雷达，其中一个移动的雷达被用来模拟一个非常大的天线，并获得高分辨率的图像，通常不是业余爱好者的东西。然而，没有人告诉[Henrik Forstén]，因此我们有了这个自行车上安装的合成孔径雷达项目来惊叹。

使合成孔径雷达工作所涉及的电子学和数学都不是微不足道的，所以[Henrik]的全面综述对于理解正在发生的事情是非常宝贵的。第一步:建造一个 6 GHz 调频连续波(FMCW)雷达，这个项目是[Henrik]前一段时间承担的，真的让我们大吃一惊。他的 FMCW 装置足以分辨 100 米左右人体大小的物体。

下一步是沿着一条路径移动雷达和捕捉数据，这很简单，但弄清楚如何处理这些数据却绝非易事。[Henrik]详细介绍了他使用的 SAR 算法，称为 Omega-K，这是一个利用快速傅立叶变换的例程，他使用[张量流](https://hackaday.com/2017/04/11/introduction-to-tensorflow/)为 GPU 实现了该算法。我们通常在神经网络应用中看到这种情况，但代码产生了非常详细的 2D 扫描，他骑着自行车用车载雷达扫描了一个停车场。[Henrik]还增加了自动对焦程序，你可以清楚地看到雷达范围内的每辆停放的汽车、灯杆和远处的建筑。

我们发现[Henrik]能够用相对低预算的设备完成的事情非常令人惊讶。合成孔径雷达有很多应用，我们希望看到这种技术得到进一步完善和发展。

[通过[遥控/电子](https://www.reddit.com/r/rfelectronics/comments/cpu9qo/syntheticaperture_radar_imaging/?utm_medium=android_app&utm_source=share)