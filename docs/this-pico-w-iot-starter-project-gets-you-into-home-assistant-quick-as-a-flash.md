# 这个 Pico-W 物联网入门项目可以让您快速进入家庭助理

> 原文：<https://hackaday.com/2022/09/03/this-pico-w-iot-starter-project-gets-you-into-home-assistant-quick-as-a-flash/>

我们当中许多具有一些硬件知识和一知半解的嵌入式经验的黑客都想进入家庭自动化领域，但这需要相当长的学习曲线。如果你正在寻找一个可破解的起点；一些需要部署、学习和扩展的东西，然后看看来自[达尼洛·坎波斯]的 PicoW Home Assistant Starter 项目。

该项目基于 arduino-pico 核心，它支持一大堆基于 RP2040 的主板，所以你不需要将自己限制在“官方”的 Pico-W 上，只要你有工作网络、Wi-Fi 或其他。集成是由 [arduino-home-assistant](https://github.com/dawidchyrzynski/arduino-home-assistant) 库提供的，它充当了你的传感器和其他小部件、MQTT 之间的桥梁，并由此延伸到网络之外。端点上的事件和传感器数据与 MQTT 打包在一起，并通过提供的网络发布给代理，所有这一切只需最少的初始工作。一旦你与你的家庭助手实例建立了基本的连接，在 arduino-home-assistant GitHub 页面上有许多代码示例，可以帮助你开始连接任何你想连接的东西。

事实证明，我们已经在这些公平的页面上覆盖了相当多的 HA，例如，这些可爱的[自动百叶窗](https://hackaday.com/2021/09/26/automated-window-blinds-using-mqtt-and-home-assistant/)。另一个黑客使用床腿下的[测压元件来检测某人是否在床上](https://hackaday.com/2019/09/11/does-your-home-assistant-know-when-you-are-sleeping/)，如果这不是你的事情，也许你心目中的家庭助手是[更像这个](https://hackaday.com/2022/04/23/2022-sci-fi-contest-your-home-assistant-hal-9000/)？