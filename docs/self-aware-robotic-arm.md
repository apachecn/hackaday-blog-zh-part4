# 自我感知机器人手臂

> 原文：<https://hackaday.com/2019/04/24/self-aware-robotic-arm/>

如果你曾经试图对一个机械臂或几乎任何具有超过 3 个自由度的机器人机构进行编程，你会知道编程的很大一部分是对运动本身的编程。如果你造了一个机器人，不管你如何连接马达和关节，在没有自身知识的情况下，机器人会意识到它的物理构造方式？

这就是哥伦比亚工程研究人员通过[创造一个能够学习](https://www.eurekalert.org/pub_releases/2019-01/cuso-asc012819.php)如何连接的机器人手臂所做的，没有任何物理学、几何学或电机动力学的先验知识。起初，机器人不知道它的形状，它的马达如何工作，以及它们如何影响它的运动。经过一天以非常随机的方式尝试自己的输出并获得其行动的反馈后，机器人使用深度学习技术创建了一个准确的内部自我模拟。

利普森和他的博士生罗伯特·科维亚特科夫斯基在这项研究中使用的机械臂是一个四自由度铰接机械臂。第一个自我模型是不准确的，因为机器人不知道它的关节是如何连接的。经过大约 35 个小时的训练，自我模型与实体机器人的误差在 4 厘米以内。然后，自模型执行一个拾取和放置任务，使机器人能够完全基于内部自模型在轨迹的每一步之间重新校准其原始位置。

为了测试自我模型是否能够检测到自身的损伤，研究人员 3D 打印了一个变形的零件来模拟损伤，机器人能够检测到这种变化并重新训练它的自我模型。新的自我模型使机器人能够在几乎不损失性能的情况下继续其拾取和放置任务。

由于内部表示不是静态的，这不仅有助于机器人随着时间的推移改善其性能，还允许它适应自身结构的损坏和变化。这可以帮助机器人在零件开始磨损时，或者，例如，当替换零件的格式或形状不完全相同时，继续更可靠地工作。

当然，这只手臂还需要很长时间才能达到接近 2018 年 Hackaday 奖得主 Dexter 的精度，但看到这项研究的视频仍然很酷:

 [https://www.youtube.com/embed/4dp_iiESLo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4dp_iiESLo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

