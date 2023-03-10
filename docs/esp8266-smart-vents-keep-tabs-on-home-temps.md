# ESP8266 智能透气产品可监控家庭温度

> 原文：<https://hackaday.com/2022/08/18/esp8266-smart-vents-keep-tabs-on-home-temps/>

你有没有发现，尽管有中央供暖和空调系统，但并不是你家里所有的房间都达到了你想要的温度？也许当暖气开着的时候，餐厅太热了，或者在夏天的几个月里，卧室似乎从来没有足够的凉爽。如果那听起来像你的房子，那么这些来自[Tony Brobston]的电动“智能通风口”可能正是你所需要的。

[![](img/9856daa8788c0cce7fac87944a5dc5ad.png)](https://hackaday.com/wp-content/uploads/2022/08/smartvent_detail.jpg) 这里的想法非常简单:一个 ESP8266 和一个伺服系统内置在 3D 打印的通风口寄存器中，这允许它控制其百叶窗的位置。当通过 MQTT 连接到您的家庭自动化系统时，通风口允许您根据您希望的任何参数单独控制每个房间的气流。最有可能的是，你会想将这些通风口与分布在整个房子的[温度计阵列配对。](https://hackaday.com/2020/12/08/exploring-custom-firmware-on-xiaomi-thermometers/)

虽然[托尼]说这个设计仍然需要一些测试，但他已经发布了尺寸范围从 2×10 到 6×12 英寸的智能透气产品。他还提供了关于如何打印、组装和编程这些设备的优秀文档。很明显，这个项目的每一个元素都经过了大量的关注和思考，我们很兴奋地看到随着项目的公开，新的想法和贡献者将会不可避免地出现，从而进一步发展这个项目。

想为您的暖通空调系统增加一些自动化功能，但没有一个别致的中央单元？别担心，只要[你的加热器或空调有一个红外遥控器](https://hackaday.com/2018/08/25/air-conditioner-remote-reverse-engineered-despite-esoteric-protocol/)，你就能[将一个支持 WiFi 的微控制器嵌入方程式](https://hackaday.com/2019/06/11/smarten-up-your-air-conditioning-with-the-esp8266/)。

 [https://www.youtube.com/embed/ANneINQjgso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ANneINQjgso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

