# Pac-Man 热降临 Pano Logic FPGA

> 原文：<https://hackaday.com/2019/01/11/pac-man-fever-comes-to-the-pano-logic-fpga/>

如果你已经阅读 Hackaday 有一段时间了，你可能会想起我们在 2013 年首次报道的 Pano Logic 的故事。他们是一家推出了一些非常有趣的基于 FPGA 的瘦客户机的公司，但正如在这种情况下偶尔发生的那样，市场还没有准备好，公司破产了。这些瘦客户，现在没有官方支持，总是被扔到二手市场。对 Pano Logic 和他们的员工来说是耻辱，但对像[Skip Hansen]这样的黑客来说是好消息。

[![](img/133a40b8e7fd56fb5dedfd1c99ffdacf.png)](https://hackaday.com/wp-content/uploads/2019/01/pacpga_detail.jpg) 在看到一些关于 Pano 逻辑设备和通用 FPGA 黑客的帖子后，他决定在易贝上抓几个，然后一头扎进去。使用开源工具和可用的大量信息[【Skip】能够在他的假期](https://github.com/skiphansen/pano_man)启动并运行一个吃豆人模拟器，他告诉我们他的生活可能再也不会一样了。FPGA 黑客是一个迷人的主题，现在有很多活动，因为在某些情况下，你可以在易贝以不到 10 美元的价格获得这些 Pano Logic boxes，现在是一个让你的脚湿起来的好时机。

像许多开源项目一样，[Skip]说他的代码是建立在许多其他程序员的现有工作基础上的，这让他能够比从零开始更快地启动和运行。他将自己的代码描述为将这些项目融合在一起的“胶水”，但我们认为他在这方面有些谦虚。要让 Blinky、Pinky、inky 和 Clyde 在 Pano Logic 上做他们的事情，需要的不仅仅是复制和粘贴一些代码到 IDE 中。

最大的挑战是缺乏 I/o。Pano Logic 瘦客户端有 USB 端口，但似乎没有人知道如何让它们工作。为了与外界交流，你必须变得更有创造力。最终[Skip]找到了四条可以有效用作 GPIO 的线路:两条用于驱动设备上的 led，两条用于 VGA 端口的显示数据通道(DDC)引脚。从 led 到设备 VGA 连接器中未使用的引脚的焊接跳线意味着他甚至能够从 Pano Logic 的外部访问这四条 GPIO 线，而不必在外壳上切割任何孔。

任何拥有 Pano Logic 客户端的人，只要有 VGA 端口，Atari 2600 操纵杆，并且不介意焊接几根电线，现在就可以用[Skip]提供的比特流玩 Pac-Man 了。但我们将何去何从？我们还要多久才能看到厄运降临？也许你们中的一个优秀读者应该拿起一个，看看你能做些什么来推进 Pano Logic hacking 的状态。一定要让我们知道这件事。

我们之前已经报道过一个用于让这个 Pac-Man 模拟器起飞的项目，这是一个由[Tom Verbeure] 开发的 Pano Logic 的非常酷的光线跟踪演示。事实上，[Skip]说，正是这个项目让他对 FPGA 黑客产生了兴趣。如果你想追随他的脚步，[你可能也想看看我们的 FPGA 训练营](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)。