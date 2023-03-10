# 橡树视觉模块帮助你看到森林和树木

> 原文：<https://hackaday.com/2020/08/09/oak-vision-modules-help-you-see-the-forest-and-the-trees/>

OpenCV 是一个计算机视觉算法的开源库，它的强大和灵活性使得许多机器视觉项目成为可能。但是，即使代码经过高度优化以获得最佳性能，我们总是希望得到更多。这就是为什么每当我们听到硬件加速视觉模块时，我们的耳朵就会竖起来，最近的嗡嗡声来自于 [OpenCV AI Kit (OAK) Kickstarter 活动](https://www.kickstarter.com/projects/opencv/opencv-ai-kit)。

本次活动推出了两个愿景模块。OAK-1 配有用于二维视觉应用的单色摄像机，OAK-D 增加了用于三维视觉应用的立体摄像机。板载大脑是 Movidius Myriad X 处理器，据研究其数据表的团队成员称，该处理器在其他产品中未得到充分利用。他们相信 OAK 模块将有助于芯片实现其视觉应用的潜力，在小尺寸中提供高性能，同时消耗低功率。阅读规格表，我们认为称这些为“终极无数 X 开发板”是公平的，但我们必须承认“OpenCV AI Kit”听起来更好。它没有为整个 OpenCV 库提供硬件加速(这可能是一个不可能的任务)，但它覆盖了适合 Myriad X 加速的高要求子集。

自从几周前发起运动以来，一些额外的信息已经发布，以帮助向支持者保证这个项目有真正的实质内容。事实证明，OAK 是一个我们一年前报道过的项目的演变，这个项目成为了真正的产品，所以至少这不是他们的第一次竞技。同样令人鼓舞的是，他们对开放硬件社区的邀请已经结出了果实。查看[这篇讨论 OAK for robot vision](https://discourse.ros.org/t/opencv-ai-kit-oak/15406/14) 的帖子，OAK 团队诚实地回答了一个问题“我们没有这方面的专业知识”，但之后 ArduCam 用他们的相机模块经验提供了帮助。

我们祝愿他们在计划的 2020 年 12 月交付中取得成功。他们已经远远超过了他们的资金目标，他们以前已经发运了硬件，我们看到了一个开发社区的良好开端。我们期待 OAK-1 和 OAK-D 加入其他黑客友好视觉模块的行列，如 [OpenMV](https://hackaday.com/2016/12/29/the-story-of-kickstarting-the-openmv/) 、 [JeVois](https://hackaday.com/2017/05/17/jevois-machine-vision-camera-nails-demo-mode/) 、 [StereoPi](https://hackaday.com/2018/12/30/this-raspberry-pi-is-a-stereo-camera-and-so-much-more/) 和 [AIY 视觉](https://hackaday.com/2017/12/17/googles-aiy-vision-kit-augments-pi-with-vision-processor/)。