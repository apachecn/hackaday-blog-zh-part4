# 一个更好的小鸡行走马达

> 原文：<https://hackaday.com/2019/06/24/a-better-motor-for-chickenwalkers/>

过去十年左右，机器人和业余爱好应用的电机技术取得了显著进步。我们不再受困于蹩脚的有刷电机，现在我们有了花哨(而且便宜！)步进电机，无人机无刷电机，伺服电机。这导致了一些令人难以置信的成就；无人机只有用有刷电机才勉强可能，没有编码器你就造不出机器人。

为了参加 Hackaday 奖，[Gabrael Levine]正在接受最困难的机器人挑战之一:双足机器人。[是小鸡沃克，或者 AT-ST](https://hackaday.io/project/160882-blackbird-bipedal-robot)；无论哪种方式，你都需要在一个非常小的空间里有很大的动力，这就是开启扭矩致动器的[的用武之地。这是一种准直接驱动马达，最初由麻省理工学院仿生实验室首创。](https://hackaday.io/project/159404-opentorque-actuator)

OpenTorque 执行器的主要特点是使用一个大的无刷电机、一个旋转编码器和一个小的 8:1 行星齿轮组。这使得电机可以反向驱动，能够进行力感测和开环控制，因为这种致动器是 3D 打印的，所以生产成本非常低。

但是没有底盘的马达什么都不是，这就是[黑鸟双足机器人](https://hackaday.io/project/160882-blackbird-bipedal-robot)的用武之地。为了与机器人设计的最佳实践保持一致，运动学首先在模拟中进行测试，机械制造同时进行。这意味着有一些很棒的关于这只小鸡漫步的视频(下面有)，到目前为止，一切看起来都很棒。这种双足机器人可以转弯、行走、偏转，目前正在努力让这种鸟腿机器人保持静止。

 [https://www.youtube.com/embed/EzWQGBFH6xY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EzWQGBFH6xY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/2hsYPRzH3k8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2hsYPRzH3k8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

