# 一次攀登一座山峰——并记录下来

> 原文：<https://hackaday.com/2020/10/17/climbing-everest-one-hill-at-a-time-and-keeping-track-of-it/>

互联网充满了自我宣称的挑战，从一些绝对无意义的时尚到有实际目的的精心设计的任务。在抖音时代，后者当然越来越少，因为快速、轻松地赶上潮流更容易提高你的互联网积分。另一方面，骑自行车的人喜欢一个很好的挑战，他们在网上互相竞争，测试他们的技能，并在途中将他们最喜欢的活动游戏化。其中一个选择是 *Everesting* ，你选择一座山，在一次训练中，你可以骑着它上上下下多次，直到你在上面积累了珠穆朗玛峰的高度。这个想法引起了他的兴趣，但不是它的竞争方面，[rabbitcreek]开始好奇他用自己的休闲自行车用法[需要多长时间才能达到这个目标，所以他建造了一台自行车计算机来测量和跟踪它](https://www.instructables.com/BikeEverest/)。

虽然总距离和时间是真正挑战的因素，但[rabbitcreek]的主要兴趣是累计高度，因此该设备的主要组件是一个连接到电池供电的 ESP32 的[BMP 388](https://www.bosch-sensortec.com/products/environmental-sensors/pressure-sensors/pressure-sensors-bmp388.html)气压传感器。一个电子纸显示屏显示总高度和完成百分比，以及一些随机的珠穆朗玛峰相关图片。所有东西都整齐地包装在一个 3D 打印的盒子里，可以安装在自行车的车把上，STL 文件和源代码可以在他的文章中找到。

当然，如果你真的对挑战本身感兴趣，你可能会有各种各样的运动跟踪设备，但这是一个很好的补充，可以在你进行跟踪的同时，降低勒索软件攻击的风险。如果[rabbitcreek]听起来对你来说是一个熟悉的名字，他确实已经成为一名黑客常客，他的环境黑客如[潮汐时钟](https://hackaday.com/2018/09/09/the-tide-is-high-and-this-clock-lets-you-know/)、[手持粒子嗅探器](https://hackaday.com/2020/04/02/particle-sniffer-for-pollution-point-sources/)或[记录阿拉斯加荒野的温度](https://hackaday.com/2019/08/22/temperature-logging-on-the-last-frontier/)。