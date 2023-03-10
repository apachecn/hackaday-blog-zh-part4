# 黑客入侵的 360 度摄像头捕捉不到任何东西

> 原文：<https://hackaday.com/2019/10/18/miss-nothing-with-a-hacked-360-degree-camera-trap/>

相机陷阱是野生动物保护和研究中非常常见的工具，但正确放置和指向它们可能有点像猜谜游戏。一些非常有趣的事情可能会发生，而你却一无所知。巴拿马数字自然主义实验室的 Andrew Quitmeyer 和 Danielle Hoogendijk 正在试验被黑客入侵的消费者 360 度 T2 T3 相机 T4 来帮助解决这个问题。

这个项目叫做 Panatrap，看起来很有前景。他们已经对许多不同的 360 相机进行了非常详细的测试，并使用小米 Misphere 和 理光 Theta V 构建了功能原型。小米在相机底部有一些方便的触点，用于其自拍杆接口(简单的电阻和按钮)，可以完全控制相机。Arduino 兼容板等待来自 PIR 传感器的运动检测信号，然后 PIR 传感器向摄像机发送所需的命令，以唤醒摄像机并拍摄镜头。理光略具挑战性，但他们发现，如果从青少年的 USB 端口接收到模拟键盘命令，相机将会唤醒。触发是由一个伺服推动相机的按钮来完成的。 所有东西都装在一个激光切割的亚克力盒子里，以帮助它在潮湿的丛林中生存。如果有人知道如何破解 Samsung Gear 摄像头，我们的团队渴望听到您的反馈！ 

所有的工作都是开源的，构建细节和硬件设计可以在项目页面上找到，软件可以在 [Github](https://github.com/Digital-Naturalism-Laboratories/Panatrap) 上找到。休息之后，看看一些当地野生动物的 360°测试视频。我们期待更多的镜头！

 [https://www.youtube.com/embed/AOXLAcXRMOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AOXLAcXRMOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你可以用树莓派来制作自己最基本的[360°相机。也可以看看我们最近关于大猩猩保护英雄](https://hackaday.com/2016/10/09/cheap-360-degree-camera/)[戴安·福西的文章。](https://hackaday.com/2019/09/03/dian-fossey-gorilla-girl/)