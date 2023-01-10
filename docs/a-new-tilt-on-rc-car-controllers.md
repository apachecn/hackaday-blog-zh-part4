# 遥控汽车控制器的新倾斜

> 原文：<https://hackaday.com/2018/10/02/a-new-tilt-on-rc-car-controllers/>

如果你是所有遥控物品的爱好者，很可能你对控制器略知一二。你会有一两个东西，既有熟悉的双操纵杆型，也有手枪握柄型。但是你有没有想过也许还有别的方法可以做到这一点？ELECTRONOOBS [的 Andrei 发布了一份倾斜控制遥控汽车的指南](https://www.electronoobs.com/eng_arduino_tut44.php)。这是一个很好的例子，说明如何将简单的部分连接在一起，使一些新颖和有趣的东西，对于一个有抱负的黑客来说，这是一个很好的起步项目。

Arduino Nano 通过 I2C 总线读取加速度计，并通过一对 HC-12 无线模块的无线链接发送命令。另一个安装在汽车上的 Nano 解码命令，并使用一对 H 桥[，我们已经详细介绍过](http://hackaday.com/2014/04/25/a-h-bridge-motor-controller-tutorial-makes-it-simple-to-understand/)，来控制电机。

本教程做得很好，包括硬件的细节和你需要的所有代码。休息之后，请观看构建和演示视频。

 [https://www.youtube.com/embed/3GhNX7gTP4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3GhNX7gTP4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们希望看到这个想法通过使用一辆性能更好的基础车，以及更好的转向控制——也许是一辆本田思域？

【感谢 Baldpower 的提示！]