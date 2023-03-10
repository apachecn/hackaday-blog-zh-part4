# 基于 Google Coral 的智能相机

> 原文：<https://hackaday.com/2021/06/30/smart-camera-based-on-google-coral/>

随着机器学习和人工智能变得越来越普遍，可供任何人尝试该技术的平台数量也在增加。就像过去十年的单板计算机革命一样，我们目前正在目睹一场类似的革命，机器学习平台的数量也在增加。其中之一是 Google Coral，这是一套专为利用这项新技术而设计的硬件。虽然它缺少对某些硬件的支持，所以[Ricardo]开始使用树莓 Pi Zero 和基于 Google Coral 构建的智能相机[。](https://github.com/ricardodeazambuja/Maple-Syrup-Pi-Camera)

该项目使用带有 USB 加速器的谷歌珊瑚边缘 TPU 作为机器学习的基础。Pi Zero 的完整图像是可用的，它立即设置了系统的大部分，包括无头操作，并包括一系列机器学习软件，如 OpenCV 和[pytesserac](https://pypi.org/project/pytesseract/)。通过将相机与 Edge TPU 和 Raspberry Pi 配对，[Ricardo]用几个示例项目展示了它的许多机器学习能力，例如自动车牌检测器，甚至可以识别面具是否戴着，甚至戴得有多正确的模式。

对于那些想进入机器学习和人工智能领域的人来说，这是一个很好的入门项目，因为使用这些硬件的入门成本非常低。所有的项目代码和例子都可以在[Ricardo]的 GitHub 页面上找到。我们甚至可以想象他的车牌识别软件被用来增强这个[车牌阅读器，它使用一个更强大的摄像头](https://hackaday.com/2016/08/31/big-brother-and-others-are-watching-your-car/)。