# 8 位视频卡中一些令人愉快的实验

> 原文：<https://hackaday.com/2021/10/03/some-pleasing-experiments-in-8-bit-video-cards/>

如今，供应链因素和高需求使得人们很难找到一款 GPU。然而，如果你对旧电脑感兴趣，你可能会发现很难找到老式显卡。不用担心，因为[戴夫的开发实验室]一直在炮制一些实验，目标是最终从头开始生产一种新的 8 位 ISA 视频卡。

长期目标是重建早期 IBM 硬件的原始设计，即几十年前的 MDA 和 CGA 视频卡。实验围绕古老的摩托罗拉 6845 展开，它在 20 世纪 80 年代被广泛应用于计算机。然而，[Dave]打算使它们适合输出到使用典型 VGA 和 DVI 输出的现代屏幕，以及现代 TFT LCDs 所期望的那些屏幕。

到目前为止，【Dave】已经在 40×35 文本模式下实现了[成功的 VGA 输出](https://hackaday.io/project/167089-isa-8-bit-video-experiments/log/170184-ive-got-vga-output)。使用 8×16 的字体，显示器以 640×480 的分辨率在 60 赫兹下运行，一切都很和谐。现代 480×272 液晶显示器[的类似实验也运行良好](https://hackaday.io/project/167089-isa-8-bit-video-experiments/log/167333-video-test-pattern-on-lcd)。

在[戴夫的]硬件扮演指挥官基恩之前还有很长的路要走，但很高兴看到这样的努力被投入到平台中。对于那些希望使用他们的老式 IBM metal 而不必购买一台旧的 CGA 显示器的人来说，它仍然是一个很好的升级。

我们以前也见过类似的工作，[《地铁时代》中的图形精灵完成了类似的任务。](https://hackaday.com/2021/05/18/retro-isa-card-means-old-slow-computers-no-longer-need-old-heavy-monitors/)如果你一直在家里酝酿自己的 ISA 硬件，[请给我们写封短信](http://hackaday.com/submit-a-tip)。