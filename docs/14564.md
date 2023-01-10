# 这是现存最古老的开源 HVAC 项目吗？

> 原文：<https://hackaday.com/2022/08/22/is-this-the-oldest-open-source-hvac-project-in-existence/>

家酿暖通空调系统是那些需要投入大量时间、精力和金钱的项目之一，你必须是一个真正专注的(最好是拥有自己的家)黑客，拥有多种多样的多学科技能，才能实现一个在现实中可以工作的实施方案。一个这样的暖通空调黑客是[瓦迪姆·特卡琴科]和他的多区域家庭气候控制(HCC)项目，我们早在 2007 年就报道过。我们现在有难得的机会来看看 15 年的兼职开发所能产生的改进，当一个项目在他们自己的家里一年到头整天都被使用时。一开始，事情很简单，只需打开和关闭通风机，不需要那些现代的 MQTT 驱动的云计算东西。

目前名为 DZ ( [GitHub 项目链接](https://github.com/home-climate-control/dz))的实现已经使用现代[反应式编程](https://en.wikipedia.org/wiki/Reactive_programming)技术进行了重写(这对 HVAC 控制系统来说显然是一件好事)，HCC 核心应用程序可以在任何 UNIX 上运行，但很适合在 Raspberry Pi 上运行。测量数据(温度、湿度等。)可以从 1 线设备以及 XBee 模块中获取，从而实现安装周围的有线和无线传感。该系统可以根据加热、冷却或通风的需要来控制各种空气管理设备，例如加热器、热泵和风扇。不要忘记经常被忽视的 HVAC 的第三条腿，V 形部分对健康的房子至关重要。远程控制和监测是由一个 Android 应用程序(HCC 远程)提供的，该应用程序允许用户可视化当前状态以及 HCC 目前正在做什么来控制编程的气候。

使用通用 MQTT 协议传输数据，允许简单连接到安装中已经存在的任何传感器或控制器，HCC 为 [ESPHome](https://esphome.io/) 和 [Home Assistant](https://www.home-assistant.io/integrations/climate/) 提供集成，因此围绕现有硬件构建系统有很多选择。这个项目相当大(正如你对这段时间的预期),但[Vadim]想强调的是，他们在这个问题上看到了很多重新发明的轮子，好好看看 HCC 可能会让一些人省去很多在没有如此坚实基础的情况下实现系统的痛苦。

如果你的需求更基本，也许这个简单的基于 ESP8266 的智能通风口就足够了？而且，如果控制系统不是问题，而你对实际的物理实现更感兴趣，为什么不看看这个 [DIY 能量回收呼吸机(ERV)](https://hackaday.com/2020/10/21/how-an-engineer-designs-a-diy-energy-recovery-ventilator/) 项目呢？