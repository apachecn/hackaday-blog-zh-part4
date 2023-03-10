# 打造您自己的卡特彼勒–需要一些组装

> 原文：<https://hackaday.com/2022/04/18/build-your-own-cat-some-assembly-required/>

机器人宠物是科幻材料，来自[Kev 的机器人]的[Kevin McAleer]正在让我们更接近一个更光明、更快乐、更机器人化的未来。他的最新机器人产品之一 [PicoCat 是一只带有伺服驱动爪子的机器猫](http://www.kevsrobots.com/blog/picocat-lives.html)。这是继 2016 年李荣忠博士[的 OpenCat 项目](https://hackaday.com/2018/03/06/the-sensor-array-that-grew-into-a-robot-cat/)之后，我们总是很高兴看到有人接手另一名黑客留下的工作。[Kevin]从 OpenCat 的设计中获得了很多灵感——用对今天的制造商来说更友好、更容易使用的硬件来重建它。

像这样的项目，涉及数据处理和计算以使伺服系统正确运行，将受益于最近发布的 RP2040 MCU 的计算能力。因此，Pimoroni Servo 2040 板是这一构建的关键组成部分，既是该项目的大脑，也是帮助这个机器人活过来的 11 个伺服系统的 PIO 推动的驱动器。这只猫的眼睛是一个超声波传感器，你可以为你的任何机器人意图添加更多的传感器。不要指望这只小猫能跳一米高或把你最喜欢的沙发抓破*现在还不到*，但它已经有很大的潜力，尤其是再加上一个小扬声器。

你对这只机器猫感兴趣吗，是因为你的科幻倾向还是对猫毛过敏？你很幸运，因为[凯文]是[保持事情稳定在“开源一切”领域](http://www.kevsrobots.com/blog/picocat-v2.html)。MicroPython 代码存储在 GitHub repo 的[中，STL 存储在链接到页面](https://github.com/kevinmcaleer/picocat)的`.zip` [中，并且有大量的渲染，永远不会让你搞不清什么去了哪里。有了所有这些资源，你可以采购伺服系统和电路板，启动你的 3D 打印机，坐下来组装你自己的微型计算机。不仅如此，[凯文]还录制了三个完整的视频流，给了我们四个多小时的视频材料，供我们学习。首先，](http://www.kevsrobots.com/blog/picocat-lives.html#stl-files--code)[他在 Fusion360 中设计 PicoCat 的两个流](https://www.youtube.com/watch?v=1mj3Ja2Zj0Q)，然后，他谈论了[他在 MicroPython](https://www.youtube.com/watch?v=TO5B9doMss0) 中创建单元测试的方式，以提高他的机器人的可靠性并显著减少出现的错误数量。

这并不是我们最后一次听到[凯文]的机器人工作室，之前，我们已经报道过他的[克雷-1 形 Pi 零集群系统](https://hackaday.com/2022/03/21/cluster-your-pi-zeros-in-style-with-3d-printed-cray-1/)和[树莓 Pi theremin】，它们都像这只小猫一样开放和可复制！当你给自己组装一只小猫咪，或者](https://hackaday.com/2022/03/28/raspberry-pi-creates-melody/)[一只史丹福小狗](https://hackaday.com/2020/05/12/robotic-open-source-puppy-needs-a-home/)或者任何其他我们之前介绍过的可爱的四脚宠物时，你可能会想知道如何正确地移动伺服系统，我们已经[报道了一个专门教你这个](https://hackaday.com/2015/05/07/the-simplest-quadrupedal-robot-ever/)的项目。

 [https://www.youtube.com/embed/9txATldoURE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9txATldoURE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

