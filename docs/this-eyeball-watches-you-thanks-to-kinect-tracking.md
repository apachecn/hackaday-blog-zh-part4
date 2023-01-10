# 这个眼球通过 Kinect 追踪来观察你

> 原文：<https://hackaday.com/2021/10/29/this-eyeball-watches-you-thanks-to-kinect-tracking/>

眼球经常看着我们，但它们通常嵌在另一个人或动物的头骨里。当他们单独盯着你看的时候，他们会更加令人毛骨悚然。来自[allpartscombined]的这个万圣节项目旨在引出[那种确切的怪异氛围](https://hackaday.io/project/182345-an-eyeball-that-watches-you-using-kinect)。

该项目依靠 Kinect V2 来进行身体跟踪。它向 Unity 应用程序输入数据，该应用程序会计算出如何将眼球对准场景中检测到的任何人。该应用程序通过串行方式向 Arduino 发送角度数据，微控制器生成必要的信号来命令伺服系统移动眼球。

随着倾斜和平移伺服系统的安装和 Kinect 数据的精确跟踪，眼睛可以在二维空间瞄准人。这比简单地来回扫视眼睛要可怕得多。

这个建筑实际上是通过修改一个早期的项目来创建一个气枪炮塔，[我们已经在这些部分](https://hackaday.com/2017/08/04/opencv-turret-tracks-motion-busts-airsoft-pellets/)见过几次了。从根本上来说，跟踪部分是相同的，只是在这种情况下，眼睛没有向人开枪…还没有！休息后的视频。

 [https://www.youtube.com/embed/jNCQnDVfFmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jNCQnDVfFmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

