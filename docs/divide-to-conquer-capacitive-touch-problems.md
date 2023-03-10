# 分而治之，解决电容式触摸问题

> 原文：<https://hackaday.com/2019/06/13/divide-to-conquer-capacitive-touch-problems/>

过去，你所有的音乐都放在架子上(或者牛奶箱里),选择听什么是有形的行为。[Michael Teeuw]欣赏音乐点播的力量，但在“放点东西”的时候，却忽略了身体方面。他的解决方案是一个他称之为 MusicCubes 的硬件控制器。

![](img/d303d78eecf1fb26ddd67ced5978bf0e.png)

Music cube makes selection using RFID, and touching to the right raises the volume level

这是一个由多个部分组成的项目，但是最近的返工吸引了我们的眼球。该系统为每个相册使用带有 RFID 标签的立方体。控制器的这一部分工作起来像一个魔咒，只需将立方体放在控制器的凹陷部分——就像超人在孤独堡垒中的晶体一样——系统就知道你已经做出了决定。但是音量的触摸控制效果不好。偶尔他们会读到一个错误的触摸，大约一个小时后系统就会静音。他的研究发现，电容式触摸板本身需要更小。

在求助于硬件修复之前，[Michael]试图过滤掉软件中的误报。这只是取得了一些成功，所以他的下一个尝试是将大触摸板切割成四块板，只有当两块板同时记录一次按压时才会做出反应。

他正在使用 MPR121 电容式触摸传感器，该传感器具有多达 12 个键的输入，因此在现有硬件上进行这种改变没有问题。令人惊讶的是，一旦他为每个传感器安装了四个垫片，假阳性就完全消失了。该系统现在坚如磐石，无需过滤两个同时激活的子垫。其他人有没有遇到过用大盘作为触摸传感器的问题？这能很容易地过滤掉吗，或者[Michael 的]解决方案是继续进行的常用方法吗？在下面的评论中分享你自己的电容式触摸传感器技巧！

想看看整个项目吗？[从第一步](https://michaelteeuw.nl/post/180929903442/musicubes-part-1-concept-prototyping)开始，它包括其他构建日志的目录。