# Dashing Diademata 推出第二代 ROS

> 原文：<https://hackaday.com/2019/06/06/dashing-diademata-delivers-second-generation-ros/>

一个执行循线或避障的简单机器人可以将其所有逻辑放在一个 Arduino 草图中。但是随着机器人自主性的增加，其相应的软件变得非常复杂。用不了多久，诊断监控和日志记录就会派上用场，或者封装功能区域并协调它们如何协同工作的愿望也会实现。这就是像机器人操作系统(ROS)这样的工具的用武之地，所以我们不必重复发明这些轮子。Open Robotics [刚刚发布了 ROS 2 *给我们大家使用。*](https://discourse.ros.org/t/ros-2-dashing-diademata-released)

ROS 是一个开源项目，自 2007 年以来一直在进行，并定期更新，每一个[都以一个海龟物种](http://wiki.ros.org/Distributions)命名。是什么让这一个值得格外关注？*冲刺*标志着 ROS 2 的首次长期支持(LTS)发布，这是一个更新的第二代 ROS。所有的高级概念保持不变，这意味着几乎所有在[我们的 ROS 定位指南](https://hackaday.com/2018/05/31/modular-robotics-made-easier-with-ros/)中的东西在 ROS 2 中仍然适用。但是在过去的十年里，在引擎盖下发生了巨大的变化，反映了技术的进步。

ROS 是在一个 Unix 工作站花费数千美元、XML 将成为我们在线交流所有数据的方式、自主机器人[比高端豪华汽车](http://www.willowgarage.com/pages/pr2/order)还要贵的时代建立的。现在我们有 35 美元的树莓 Pi 运行 Linux，XML 由于处理开销已经失宠，一些自主机器人 ***是*** [高端豪车](https://www.autoware.auto/)。出于这些以及许多其他原因，开放机器人的人们决定是时候与遗留代码彻底决裂了。

这一突破也有其批评者，因为它意味着留下研究人员多年来发布的大量免费可用的机器人智能模块。流行的已经(或将)移植到 ROS 2，有一个翻译桥足以处理一些，但其余的将被留下。然而，这一更新也解决了许多阻止在研究之外采用的交易破坏者，使 ROS 对商业投资更具吸引力，这将使更多的机器人成为主流。

从对发布公告的反应来看，有很多人渴望将 ROS 2 投入使用，但它不是唯一新鲜出炉的机器人框架。我们刚刚看到 Nvidia 发布了他们的 [Isaac 机器人引擎](https://hackaday.com/2019/06/01/nvidia-jetson-robots-get-a-head-start-with-isaac-software-tools/),该引擎是为充分利用他们的 Jetson 硬件而定制的。