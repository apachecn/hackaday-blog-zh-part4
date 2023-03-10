# 开源机器人 Reachy 说你好

> 原文：<https://hackaday.com/2021/01/14/reachy-the-open-source-robot-says-bonjour/>

人形机器人总是吸引人的注意，但任何试图制造机器人的人都会很快学会尊重一种我们认为理所当然的形状因素，因为我们生来就有这种因素。花粉机器人公司希望通过 [Reachy](https://www.pollen-robotics.com/reachy/) 帮助推进该领域:一个机器人平台，既可以作为产品，也可以作为在线共享的大量信息。

这个法国团队以前发布过开源机器人。我们看过他们的 Poppy 机器人，发现它和 Reachy 有很强的家族相似性。罂粟是一个非常雄心勃勃的设计，既有胳膊又有腿，但它只能靠辅助[行走](https://www.youtube.com/watch?v=5AnbuB39dpo)。相比之下，Reachy 只关注上半身。最有趣的创新之一是在 Reachy's neck 中发现的，这是一个设计巧妙的三自由度机构，他们称之为[轨道](https://medium.com/pollen-robotics/orbita-is-turning-heads-literally-d10d378550e2)。结合头顶上两根活动的触角，Reachy 尽管没有太多的面部表情，却能做出各种各样的表情。Reachy 的其余关节是用 Dynamixel [串行总线伺服系统](https://hackaday.com/2018/07/05/wrangling-rc-servos-becoming-a-hassle-try-serial-bus-servos/)连接的，尽管我们在演示视频中看到了一个可选的基于 Orbita 的手部附件(嵌入在下面)。

相对于工业机器人，Reachy 的€ 19，990 英镑的价格可能是可以承受的，但对于家庭黑客来说，这太贵了。没有必要担心，我们这些银行账户较小的人仍然可以加入这一乐趣，因为花粉机器人已经开源了许多深奥的细节。深入挖掘这些信息，我们看到 Reachy 有一个用于加速 TensorFlow 的 [Google Coral](https://hackaday.com/2019/03/05/google-launches-ai-platform-that-looks-remarkably-like-a-raspberry-pi/) 和一个用于一般计算的 Raspberry Pi 4。机械设计通过基于网络的 Onshape CAD 发布。Reachy 在 GitHub 上的软件套件主要集中在 Python 上，它允许我们在 Jupyter 笔记本上进行实验。模拟可以在 Unity 3D 游戏引擎中完成，该引擎可以随意编译以在类似[模拟游乐场](http://playground.pollen-robotics.com/)的浏览器中运行。但是学术机器人研究人员并没有被排除在乐趣之外，因为 [ROS1 集成也是可用的](https://medium.com/pollen-robotics/reachy-now-runs-ros-934dcef40c95)，尽管 [ROS2](https://hackaday.com/2019/06/06/dashing-diademata-delivers-second-generation-ros/) 支持仍然在待办事项列表中。

Reachy 可能不像我们见过的一些人形设计那么复杂，而且没有下半身，它不可能跳舞。[。](https://hackaday.com/2020/12/30/boston-dynamics-dancing-bots-beg-for-your-love-a-la-napoleon-dynamite/)但我们非常感谢一家愿意与世界分享知识的公司。愿它为未来带来新的想法。

[via [Engadget](https://www.engadget.com/reachy-the-robot-can-now-be-controlled-via-vr-200508703.html)

 [https://www.youtube.com/embed/iSL39WFxCLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iSL39WFxCLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

