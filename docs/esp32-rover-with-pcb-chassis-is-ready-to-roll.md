# 带 PCB 底盘的 ESP32 漫游者准备上路

> 原文：<https://hackaday.com/2020/03/02/esp32-rover-with-pcb-chassis-is-ready-to-roll/>

微控制器很便宜，传感器很便宜，甚至马达也很便宜。那么为什么好的轮式机器人平台都那么贵呢？[Dimitris Platis]想要开发一个负担得起的平台来试验漫游者，但是他使用的廉价塑料底盘给他带来了各种各样的问题。所以他做了任何优秀黑客都会做的事情，[并自己构建了一个更好的版本](https://platis.solutions/blog/2020/02/16/smartcar-gets-an-esp32-upgrade/)。

有趣的是，[Dimitris]决定采用由两块 PCB 板制成的机箱。安装在小角度支架上的电机直接用螺栓固定在下部 PCB 上。这些也不是标准的 2 美元 DC 罐头。每个 JGB37-520 齿轮减速电机都配有编码器，允许您的软件确定速度、距离和方向。上面的 PCB 通过几排引脚头连接到下面的 PCB，并充当当时您可能正在试验的任何电子有效载荷的主机。

[![](img/bbb588c0fd1276c57afb40250d286969.png)](https://hackaday.com/wp-content/uploads/2020/02/esp32car_detail.jpg) 对于控制器，[Dimitris]说 ESP32 很难被你想用的几乎任何指标击败。凭借集成的无线技术和强大的计算能力，有大量选项可以远程或自主控制您的小漫游车。但他也表示，如果你想开发定制版本，已经尽一切努力确保你可以用其他东西替换微控制器。

整个想法[让我们想起了过去见过的四轴飞行器](https://hackaday.com/2012/04/16/tiny-quadcopter-gets-an-update-on-the-virge-of-flying-without-pc/)，其中 PCB 在结构上不仅仅是用来固定电机和硬件的地方，而是实际上包含功能迹线和组件，减少了所需的布线数量。自然，这意味着底盘的任何损坏都可能削弱电子设备，但据推测，这就是大泡沫保险杠的作用。

[Dimitris]设计这个项目是为了教育用途，所以他假设你想为整个教室建造 10 或 12 个这样的设备。他说，以这些数量计算，每个机器人的成本大约为 60 美元。他说，如果你想进一步降低价格，交换电机将是你的最佳选择，因为它们是设计中最昂贵的组件。也就是说，60 美元购买一个高质量的开源漫游平台对我们来说很公平。

还是太多了？你可以看看我们多年来报道的 [3D 可打印漫游者设计](https://hackaday.com/2018/10/29/low-cost-autonomous-rover-will-drive-your-projects/)。或者看你能不能走运[从清仓架上拿起一个廉价机器人黑掉](https://hackaday.com/2020/01/20/teardown-bilbot-bluetooth-robot/)。