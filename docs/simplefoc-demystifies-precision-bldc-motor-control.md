# SimpleFOC 揭开精密 BLDC 电机控制的神秘面纱

> 原文：<https://hackaday.com/2021/07/07/simplefoc-demystifies-precision-bldc-motor-control/>

无刷 DC (BLDC)电机是低精度，快速钢筋混凝土应用的标准票价。需要缓慢或精确运行它们的控制方案深入到电机理论中，可能会使这些电机超出你的下一个自制机器人项目的范围。[Antun Skuric]和工作人员的目标就是改变这一切。他们采用了*场定向控制*算法，并将其封装到一个紧凑的 Arduino 库中，添加了大量示例，并制作了一个可堆叠的 BLDC 电机控制屏蔽。他们努力的总和被纳入到 [SimpleFOC 项目](https://simplefoc.com/)中，目的是将精确的 BLDC 控制带给广大的新黑客社区。

磁场定向控制是一种 BLDC 电机控制方案，涉及使用微处理器控制定子绕组电流，使其始终向转子施加扭矩。这样做需要您的处理器测量电机电流(想想:分流电阻)和转子位置(想想:编码器)。然而，实现该算法可能会有点棘手，因为它涉及到线性代数、电机物理和控制理论的一些内容。但这就是 SimpleFOC 背后的魔力。图书馆唾手可得，你不必如此！因此，无刷电机控制的最困难部分变得更加简单，这是一种几乎即插即用的解决方案。

SimpleFOC 已经被实现为扩展到各种可能的实现。虽然您当然可以设计自己的控制板，但也可以从单个电机的 SimpleFOC 电机屏蔽层开始，其电流最高可达 5 A。从那里，你有相当多的微控制器可供选择，因为该库已经扩展到 Arduino、Teensy、STM32 和其他一些微控制器系列。对于实现细节、理论和设置，有一套健康的[文档](https://docs.simplefoc.com/)可供参考。如果你想分享你的项目或提出问题，你可以进入[社区论坛](https://community.simplefoc.com/)寻求一些击掌和建议。最棒的是，[源代码](https://github.com/simplefoc/Arduino-FOC)已经在慷慨的 MIT 许可下提供给你享受。

虽然该项目于去年启动，但它正在不断改进，除了位置控制之外，还增加了对电流感测和扭矩控制的支持。随着项目周围健康社区的出现，我们将密切关注更多基于这一出色参考设计的项目。

如果 BLDC 电机控制引起了你的兴趣，看看我们的其他 BLDC 电机控制项目的档案，包括[电机/控制器混合](https://hackaday.com/2020/11/07/how-to-improve-a-smart-motor-make-it-bigger/)、[防齿槽控制方案](https://hackaday.com/2016/02/23/anti-cogging-algorithm-brings-out-the-best-in-your-hobby-brushless-motors/)和其他[低速位置控制器](https://hackaday.com/2015/04/20/driving-a-brushless-dc-motor-sloooooooowly/)。如果你准备好迎接真正的挑战，[为什么不也 3D 打印马达呢](https://hackaday.com/2017/05/08/powerful-professional-brushless-motor-from-3d-printed-parts/)？

 [https://www.youtube.com/embed/Y5kLeqTc6Zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y5kLeqTc6Zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

