# 适用于各种项目的 DIY 风速计

> 原文：<https://hackaday.com/2021/10/11/diy-anemometer-for-projects-big-and-small/>

当[Fab]的最新项目需要一个风速计时，他被商业选项的有限范围和相对较高的价格所阻碍。他没有被吓倒，他的解决方案是一个令人印象深刻的 DIY 风速计，可以与现成的替代产品相媲美。

AnemoSens 完全是作为雄心勃勃的 [WinDIY_2 水平轴风力涡轮机](https://hackaday.io/project/179999-windiy2-horizontal-axis-wind-turbine)的一个组件而设计的，然而它也适合作为标准家庭气象站的一部分。微控制器单元使用 RS485/Modbus 连接，确保来自风传感器的数据可以跨各种平台访问。通过 USB 和 SD cart 插槽的串行流也可用于记录数据，后者对于长期无人监管的监控特别有用。[Fab]还集成了一个 ESP32，用于空中记录数据。

MCU 还具有古老的 BME280 的位置，BME 280 是一种相对精确的温度、压力和湿度传感器，经常部署在 DIY 气象站中。这感觉很好，因为这意味着风速计包可以单独作为一个基本的天气传感站，或作为更复杂的环境监测的备份。

原型目前使用霍尔效应传感器来测量风速，而 AS5048B 磁性旋转编码器在测量旋转(风向)方面做得不错。可能需要一些校准来提高这种设置的精度，但这是一个有希望的开始。

[Fab]已经发现了轴承的一些缺点，但对未来的迭代有一个计划。他可能想看看这个使用旧硬盘轴承的备用风速计。

 [https://www.youtube.com/embed/w3RU5c9Zf3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w3RU5c9Zf3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

