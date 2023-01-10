# 车载电话——不，不是那种

> 原文：<https://hackaday.com/2019/08/27/a-car-phone-no-not-that-kind/>

对于普通黑客来说，自动驾驶汽车开发是一个相对难以捉摸的技术领域，需要一整辆汽车等等。Piotr Sokólski 没有处理如此大规模的挑战，而是转向在小型无线电遥控汽车上实施相同的原则。

为了降低开发自动驾驶汽车软件的门槛，他的设计基于你可能已经拥有的东西:智能手机。他引用了谷歌 Cardboard 项目作为自己的灵感，该项目如何在不需要昂贵硬件的情况下使虚拟现实变得更容易实现。这款手机能够通过一个定制板来控制致动器和车轮电机，并通过蓝牙连接与之对话。由于摄像头指向手机安装在框架中的方向，[Piotr]想出了一个非常聪明的解决方案，使用镜子作为潜望镜，这样汽车就可以看到自己的前方。

这里的软件有两个部分，尽管手机应用 one 不仅仅是作为一个界面，通过发送视频信号进行处理。整个计算机视觉处理是在桌面部分完成的，它允许[Piotr]做一些有趣的事情，比如使用强化学习来尽可能长时间地保持汽车行驶而不发生碰撞。这是通过让算法观察来自手机的图像，并在加速度计检测到碰撞时给予负面奖励来实现的。他做的另一个实验是使用汽车顶部的 QR 标签，固定的头顶摄像头可以看到，以确定汽车在房间中的位置。

这可能不是第一次[有人制作自动驾驶汽车](https://hackaday.com/2017/06/06/self-driving-rc-cars-with-tensorflow-raspberry-pi-or-macbook-onboard/)的缩小模型，尽管它是设计最巧妙的汽车之一，而且它肯定比[试图在你车库里的全尺寸汽车上做这件事](https://hackaday.com/2015/12/17/self-driving-acura-built-in-a-garage/)简单得多。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/TzK58WcRrrI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TzK58WcRrrI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

