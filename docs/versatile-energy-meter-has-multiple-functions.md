# 多功能电能表具有多种功能

> 原文：<https://hackaday.com/2020/07/22/versatile-energy-meter-has-multiple-functions/>

如果你在处理太阳能或电池能源，你可能会想要一个由[开放绿色能源]制造的这种小型[能量计](https://www.instructables.com/id/DIY-Arduino-Multifunction-Energy-Meter/)。基于 Arduino 的仪器测量 DC 电压、电流、功率、能量、容量和温度。范围只有 26 伏和 3.2 安培，但你可以用一些外部电路来扩展。

当然，用 Arduino 测量电压已经过时了。但 INA219 电流传感器的加入在单个模块中提供了电压、电流和功率测量，并将 I2C 传回主机。

虽然他也在 PCB 上工作，但布局很整洁。这种基本电路只需对软件进行少量修改，就可以很好地用于数据记录器或电流监控器。

如果你喜欢这种东西，INA219 实际上有两个版本。“A”版本不如“B”版本精确。不过，差别很小。根据数据手册，“A”版本在整个温度范围内的电流测量误差最高可达 1%，而“B”版本则保持在 0.5%。正常工作条件下，这两款器件的典型值都在 0.2%左右。

该器件采用外部分流电阻工作，因此它测量分流电阻一端的电源电压，通过观察另一端的电压差，就可以计算出电流量。

如果你想知道一台价值 8000 美元的仪器在电流测量方面能做些什么，看看 Keithley 2460 SourceMeter 。如果你的预算有点少，有[的 Joulescope](https://hackaday.com/2019/03/06/joulescope-dc-energy-analyzer-reviewed/) 。

 [https://www.youtube.com/embed/V3hhX_TEYjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V3hhX_TEYjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

