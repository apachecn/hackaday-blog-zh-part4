# 把智能手机机器人的控制权交给树莓派

> 原文：<https://hackaday.com/2021/07/21/giving-control-of-a-smartphone-robot-to-a-raspberry-pi/>

大多数与智能手机连接的设备寿命都很短，最终不可避免地成为电子垃圾。除非黑客给他们第二次生命，就像智能手机控制的小机器人罗莫一样。[David Goeken]已经成功地对通信协议进行了逆向工程，允许罗莫控制 Raspberry Pi(或微控制器)

罗莫是一个由 iPhone 控制的小机器人，在 2013 年的 Kickstarter 活动中被推向市场。它最初使用 iPhone 的音频插孔作为控制接口，但很快就出现了使用 iPhone 4 的 30 针连接器和后来的 Lightning 端口的更新版本。罗莫背后的 Romotive 公司最终倒闭了，但幸运的是，他们开源了 IOS 应用程序和固件。这导致目前 app store 上只有少数第三方应用。

[David]想要使用其他硬件进行控制，所以他开始使用开源软件和逻辑分析仪对协议进行逆向工程。不出所料，它使用串行接口来发送和接收命令，还有两个额外的引脚来检测连接和唤醒罗莫。在断开电路板上的接口插头后，他能够修改罗莫以安装一个 Raspberry Pi Zero，并使用内部电池供电。

[David]还没有公开他的代码，但听起来他打算公开。看起来罗莫的可以成为一个有趣的小实验平台，而且在易贝可以买到便宜的。我们在 2014 年报道过另一个很酷的罗莫黑客，它使用[投影仪和视觉系统创建了一个类似 Mariokart 的游戏](https://hackaday.com/2014/10/04/your-living-room-becomes-next-mario-kart-course/)。对于完全开源的智能手机机器人，请查看 [OpenBot](https://hackaday.com/2020/11/06/open-source-self-driving-smartphone-robot/) 。