# 逆向工程硅，一次一个晶体管

> 原文：<https://hackaday.com/2021/04/03/reverse-engineering-silicon-one-transistor-at-a-time/>

许多人会惊叹于通过解封集成电路并通过检查原始硅芯片解码其秘密而实现的逆向工程的壮举。我们中很少有人会亲自尝试，但这并不妨碍这个过程令人着迷。幸运的是[Ryan Cornateanu]手头有[一步一步地描述他的解封艺术之旅](https://ryancor.medium.com/pulling-bits-from-rom-silicon-die-images-unknown-architecture-b73b6b0d4e5d)，因为他以你会在 Arduino Nano 板上找到的 CH340 USB 转串行芯片的形式进行了一个看起来不太可能的主题。

从热硫酸开始可能不是每个人在工作台上一天的想法，但是用它从 CH340 上剥离环氧树脂后，他能够在显微镜下观察。这不是普通的显微镜，而是冶金学家设计的一种仪器，用偏振光从一侧照亮样品的顶部。这使他能够识别掩模 ROM 的一个区域，并放大构成每一位的晶体管。

在这一点上，化学移动到彻头彻尾的可怕，因为他达到氢氟酸，并不得不使用聚四氟乙烯容器，因为 HF 是臭名昭著的贪婪的反应。这使得他可以拿走互连，查看晶体管层。然后，他可以通过一点计算机视觉处理来帮助提取位图层，通过一些实验和猜测，可以将该位图层操作到固件转储中。即使这样也没有完成，因为他把我们带入了一个未知建筑的拆解世界。绝对值得扶手椅芯片爱好者一读。

如果你还想知道更多，[我们当然会把你引向[Ken Shirriff]](https://hackaday.com/2018/12/05/hold-for-publishing-plan-ken-shirriff-explains-his-techniques-for-reverse-engineering-silicon/) 的作品。