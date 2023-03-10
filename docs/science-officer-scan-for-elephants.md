# 科学官…扫描大象！

> 原文：<https://hackaday.com/2021/03/17/science-officer-scan-for-elephants/>

如果你看许多以当今为背景的间谍或恐怖主义电影，通常会有这样一个场景:一些政府雇员增强了卫星图像，以显示出主要恶棍的清晰面孔。现代间谍卫星有那种分辨率吗？我们不知道，即使知道也不能告诉你。但是我们确实知道，即使使用非机密分辨率，科学家们也在使用卫星图像和机器学习来计算大象数量。

仔细想想，统计栖息地的野生动物数量是个难题。首先，如果你亲自去，你会打扰目标动物。即使是无人机也可能会让胆小的野生动物感到不安。还有一个问题是，试图覆盖一个大区域，并弄清楚你今天看到的大象是否与你昨天看到的是同一只。如果你猜错了，你会少算或多算。

牛津的科学家们用 Worldview-3 卫星来计算大象的数量。每天采集多达 68 万平方公里。你没有打扰到任何被观察的生物，而且由于每张照片覆盖了一大片区域，你重复计算的问题几乎消失了。

## 不唯一

显然，从太空数动物并不是什么新鲜事。蛮力，你让一个研究生从一张照片上数数。但是自动化方法在某些情况下是有效的。从鲸鱼到企鹅的一切都可以从轨道上计数，但通常使用水或冰作为背景。

甚至有人试图从二手资料中推断动物数量。例如，企鹅的数量可以通过它们在冰上留下的痕迹来估计。是啊，那些污渍。

然而，在南非阿多大象国家公园统计大象数量时，却没有明确的背景。地面被森林覆盖，经常下雨。另一个挑战是大象看起来并不总是一样的。例如，他们把自己裹在泥里降温。机器可以学习从高分辨率的太空照片中识别出截然不同的大象吗？

 [![Elephants in a clearing are easier to spot...](img/abadeadbf65a0fc0479f8f382d41c8ec.png "el1")](https://hackaday.com/2021/03/17/science-officer-scan-for-elephants/el1/) Elephants in a clearing are easier to spot… [![... than elephants in a thicket.](img/4833dba794bae7f89db6de3fbbfcb311.png "el2")](https://hackaday.com/2021/03/17/science-officer-scan-for-elephants/el2/) … than elephants in a thicket.

## 多高？

[![](img/8c33cfb7cac38ed14537f5215ec9b6bf.png)](https://hackaday.com/wp-content/uploads/2021/02/GeoEye-2crop.jpg)

Image copyright DigitalGlobe/Lockheed Martin

Worldview 卫星拥有目前商业用户可获得的最高分辨率。分辨率低至 31 厘米。对于美国人来说，这足以挑出大约 1 英尺长的东西。这听起来可能不太令人印象深刻，直到你意识到这颗卫星距离地球表面约 383 英里。这大致就像从纽约市拍一张照片，在弗吉尼亚州纽波特纽斯看到的东西。

研究人员并没有明确要求卫星观察公园。取而代之的是，他们从公园上方的通道中提取历史图像。你可以找到卫星有哪些数据，尽管没有订阅你可能得不到最好或最新的数据。但即使是你能得到的数据也相当令人印象深刻。

据该报称，他们使用的档案图像每平方公里的成本为 17.50 美元。要求获得新的图像会将价格推高到 27.50 美元，而且你必须购买至少 100 平方公里，所以卫星数据并不便宜。

## 培养

当然，机器学习的一个必要部分就是训练。一个测试数据集有 164 头大象，覆盖了 7 幅不同的卫星图像。人类通过计算来为训练提供假设的正确答案。使用评分算法，人类平均约为 78%，机器学习算法平均约为 75%——没有太大差异。就像人类一样，算法在某些情况下比其他情况下更好，有时可以达到 80%的匹配率。

## 免费数据

想在天上用你自己的眼睛做实验吗？不是所有的卫星数据都要花钱，尽管分辨率可能不适合你。显然，[谷歌地球](https://www.google.com/earth/)和[地图](https://www.google.com/maps/place/85634RVX+VH/@34.1446875,-118.1532512,947m/data=!3m1!1e3)可以给你看一些卫星图片。[美国地质调查局](https://earthexplorer.usgs.gov)也有大约 40 年的在线数据 [NASA](https://search.earthdata.nasa.gov/search) 和 [NOAA](https://coast.noaa.gov/digitalcoast/data/) 也有[相当](https://coast.noaa.gov/dataviewer/#/)位[位](https://www.avl.class.noaa.gov/saa/products/welcome)，包括 NASA 的高分辨率[世界观](https://worldview.earthdata.nasa.gov)。Landviewer 为你提供一些免费的图片，尽管你需要为最高分辨率的数据付费。ESA 运行哥白尼系统，它有来自哨兵卫星的几种类型的图像，你也可以从 T21 的 EO 浏览器或哨兵游乐场获得重要的数据。如果你不介意葡萄牙语，巴西人有一个很好的南半球图片门户。JAXA——类似于美国国家航空航天局——也有自己的 30 米分辨率数据网站。还有一个来自印度的对等词，ISRO。

[![](img/ffaeaa761bfa39964225467c53ea2422.png)](https://hackaday.com/wp-content/uploads/2021/02/v2.jpg)

The V-2 took this picture at 65 miles up in 1946.

如果你不想登录，[文森特·萨拉戈的] [远程像素](https://remotepixel.ca)网站让你无需注册就能访问来自 Landsat 8、Sentinel-2 和 CBERS-4 的数据。还有其他的也有: [UNAVCO](https://www.unavco.org) 、 [UoM](https://glad.umd.edu) 、 [Zoom](https://zoom.earth) 、 [VITO](https://vito.be/en) 。当然，其中一些图像的分辨率相当低(甚至高达 1 公里/像素)，因此根据您想要对数据做什么，您可能需要查看付费来源。

有各种各样的分辨率和数据类型，如可见光、红外或雷达。然而，这一切都超过了 1946 年的艺术水平，当时 V-2 照片是从 65 英里高处拍摄的。事情已经有了很大进展。

## 极高的

我们设想这些相同的技术可以用于空中摄影，就像你可以从无人驾驶飞机甚至杆子上的相机中得到的一样。这可能比购买卫星图像更划算。这让我们想知道还有哪些计算机视觉项目即将登场。

也许我们的 3D 打印机有一天会将它们的输出实时与输入模型进行比较，以检测打印问题。这将是最终的“细丝外”传感器，也可以检测床粘附的损失和其他异常。

来自热成像或电子束频闪观测的电子数据可以将伪图像作为像这样的算法的输入。想象一下，训练一台计算机知道一块好的电路板是什么样子，然后让它识别坏的电路板。

当然，你可以随时[抓取自己的卫星图像](https://hackaday.com/2013/01/04/pictures-from-weather-satellites-with-a-usb-tv-tuner/)。我们已经看到[做了很多次](https://hackaday.com/2020/03/14/get-your-weather-images-straight-from-the-satellite/)。