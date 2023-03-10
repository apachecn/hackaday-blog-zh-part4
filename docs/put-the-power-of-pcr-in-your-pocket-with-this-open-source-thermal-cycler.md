# 使用这款开源热循环仪，将 PCR 的强大功能放入您的口袋

> 原文：<https://hackaday.com/2020/01/26/put-the-power-of-pcr-in-your-pocket-with-this-open-source-thermal-cycler/>

当第一台用于聚合酶链式反应的热循环仪在 20 世纪 80 年代问世时，它们的价格是由赠款驱动的市场所能提供的最高价格。这些年来，情况并没有好转多少，很大程度上将干细胞课程和生物黑客排除在 PCR 市场之外。不过，如果价格为 99.00 欧元的 PocketPCR 热循环仪开始流行，这种情况可能会改变。

PCR 通过三个步骤放大 DNA:变性，将双链 DNA 熔化成单链；退火，让小片段引物 DNA 结合到感兴趣区域的任一侧；和延伸，其中 DNA 聚合酶沿着从引物开始的单链拉链移动以复制 DNA。循环重复，原始 DNA 的拷贝以指数方式积累。像任何热循环仪一样，[Urs Gaudenz]的 PocketPCR 通过结合使用安装在 PCB 上的加热元件和冷却风扇来自动进行温度转换。线圈将反应块快速加热到 99℃的变性温度，风扇将温度降低到退火所需的 68℃，然后温度回升到 72℃，以便用[热稳定的 DNA 聚合酶](https://hackaday.com/2016/03/22/enzymes-from-the-deep-the-polymerase/)进行延伸。PID 回路使反应温度得到精确控制。顾名思义，整个系统小到可以装进口袋，既可以以套件形式购买，也可以从 GitHub 上的[构建文件中临时构建。](https://github.com/GaudiLabs/PocketPCR)

我们为[Urs]将 PCR 的力量传递到公民科学家手中的努力喝彩。[快速和肮脏的热循环仪](https://hackaday.com/2012/09/09/genetic-research-on-the-cheap/)是一回事，但袖珍 PCR 具有很好的适应性和光洁度，使其更容易使用。

感谢[Abe Tusk]的提示。