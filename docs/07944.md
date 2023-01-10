# 光纤，但是…更湿？

> 原文：<https://hackaday.com/2020/09/29/fiber-optics-but-wetter/>

光纤是以闪电般的速度传输大量数据的绝佳方式。由于全内反射的特性，允许光像流体一样通过管道在玻璃纤维中流动，它们可以用于长距离通信，并形成现代通信网络的主干。然而，水也能够实现全内反射聚会的把戏，[和【Mike Kohn】决定看看它是否也可以用作交流媒介。](https://www.mikekohn.net/micro/water_optic_communication.php)

实验装置由 ATTiny85 组成，它通过其串行端口接收信号，并通过闪烁 LED 输出接收到的位。这个发光二极管连接在一个装满水的塑料管上。在接收端，另一个 ATTiny85 读取置于显像管另一端的光电二极管的电压电平。当 ADC 检测到电压超过一定水平时，它会触发一个连接到串行 RX 引脚的引脚。

将该装置连接到一对终端上，仅用一个 LED 和一个小型微控制器，[Mike]就能够通过一个装满水的管子成功传输 9600 波特的串行数据。为了验证成功，他用一根充气管再次进行了测试，结果失败了。通过这样做，他证明了水在做功。

我们也见过其他光学数据黑客——[像这个令人敬畏的激光以太网构建。](https://hackaday.com/2017/04/19/go-wireless-with-this-diy-laser-ethernet-link/)休息后的视频。

 [https://www.youtube.com/embed/Mk4rtyzDQp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mk4rtyzDQp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

