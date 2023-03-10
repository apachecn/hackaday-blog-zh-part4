# 这是废物管理的未来

> 原文：<https://hackaday.com/2022/12/04/this-is-the-future-of-waste-management/>

一段时间以来，我们许多人一直在问“我们的机器人仆人在哪里？”我们被许诺过这种休闲奢华的梦幻生活，但我们仍在等待。现代生活是一种非常浪费的生活，只需点击一下鼠标，商品就会送到我们的门口，但包装的处理仍然是一件手工的事情。如果能够召唤一个机器人去回收垃圾，最好是同时让它去拿啤酒，这不是很棒吗？[詹姆斯·布鲁顿]分享这个梦想，并凭借他广泛的机器人技术，想出了完美的解决方案； [看哪 Binbot 9000](https://www.youtube.com/watch?v=j0aKJHhNAhc) 。(视频，下方嵌入 break)

这款现成的垃圾桶采用铝型材制成框架，在需要的地方用 t 型螺母固定在 3D 打印件上，非常合适。该基地有一个三轮方法与后置脚轮。在正面，一对[Gimson robotics](https://gimsonrobotics.co.uk/)24v 蜗杆减速电机以两轮差动排列方式驱动每个车轮，每侧都有一个 3D 打印的 TPU 轮胎。框架背面的一个大伺服电机拉动连接到安装在箱盖上的叶片的绳索，完成机械结构。

通过 Arduino Mega 连接到一对安装在小型 PCB 上的 BTS7960 高电流 H 桥驱动器来控制电机，每个电机顶部都有车轮编码器，以提供一些基本的航位推算导航。然而，正如[James]解释的那样，由于车轮旋转和其他外部因素造成的累积误差使室内航位推算导航成为一种死物，因此 Nvidia Jetson Nano 与 Raspberry Pi 摄像头和一些基准标记一起使用，以提供更准确的定位系统。强制性的眼睛为机器人的美学增添了点睛之笔。但这并不是全部的解决方案。正如[詹姆斯]所展示的，按下调试按钮来启动机器人是没有用的。语音召唤是构建的最后一部分，利用 [DeepGram](https://deepgram.com/) 基于人工智能的语音识别告诉机器人去哪里。所有需要做的就是插入一个 USB 全向麦克风，并在 Jetson 上添加一些额外的脚本，然后它就走了。

现在它所需要的是与冰箱接口并取出啤酒的能力，我们已经成功了。随意挖掘 [项目 GitHub](https://github.com/XRobots/RobotBin) 添加拉取请求！

关于语音控制取啤酒机器人，这是一个已经解决的问题，但是它不能为你回收空瓶子。

 [https://www.youtube.com/embed/j0aKJHhNAhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j0aKJHhNAhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

