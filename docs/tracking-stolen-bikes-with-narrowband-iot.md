# 利用窄带物联网追踪被盗自行车

> 原文：<https://hackaday.com/2019/05/20/tracking-stolen-bikes-with-narrowband-iot/>

为了参加 2019 年 Hackaday 奖，[Marin Vukosav]正在进行一个雄心勃勃的项目，以创建一个小型 GPS 跟踪设备，利用窄带物联网(NB-IoT) 进行远程通信。NB-IoT 不使用会在短时间内吸干电池的 GSM 调制解调器，理论上可以在 10 到 15 公里的范围内保持连接，同时保持足够低的能耗，使追踪器可以在需要充电前长达一年。

此时，硬件仍处于概念验证阶段。[Marin]正在使用一个带有 GPS 屏蔽和 SIM7000 NB-IoT 模块的 Arduino 来试验这个概念，但最终他说他希望将硬件缩小到可以放在自行车灯内的程度。展望更远的未来，他希望与自行车制造商达成协议，这样模块就可以集成到车架本身，小偷根本无法接触到它。

当然，没有人说这项技术必须局限于自行车。如果[马林]能让它足够小，甚至能达到他的目标电池寿命的一半，他手上就会有一个非常引人注目的产品。谁不想在他们的远程无人机上增加这样的东西以防丢失呢？

这个项目还有很长的路要走，而且不全是硬件。[马林]还必须创建软件方面的东西，一个网站，你可以注册你的追踪器，并能够在地图上查看其近乎实时的位置。这需要做大量的工作，尤其是如果你打算把它变成一个商业产品，我们非常有兴趣继续跟进，看看这个项目全年的进展情况。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)