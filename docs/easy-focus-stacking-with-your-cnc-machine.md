# 使用您的数控机床轻松聚焦堆叠

> 原文：<https://hackaday.com/2020/09/07/easy-focus-stacking-with-your-cnc-machine/>

微距摄影是一种在非常近的距离拍摄事物的艺术，最好是非常详细的照片。不幸的是，相机在近距离的景深很差，所以为了解决这个问题，许多相机使用了聚焦叠加技术。这包括以不同的焦距拍摄许多照片，并以数字方式将它们合成在一起。为了帮助实现这一目标， [[gtoal]意识到普通的数控机床将非常适合这项工作](https://www.instructables.com/id/Convert-Your-CNC-to-a-Macro-Photography-Rail-in-30/)。

为了有效地聚焦，最好以亚毫米精度的微小增量来移动相机，以便聚焦主体的不同部分。在这方面，数控机床表现出色，因为它被设计成以非常微小、精确的运动来移动工具头。

为了获得便宜的 focus 堆垛设备，[gtoal]使用了 Dremel 工具架来切割光盘。它在这里被重新利用，作为一种通过安装孔将 Raspberry Pi 相机安装到 CNC 工具头的简单方法。从那里开始，这是一种简单的方式，在 Z 轴上一次一点点地步进 CNC，同时一路上用 Raspberry Pi 拍照。[gtoal]指出，对于一个有经验的 CNC 用户来说，编写一个程序来自动化整个过程是很简单的。

在之前，我们已经看到了其他[预算聚焦堆码设备，甚至还有一台](https://hackaday.com/2019/12/30/focus-stacking-for-tiny-subjects/)[报废的 3D 打印机被改造成了自动扫描显微镜](https://hackaday.com/2020/01/24/broken-3d-printer-turned-scanning-microscope/)。如果你有自己的顶级微距摄影技巧，[给我们留言吧！](http://hackaday.com/submit-a-tip)