# USB 适配器隔离多个串行接口

> 原文：<https://hackaday.com/2020/10/13/usb-adaptor-isolates-multiple-serial-interfaces/>

你需要一把串行通信的瑞士军刀？Ollie 是一款[紧凑型隔离 USB 适配器](https://www.crowdsupply.com/ali-slim/ollie)，提供 USB、CAN 总线和两个逻辑、RS-232 和 RS-485 信号电平的 UARTs，以及一个隔离电源。[Slimelec]已经设法将所有这些都压缩到一个口琴大小的包装中。我们喜欢使用 PCB 材料制作外壳的技术，包括清晰标注的开关、led 和连接器引脚名称。

到目前为止，这个项目只有编译好的[固件可用](https://github.com/slimelec/ollie-hw)，但是硬件文件，大概还有源代码和文档，很快就会出来。

这里的中心主题是隔离和灵活性。我们在项目规格中找不到隔离电压，但该适配器所基于的 [CANable 项目](https://canable.io)提供 2.5 kV 电流隔离。标准 A 型连接器上还提供一个隔离 USB 接口。四线逻辑电平 UART 信号可在 2 x 7 盒式接头上获得，并且电压可选。RS-232、RS-485 和 CAN 信号位于 8 针可插拔螺丝端子板上，或者您可以使用带可插拔适配器板的 DB9 连接器。

无论您是需要现场测试的故障排除帮助，还是在您的项目中使用 CAN 总线，或者只是想将您昂贵的计算机与粗略的原型硬件隔离，请看看这个项目。