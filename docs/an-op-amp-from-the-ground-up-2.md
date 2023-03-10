# 一个全新的运算放大器

> 原文：<https://hackaday.com/2021/01/30/an-op-amp-from-the-ground-up-2/>

如果我们不得不挑选一个部件作为模拟电子世界中的通用部件，它将是运算放大器。不起眼的运算放大器可以配置成如此多的电路构建模块，它已经成为设计师不可或缺的工具。将运算放大器视为电路图中的三角形黑匣子很有吸引力，但理解其工作原理可以让我们深入了解值得拥有的模拟电子设备。[ Mitsuru Yamada ]的[自制的使用分立元件的运算放大器](https://hackaday.io/project/176860-homemade-operational-amplifier)因此是一个有趣的项目，因为它实现了一个完整的五晶体管简单运算放大器。

[![](img/91e6cd066d0299615397c3a8dc2bc71a.png)](https://hackaday.com/wp-content/uploads/2021/01/Mitsuru-Yamada_homemade_opamp.jpeg) 查看电路图，它跟随经典运算放大器，由一对长尾 NPN 晶体管驱动 PNP 增益级，最后由一个互补射极跟随器作为输出缓冲器。它集成了反馈电容，这在早期的运算放大器芯片中是一个外部元件，它还有几个可变电阻来调节偏置。目光敏锐的读者会注意到它的缺陷，如不可避免的不匹配晶体管和长尾对中缺乏电流镜，但利用这些来寻找为学习而构建的电路中的故障是题外话。他在使用中演示了它，甚至展示了它运行一个音频功率放大器来驱动一个小扬声器。

对于专门研究运算放大器的学生来说，[在我们研究第一款集成电路运算放大器](https://hackaday.com/2018/02/20/deconstructing-a-simple-op-amp/)时，我们可以建议进一步阅读吗？