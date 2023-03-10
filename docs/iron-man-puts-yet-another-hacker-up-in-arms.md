# 钢铁侠让另一名黑客奋起反抗

> 原文：<https://hackaday.com/2019/11/28/iron-man-puts-yet-another-hacker-up-in-arms/>

当《钢铁侠》电影上映时，我们敢打赌，没有一个黑客离开电影院时不梦想拥有几个自己的机器人实验室助手。但与他们中的大多数人不同，[托尼-林]决定将他的电影梦想变成现实，[开始研制他的机器人手臂，大约在](https://hackaday.io/project/165455-open-source-robotic-arm-abot)。

Abot 由 5 毫米尼龙面板和 3D 打印零件组合而成。我们发现[关于这种构造特别有趣的一点](https://hackaday.com/2018/09/04/a-servo-powered-robotic-arm-but-like-youve-never-seen-before/)是，关节的电机减速是使用滑轮和 GT2 皮带级完成的，而不是行星齿轮箱或摆线驱动器。这产生了重量轻且可负担的构造。

他还使用 STM32 为每个电机设计了自己的驱动板。它们通过使用 USB 连接器的 CAN 总线进行通信，这是一个有趣的选择。只要确保不要试图用它给你的手机充电。

我们不得不承认有点嫉妒，托尼比我们其他人更接近托尼·斯塔克。我们将不得不通过他的项目文件来替代生活。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)