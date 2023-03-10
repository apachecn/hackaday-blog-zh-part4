# UART 不行？Arduino CANSerial Can！

> 原文：<https://hackaday.com/2022/07/04/uart-cant-arduino-canserial-can/>

[雅各布·盖格]有一个问题。在 AVR Arduino 项目中，一个 GPS 单元和一个蓝牙转串口绑定了所有的硬件 UARTs。我听到你说“软件连载”。但是如果我告诉你[Jacob]已经让有问题的电路板通过 CAN 总线发送数据了呢？

【Jacob】的甜蜜黑客[在 Arduino 代码](https://github.com/techie66/CANSerial)内创建任意数量的 CAN“设备”，并可以将它们中的每一个视为自己的串行数据通道。毕竟，CAN 中的“N”代表网络。诀窍是为每个所需的 can 串行接口创建一个设备 ID，这是在他的库中使用通常的 Arduino 设置步骤完成的。缓冲器负责存储所有不同的通道，直到它们可以通过硬件 can 外设推出。在大型计算机方面，一些软件监听不同的“设备”枚举 id，并给每个 id 分配一个虚拟串行端口。

虽然这是一个必要的攻击，但我们可以把它看作是一个聪明的机会，把来自微控制器的信息分成不同的流。可能是调试通道、命令通道和数据通道？它们是虚拟设备，所以疯狂吧！

虽然我们通常看到 CANbus 在它的自然栖息地——在你的车里——但想想我们可以把它用在什么地方也很酷。比如，[控制 3D 打印机](https://hackaday.com/2021/11/03/simplify-3d-printer-wiring-with-can-bus/)。需要[一个可以进修的](https://hackaday.com/2020/07/02/custom-packet-sniffer-is-a-great-way-to-learn-can/)？我们正好有票。

【公交图片:[马耳他公交；终点，瓦莱塔](https://www.flickr.com/photos/43145783@N00/3117107491)约翰·哈斯拉姆。罐头照片:[油漆罐](https://www.flickr.com/photos/61926883@N00/3413845072)丹尼尔·r·布鲁姆。可怕的视觉双关:恐怕是我们的错。你试试找 CANbus 代码的图片！]