# 带 Chrome 的蓝牙控制

> 原文：<https://hackaday.com/2019/10/17/bluetooth-control-with-chrome/>

现在所有很酷的项目都可以连接电脑或手机进行控制，对吗？但创建一个运行在不同平台上的应用程序来与你的项目对话是一件痛苦的事情。[凯文·达拉]说不，并展示了如何使用谷歌浏览器来做脏活。他拿了一个普通的 Arduino 和一个便宜的蓝牙接口板，然后[通过 Chrome](https://www.youtube.com/watch?v=w_mRj5IlVpg) 控制它。你可以看下面的视频。

HM-10 板很便宜，几乎可以连接任何东西。控制应用程序使用 Processing，这是 Arduino 系统衍生的软件。那么如何从加工到 Chrome 呢？简单。p5.js 库允许在 Chrome 中进行处理。还有一个面向 P5 的蓝牙 BLE 库。

一旦你了解了这些库，你可能就知道剩下的了。但是[凯文]展示了一个很好的例子，你可以很容易地复制。Arduino 和蓝牙代码并不难理解。处理程序看起来很像带有设置和循环功能的 Arduino 程序，但它也有画布、按钮和其他一些 Arduino 中通常没有的东西。

创建一个与硬件对话的 Chrome 应用程序非常容易。我们通常使用的手机应用程序是 [Blynk](https://hackaday.com/2016/03/10/app-control-with-ease-using-blynk/) 。我们甚至[用它作为机器人](https://hackaday.com/2016/12/01/the-joy-of-the-esp8266-and-blynk/#more-231533)的操纵杆。

 [https://www.youtube.com/embed/w_mRj5IlVpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w_mRj5IlVpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

