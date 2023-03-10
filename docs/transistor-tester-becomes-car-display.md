# 晶体管测试仪成为汽车显示器

> 原文：<https://hackaday.com/2019/01/10/transistor-tester-becomes-car-display/>

如今，电子爱好者很幸运能够获得各种现成的模块，使传感器、屏幕和微控制器能够轻松连接起来。然而，这种工作方式通常会导致项目变得更像 PCB 沙拉而不是成品。通常，有可能从货架上找到与您的需求相近的东西，并将其重新用于工作。这正是[亚伦]所做的。

[Aaron]想在他的经典吉普车上安装一个显示器来显示时间和一些基本参数。需要一个屏幕和一个微控制器，而一个廉价的开源晶体管测试仪已经具备了这一切。它由一个 ATmega-328P 和一个 128 x 64 的图形 LCD 模块组成，拥有[Aaron]一开始就需要的大部分东西。

为了改变设备的用途，[Aaron]开始将 8 MHz 晶体换成 16 MHz 晶体，使其更容易通过 Arduino IDE 进行编程。然后，编写定制固件，与 DS3232 实时时钟、温度和压力传感器通信，并监控电池电压。所有这些都整齐地安装在 3D 打印面板后面的车辆中，图形 LCD 清晰易读——如果你会说德语的话。

[Aaron]列出了各种有助于破解的在线资源，包括晶体管测试仪原理图。我们自己的【亚当·法比奥】[在 2015 年回顾了这些单元。](https://hackaday.com/2015/04/24/review-transistor-tester/)

如果你自己已经聪明地重用了一些现有的硬件，请务必通过举报热线让我们知道。休息后的视频。

 [https://www.youtube.com/embed/jnhgDS_JZ6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jnhgDS_JZ6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/rKaVass03LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rKaVass03LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

