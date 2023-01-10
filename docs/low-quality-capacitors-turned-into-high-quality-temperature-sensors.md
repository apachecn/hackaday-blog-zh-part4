# 低质量的电容器变成了高质量的温度传感器

> 原文：<https://hackaday.com/2018/08/23/low-quality-capacitors-turned-into-high-quality-temperature-sensors/>

当生活给你一堆劣质电容器时，你会怎么做？[做一大堆温度传感器](https://www.instructables.com/id/Use-Capacitors-to-Measure-Temperature/)，显然。

问题中的不太显眼的帽子是通过我们非常喜欢购买的一个多功能组合套件来到[pyromania 303]的。储存了许多价值的电容器，像这样的套件是非常好的，尤其是当它们有高质量的元件时。但是并不是所有的陶瓷瓶盖都是一样的，因此[pyromania 303]决心不让质量较差的瓶盖浪费掉。数据手册显示，Y5V 电介质电容具有极高的温度系数，可用作有用的传感器。一个小铜板上有一个电容和一个串联电阻；Arduino 输出引脚通过电阻对电容充电，测量连接到电容另一端的输入引脚变为高电平所需的时间。充电时间与温度成正比，几次校准运行表明，响应非常线性。不幸的是，温度系数在 10°C 时达到峰值，并在该点以下急剧下降，使得传感器仅在峰值的一侧有用。尽管如此，这仍然是一个有趣的方式来使用不喜欢的部分，也是一个需要记住的方便提示。

温度传感并不是电容唯一能做到的。我们之前已经看到它们[变成了触摸传感器](https://hackaday.com/2015/11/30/conjuring-capacitive-touch-sensors-from-paper-and-aluminum-foil/)，并且曾经[把 3D 打印机变成了 3D 扫描仪](https://hackaday.com/2017/01/13/custom-sensor-head-turns-3d-printer-into-capacitive-scanner/)。