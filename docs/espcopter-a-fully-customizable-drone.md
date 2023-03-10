# ESPcopter:完全可定制的无人机

> 原文：<https://hackaday.com/2019/09/25/espcopter-a-fully-customizable-drone/>

由于有如此多的避障能力，无人机的唯一自然发展就是手动控制。对于土耳其发明家[metehanemlik]来说，即使这也不足以成为一个挑战，因为他决定创造由 ESP8266 驱动的迷你无人机: [ESPcopter](https://hackaday.io/project/167079-make-a-hand-control-drone) ，这是一种可编程的 Arduino 兼容模块化无人机，可以通过扩展护盾进行改装。DIY 爱好者不仅可以修改用于避障的算法，而且无人机可以调整到适合他们需求的任何尺寸。

无人机几乎完全由扩展护盾建造，包括多游侠护盾，在无人机的前、后、右和左方向上有四个 VL53L0x 激光测距传感器。ESPcopter 的[网站](https://espcopter.com/)带有一个 SDK，用户可以轻松修改无人机 MCU 和引脚上运行的软件，以更好地了解其硬件功能。令人印象深刻的是，它通过为期 60 天的众筹活动获得了全部资金，并将很快进行第二次发布，其中包括一些新的和改进的功能。

电力来自一个 26 毫安时的 LiPo 电池，允许长达 6 分钟的飞行时间；包括三轴陀螺仪、加速度计和磁力计；在 ESP8266-12S 32 位 MCU 上运行；通过 USB 连接在 45 分钟内充满电；重约 35 克；并且从马达到马达大约为 90 毫米。

![](img/47c70babccef1e61ae21636099a258c3.png)

该软件包括一个与 Arduino IDE 兼容的 ESPcopter 库，其中包括飞行控制软件，使无人机的飞行稳定。还有一些例子说明了如何构建一个自包含的 web 服务器，以允许用户从手机、平板电脑或笔记本电脑上控制无人机。从远程设备的控制屏幕上，用户可以使用控制操纵杆控制俯仰、滚转、偏航和油门，同时还可以在航线模拟上模拟飞行。

![](img/9b8a73d9abb774e813537067024f310f.png)

使用 SDK，用户可以实现中值滤波器、互补滤波器和 PID 算法，从而有效地为他们的无人机功能提供全方位的可能性。

ESPcopter 项目最有用的部分？已经有一个充满活力的在线社区，来自世界各地的 DIY 爱好者正在谈论衍生项目，从第一人称视角(FPV)相机设置，对成群的无人机进行编程，甚至建立教育视频合作。

 [https://www.youtube.com/embed/LB4Lqe8Wtn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LB4Lqe8Wtn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)