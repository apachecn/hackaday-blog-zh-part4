# 优先考虑机械多路复用器

> 原文：<https://hackaday.com/2021/05/04/prioritising-mechanical-multiplexer/>

当自动化几乎任何中等复杂的机械任务时，致动器和驱动电子设备会很快变得昂贵。机械多路复用可能是一种选择，而不是每个动作都使用一个致动器。[詹姆斯·布鲁顿]已经考虑在他的许多机器人项目中使用它，所以他建造了一个[优先机械多路复用器](https://www.youtube.com/watch?v=WwCmzwSE98o)来展示这个概念。

基本思想是有一个单一的驱动器，并在不同的输出之间动态切换。在他的演示中，[詹姆斯]使用了一个安装在移动平台上的电机，该电机由一个丝杠驱动，可以啮合许多不同的输出齿轮。每个输出转动一个刻度盘，目标是使刻度盘的位置与电位计的位置相匹配。“优先化”部分出现在许多输出需要调整的地方，系统必须选择先做哪一个。这很快就变成了一个任务调度问题，因为有许多因素可以用来确定优先级。休息后观看视频，了解不同的算法。

根据需要，所有输出可以通过离合器连接到单个主轴，而不是移动致动器。机械多路复用器的可能应用包括点胶机和生产线自动化。显然，Radioshack 在 80 年代出售的 Armatron 机械臂使用了类似的系统，用一个电机控制其所有功能。

[James]对机器人技术略知一二，在过去几年中已经制造了许多机器人。看看 [OpenDog](https://hackaday.com/2018/06/11/james-bruton-is-making-a-dog-opendog-project/) 和他的 [Start Wars 机器人](https://hackaday.com/2016/12/10/speed-run-james-brutons-star-wars-builds/)就知道了。

 [https://www.youtube.com/embed/WwCmzwSE98o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WwCmzwSE98o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

