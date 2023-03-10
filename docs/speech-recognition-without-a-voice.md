# 没有声音的语音识别

> 原文：<https://hackaday.com/2018/09/14/speech-recognition-without-a-voice/>

过去几年人机交互最大的变化是语音助手的兴起。Siris 和 Alexas 是我们的 HAL 9000s，很快我们就会用这些助手打开车库门。这次他们可能会这么做。

如果你可以和这些语音助手一句话不说，会发生什么？那会是心灵感应吗？这正是[Annie Ho]在今年 Hackaday 奖的项目 Cerebro Voice 中所做的。

其核心是，Cerebro Voice 背后的想法基于[次声识别](https://en.wikipedia.org/wiki/Subvocal_recognition)，这是一种检测来自声带和其他参与说话的肌肉的电信号的技术。这些电信号由表面肌电设备收集，然后发送到计算机进行处理并重建成文字。这是一项经过验证的技术，甚至 NASA 都称之为“合成心灵感应”。

这个项目背后的团队正处于这种设备原型的早期阶段，到目前为止，他们正在使用 EMG 硬件和麦克风来训练一个卷积神经网络，该网络将电信号转化为用户的内心独白。这是一个令人惊叹的项目，也是我们在今年 Hackaday 奖的人机界面挑战中看到的最好的项目之一。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)