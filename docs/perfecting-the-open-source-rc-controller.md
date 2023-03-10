# 完善开源 RC 控制器

> 原文：<https://hackaday.com/2019/05/15/perfecting-the-open-source-rc-controller/>

在过去的几个月里，我们已经看到大量自制的遥控控制器涌入我们的生活，我们当然不会抱怨。虽然商业 RC 发射器的价格处于历史最低点，其中许多甚至可以运行开源固件，但仍然没有什么比自己动手制作更好的了。除此之外，你还能怎样得到你想要的东西呢？

[![](img/97f40bfedfc309f8454a3bff46c56da2.png)](https://hackaday.com/wp-content/uploads/2019/05/openrctx_detail.jpg) 为了入围 2019 年黑客日大奖，[【熊伟·德·米兰达·恩里克】正在研发自己版本的终极开源遥控器](https://hackaday.io/project/164881-openrc-transmitter)。他的设计遵循了我们在外观设计和硬件可扩展性方面已经看到的一些趋势，但也分支到一些新的领域，如双集成显示器。

为什么您的控制器需要两个显示器？顶部的 4.3 英寸 TFT 连接到 5.2 GHz 的视频接收器，这使得它非常适合以“第一人称”的视角控制车辆，如无人机。下面的屏幕是 Adafruit 的 2.8 英寸触摸屏，一旦固件完全充实，它将用于导航菜单和选项。

为控制器供电的是一个 ESP32 和双 MCP23017 GPIO 扩展器，可连接到用户可用的输入设备阵列。控制器的当前版本有十个开关、两个编码器、一些按钮和一对滚轮。哦，当然还有几个操纵杆。所有器件都端接在控制器背面的定制 PCB 上，这使得修改和添加输入设备变得简单而整洁。

我们之前已经见过阿尔法 V1 ，一个具有相当相似设置的开源控制器，尽管没有双显示器。如果这个比你想要的稍微复杂一点，[你总是可以用 Arduino](https://hackaday.com/2019/03/19/diy-six-channel-arduino-rc-transmitter/) 来做。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)