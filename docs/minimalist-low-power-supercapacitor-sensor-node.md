# 极简低功率超级电容器传感器节点

> 原文：<https://hackaday.com/2020/11/04/minimalist-low-power-supercapacitor-sensor-node/>

无线传感器网络面临的最大挑战之一是功耗。太阳能电池板产生的电能通常比你希望的要少，尤其是小型太阳能电池板，而且设计超低功耗电路也很棘手。[Strange.rand]已经掉进了低功耗的兔子洞，正在设计一种低成本的[无线传感器节点，它依靠太阳能和超级电容器](https://hackaday.io/project/175514-wireless-solar-powered-sensor-node)运行。

传感器节点的主要组件是运行在 4Mhz 的 ATMega 328P 微控制器、RFM69 无线电收发器、I2C 温度/湿度传感器、1F 超级电容器和小型太阳能电池板。无线电、MCU 和传感器都在 1.5-3.6V 的电压下运行，但超级电容和太阳能电池板的组合可以达到 5.5V。为了调节较低电压组件的功率，低压降稳压器似乎是最简单的解决方案，但[strange.rand]发现，当电压降至 3.3V 以下时，3.3V 稳压器会额外消耗 20uA 或更多。相反，他选择消除 LDO，并用基于比较器的过压保护电路将电容的充电电压限制在 3.6V。使用这种配置，电路能够在一次充电下运行 42 小时，在高于 2.7V 时每分钟传输一次数据，低于 2.7V 时每三分钟传输一次数据。

另一个挑战是欠压保护。[strange.rand]发现，当 ATmega 在 1.8V 以下进入掉电状态时，它会消耗未记录的 3-5 mA 电流。小型太阳能电池板仅产生 1 mA 电流，因此 MCU 会阻止超级电容器再次充电。他用另一个比较器电路来切断其他元件的电源，从而解决了这个问题。

环境传感器和气象站的太阳能电池板越来越小，我们经常遇到这样的挑战。对于通信来说，[低功耗的亚 Ghz 无线电](https://hackaday.io/project/163922-low-power-high-accuracy-weather-station)可能是你最好的选择，但如果你想使用 WiFi，你可以[用几个技巧降低功耗](https://hackaday.com/2018/11/04/weather-station-is-a-tutorial-in-low-power-design/)。